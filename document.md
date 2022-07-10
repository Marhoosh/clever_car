# MOVE类

> 此类负责控制小车移动

* turn_up(speed,time)

    * 描述：小车以speed速度直行time秒

    * 参数
        * speed：速度  
        * time：小车运行时间，单位为秒
* turn_down(speed,time)
* turn_left(speed,time)
* turn_right(speed,time)
* turn_stop(time)

# TRACK类

> 此类控制小车循迹

do_track()

* 描述：让小车开始自动避障

# MAZE类

> 此类控制小车避障

* do_maze()
    * 描述：让小车开始自动避障

# WAVE类

> 控制舵机转向并测距

* do_angle(angle)

    * 描述：控制舵机转向

    * 参数
        * angle：超声波转向的角度
            * 150 转向正右边
            * 390 转向正中间
            * 750 转向正左边

* measure()

    * 描述：超声波测距
    * 返回值：返回测量到的距离

# LED类

> 控制小车红灯和绿灯亮灭

* do_led(led,level)
    * 描述：使led输出level电平
    * 参数
        * led：车灯
            * 5——红灯
            * 6——绿灯
        * level：电平
            * 1/Ture/GPIO.HIGH——高电平，小灯亮
            * 0/False/GPIO.LOW——低电平，小灯灭

# NOISE类

> 控制蜂鸣器

* do_noise(frequency,t)
    * 描述：使蜂鸣器以frequency频率输出t秒
    * 参数
        * frequency：蜂鸣器频率
        * t：时间，控制蜂鸣器输出时间，单位为秒