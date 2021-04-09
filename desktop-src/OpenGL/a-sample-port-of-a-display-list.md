---
title: 顯示清單的範例埠
description: 本主題提供定義三個顯示清單的程式碼鳶尾花 GL 範例;其中一個顯示清單會參考其定義中的其他顯示清單。 遵循鳶尾花 GL 範例即為程式碼在移植至 OpenGL 時的外觀範例。
ms.assetid: 03283b00-fb5b-4e89-9384-171b38f141ee
keywords:
- 鳶尾花 GL 移植，顯示清單
- 從鳶尾花 GL 進行移植，顯示清單
- 從鳶尾花 GL 移植至 OpenGL，顯示清單
- 從鳶尾花 GL 的 OpenGL 移植，顯示清單
- 顯示清單，從鳶尾花 GL 進行移植
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77a856350a0a248bf7dcac51c36b9d35cf114956
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673155"
---
# <a name="a-sample-port-of-a-display-list"></a><span data-ttu-id="8637f-109">顯示清單的範例埠</span><span class="sxs-lookup"><span data-stu-id="8637f-109">A Sample Port of a Display List</span></span>

<span data-ttu-id="8637f-110">本主題提供定義三個顯示清單的程式碼鳶尾花 GL 範例;其中一個顯示清單會參考其定義中的其他顯示清單。</span><span class="sxs-lookup"><span data-stu-id="8637f-110">This topic gives an IRIS GL sample of code that defines three display lists; one of the display lists refers to the others in its definition.</span></span> <span data-ttu-id="8637f-111">遵循鳶尾花 GL 範例即為程式碼在移植至 OpenGL 時的外觀範例。</span><span class="sxs-lookup"><span data-stu-id="8637f-111">Following the IRIS GL sample is a sample of what the code looks like when ported to OpenGL.</span></span>

## <a name="iris-gl-sample-display-list-code"></a><span data-ttu-id="8637f-112">鳶尾花 GL 範例顯示清單程式碼</span><span class="sxs-lookup"><span data-stu-id="8637f-112">IRIS GL Sample Display List Code</span></span>


```C++
makeobj(10);  // 10 object  
    cpack(0x0000FF); 
    recti(164, 33, 364, 600);   // Hollow rectangle  
closeobj(); 
 
makeobj(20);  // 20 object  
    cpack(0xFFFF00); 
    circle(0, 0, 25);           // Unfilled circle  
    recti(100, 100, 200, 200);  // Filled rectangle  
closeobj(); 
 
makeobj(30);  // 30 object  
    callobj(10); 
    cpack(0xFFFFFF); 
    recti(400, 100, 500, 300);  // Draw filled rectangle  
    callobj(20); 
closeobj(); 
 
// Now draw by calling the lists  
call(30);
```



## <a name="opengl-sample-display-list-code"></a><span data-ttu-id="8637f-113">OpenGL 範例顯示清單程式碼</span><span class="sxs-lookup"><span data-stu-id="8637f-113">OpenGL Sample Display List Code</span></span>

<span data-ttu-id="8637f-114">以下是將上述鳶尾花 GL 程式碼轉譯為 OpenGL：</span><span class="sxs-lookup"><span data-stu-id="8637f-114">Here is the preceding IRIS GL code translated to OpenGL:</span></span>


```C++
glNewList(10, GL_COMPILE);            // List #10  
    glColor3f(1, 0, 0); 
    glRecti(164, 33, 364, 600); 
glEndList(); 
 
glNewList(20, GL_COMPILE);            //List #20  
    glColor3f(1, 1, 0);               // Set color to YELLOW  
    glPolygonMode(GL_BOTH, GL_LINE);  // Unfilled mode  
    glBegin(GL_POLYGON);  // Use polygon to approximate a circle  
        for(i=0; i<100; i++) { 
            cosine = 25 * cos(i * 2 * PI/100.0); 
            sine =   25 * sin(i * 2 * PI/100.0); 
            glVertex2f(cosine, sine); 
        } 
    glEnd(); 
    glBegin(GL_QUADS); 
        glColorf(0, 1, 1);            // Set color to CYAN  
        glVertex2i(100, 100); 
        glVertex2i(100, 200); 
        glVertex2i(200, 200); 
        glVertex2i(100, 200); 
    glEnd(); 
glEndList(); 
 
glNewList(30, GL_COMPILE);            // List #30  
    glCallList(10); 
        glColorf(1, 1, 1);            // Set color to WHITE  
        glRecti(400, 100, 500, 300); 
    glCallList(20); 
glEndList(); 
 
// Execute the display lists  
glCallList(30);
```



 

 




