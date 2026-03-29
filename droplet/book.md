---
title: book
updated: 2026-03-28 21:53:50Z
created: 2026-03-28 14:53:01Z
latitude: 13.08577790
longitude: 74.79425620
altitude: 0.0000
---


#
![382ae6a9a8fcf4635b6dc2af9fef9b19.png](../_resources/382ae6a9a8fcf4635b6dc2af9fef9b19.png)
#
![96ed8dba3e28630885805835afd0aef8.png](../_resources/96ed8dba3e28630885805835afd0aef8.png)
#
![fd9b0b3ae7de1d3c615e442a63519a9b.png](../_resources/fd9b0b3ae7de1d3c615e442a63519a9b.png)
#
![117a062e1aa4123dc74d423f76b7612a.png](../_resources/117a062e1aa4123dc74d423f76b7612a.png)
#
![0f4787ae9331e41aee093e75b32eb718.png](../_resources/0f4787ae9331e41aee093e75b32eb718.png)
# blank[sd]
![489527ca3d5981438a16c34fe60526b2.png](../_resources/489527ca3d5981438a16c34fe60526b2.png)
# 
![7406824d33a0d23576cea6ed8d14f609.png](../_resources/7406824d33a0d23576cea6ed8d14f609.png)
#
![6551097cc81fd7cdafb26fb42989690e.png](../_resources/6551097cc81fd7cdafb26fb42989690e.png)
#
we get theta from data analysis of images 
![82276bd720494e43d99104cde9f52474.png](../_resources/82276bd720494e43d99104cde9f52474.png)
#
![f81b1f8c6306a9d49ff25ae5bc0eea10.png](../_resources/f81b1f8c6306a9d49ff25ae5bc0eea10.png)

# Particle Class 
```
class Particle:
    def __init__(self,i,x,y,
                theta,radius) -> None:
        self.id = i
        self.x = x
        self.y = y
        self.theta = theta
        self.radius = radius
        
def populate_is_occupied(radius,xc,yc,id,is_occupied: NDArray,
                        collisions:List[Tuple[int,int]]):
    Ny,Nx = is_occupied.shape
    
    xa = max(0,int(xc-radius))
    xb = min(Nx , int(xc+radius)+1)
    ya = max(0,int(yc-radius))
    yb = min(Ny , int(yc+radius)+1)
    
    for x in range(xa,xb):
        for y in range(ya,yb):    
            if (x-xc)**2 + (y-yc)**2 <= radius*radius:
                xp = x % Nx
                yp = y % Ny
                if is_occupied[yp,xp] == -1:
                    is_occupied[yp,xp] = id
                else:
                    # so we will define some function like 
                    # def collision
                    collisions.append((id,is_occupied[yp,xp]))
```
![8433587697748601dd57272ddf65e824.png](../_resources/8433587697748601dd57272ddf65e824.png)
#
![9e65cb8cd34cfba633f83ae1597c0adc.png](../_resources/9e65cb8cd34cfba633f83ae1597c0adc.png)!
#
[ff932857c4a74863e725d195e9940ba1.png](../_resources/ff932857c4a74863e725d195e9940ba1.png)
#
![3a459d1f5c953e7ead13778fb027fa4c.png](../_resources/3a459d1f5c953e7ead13778fb027fa4c.png)
#
![952f09f788d0e72b23b0e5a2eca008b7.png](../_resources/952f09f788d0e72b23b0e5a2eca008b7.png)
#
![6ef871e2d5926a084956a4935f2aa02c.png](../_resources/6ef871e2d5926a084956a4935f2aa02c.png)
#
![7fae1aafeb5718e45348872cb342e775.png](../_resources/7fae1aafeb5718e45348872cb342e775.png)
#
![1d275d1fc20fcf999ccc617bb57f0d6a.png](../_resources/1d275d1fc20fcf999ccc617bb57f0d6a.png)
#
![4f8f397ac788542a0393145fb217f31f.png](../_resources/4f8f397ac788542a0393145fb217f31f.png)
#
![8ddad31f466f687bdcba4980a2b3992a.png](../_resources/8ddad31f466f687bdcba4980a2b3992a.png)
#
![586af5cd1104ac0036c7f82c1106a7f3.png](../_resources/586af5cd1104ac0036c7f82c1106a7f3.png)
#
![f481a37c0bfa461b013515318a5a5742.png](../_resources/f481a37c0bfa461b013515318a5a5742.png)
#
![0b05ffa9d56692e59c679b1b288cc56e.png](../_resources/0b05ffa9d56692e59c679b1b288cc56e.png)