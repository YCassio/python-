# python-
import turtle
def drawSnake(rad,angle,len,neckrad):
    for i in range(len):
        turtle.circle(rad,angle)#沿着圆形爬行
        turtle.circle(-rad,angle)
        #参数rad若为负值，则圆形轨迹的半径在乌龟运行的右侧；反之则左侧
        #参数angle表示乌龟沿着圆形爬行的弧度值
    turtle.circle(rad,angle/2)
    turtle.fd(rad)#同turtle.forward()表示乌龟向前直线爬行移动,参数rad表示爬行距离
    turtle.circle(neckrad+1,180)
    turtle.fd(rad*2/3)

def main():
    turtle.setup(1300,800,0,0)#启用一个图形窗口四个参数width,height,startx,starty
    pythonsize=30
    turtle.pensize(pythonsize)#运动轨迹的宽度参数Pythonsize（变量）表示像素大小
    turtle.pencolor("blue")#运动轨迹颜色
    turtle.seth(-40)
    #turtle.seth(angle)函数表示小乌龟启动时的运动方向
    #angle参数是一个角度值，0向东，90向北，180向西，270向南；负值表示相反方向，-40表示东南方向40度
    drawSnake(40,80,5,pythonsize/2)

main()
