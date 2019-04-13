# microbit RCcar controller
input.onButtonPressed(Button.AB, function () {
    radio.sendNumber(10)
    basic.showLeds(`
        . . # . .
        . # . # .
        # . . . #
        . . # . .
        . # . # .
        `)
})
input.onButtonPressed(Button.A, function () {
    radio.sendNumber(2)
    basic.showArrow(ArrowNames.West)
})
input.onButtonPressed(Button.B, function () {
    radio.sendNumber(3)
    basic.showArrow(ArrowNames.East)
})
input.onGesture(Gesture.Shake, function () {
    radio.sendNumber(0)
    basic.showIcon(IconNames.SmallSquare)
})
input.onGesture(Gesture.TiltRight, function () {
    radio.sendNumber(4)
    basic.showLeds(`
        . # . # .
        . # . # .
        . # . # .
        . # . # .
        . # . # .
        `)
})
input.onGesture(Gesture.LogoDown, function () {
    radio.sendNumber(1)
    basic.showArrow(ArrowNames.North)
})
input.onGesture(Gesture.LogoUp, function () {
    radio.sendNumber(5)
    basic.showArrow(ArrowNames.South)
})
radio.setGroup(243)
basic.showIcon(IconNames.Yes)
