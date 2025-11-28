topics: a.box-shadow
        b.text-shadow

a.box-shadow -> inset = box-shadow:inset 0 0 40px green;
             -> conic gradient = background: conic-gradient(from 180deg ,white,black, red,yellow);

Discrete properties in css {Homework} : we cant animate these properties

@property --bgColor{
    syntax: "<color>" ;
    inittial-value: ;
    inherits: false;
}
@property --bgColor {
    syntax: "<color>";
    initial-value: red;
    inherits: false;
}

@keyframes changeBackgroundColor {
    from {
        --bgColor: red;

    }

    to {
        --bgColor: green;
    }
}



.box {
    height: 200px;
    width: 400px;
    /* animation: changeBackgroundColor 5s infinite forwards alternate; */
    border-radius: 20px;
    background-color: var(--bgColor);
    animation: changeBackgroundColor 5s forwards;
}