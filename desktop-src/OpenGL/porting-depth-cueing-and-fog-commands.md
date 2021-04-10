---
title: 移植深度提示和霧化命令
description: 移植深度提示和霧化命令
ms.assetid: 16982d11-88a1-4a35-960f-28f10491e0ac
keywords:
- 鳶尾花 GL 移植，深度提示
- 從鳶尾花 GL、深度提示移植
- 從鳶尾花 GL 移植至 OpenGL，深度提示
- 從鳶尾花 GL、深度提示的 OpenGL 移植
- 鳶尾花 GL 移植，霧化
- 從鳶尾花 GL 進行移植，霧化
- 從鳶尾花 GL 移植至 OpenGL，霧化
- 從鳶尾花 GL 的 OpenGL 移植，霧化
- 深度提示
- 霧
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fd9f65a29e0ae594bf9344cd960d3fc2b9aa646
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183899"
---
# <a name="porting-depth-cueing-and-fog-commands"></a><span data-ttu-id="3ce1a-113">移植深度提示和霧化命令</span><span class="sxs-lookup"><span data-stu-id="3ce1a-113">Porting Depth Cueing and Fog Commands</span></span>

<span data-ttu-id="3ce1a-114">移植深度提示和霧化命令時，請記住下列幾點：</span><span class="sxs-lookup"><span data-stu-id="3ce1a-114">When porting depth-cueing and fog commands, keep the following points in mind:</span></span>

-   <span data-ttu-id="3ce1a-115">鳶尾花 GL 呼叫 **fogvertex** 會設定會影響該模式的模式和參數。</span><span class="sxs-lookup"><span data-stu-id="3ce1a-115">The IRIS GL call, **fogvertex**, sets a mode and the parameters affecting that mode.</span></span> <span data-ttu-id="3ce1a-116">在 OpenGL 中，您可以呼叫 [**glFog**](glfog.md) 一次來設定模式，然後再次呼叫兩次以上來設定各種參數。</span><span class="sxs-lookup"><span data-stu-id="3ce1a-116">In OpenGL, you call [**glFog**](glfog.md) once to set the mode, and then again twice or more to set various parameters.</span></span>
-   <span data-ttu-id="3ce1a-117">在 OpenGL 中，深度提示並非個別的功能。</span><span class="sxs-lookup"><span data-stu-id="3ce1a-117">In OpenGL, depth cueing is not a separate feature.</span></span> <span data-ttu-id="3ce1a-118">使用線性霧而非深度提示。</span><span class="sxs-lookup"><span data-stu-id="3ce1a-118">Use linear fog instead of depth cueing.</span></span> <span data-ttu-id="3ce1a-119"> (本節提供如何執行這項操作的範例。 ) 下列鳶尾花 GL 函數沒有直接 OpenGL 對等專案：</span><span class="sxs-lookup"><span data-stu-id="3ce1a-119">(This section gives an example of how to do this.) The following IRIS GL functions have no direct OpenGL equivalent:</span></span>

    <span data-ttu-id="3ce1a-120">**depthcue**</span><span class="sxs-lookup"><span data-stu-id="3ce1a-120">**depthcue**</span></span>

    <span data-ttu-id="3ce1a-121">**lRGBrange**</span><span class="sxs-lookup"><span data-stu-id="3ce1a-121">**lRGBrange**</span></span>

    <span data-ttu-id="3ce1a-122">**lshaderange**</span><span class="sxs-lookup"><span data-stu-id="3ce1a-122">**lshaderange**</span></span>

    <span data-ttu-id="3ce1a-123">**getdcm**</span><span class="sxs-lookup"><span data-stu-id="3ce1a-123">**getdcm**</span></span>

-   <span data-ttu-id="3ce1a-124">若要調整霧化品質，請使用 [**glHint**](glhint.md) ( GL \_ 霧化 \_ 提示 ) 。</span><span class="sxs-lookup"><span data-stu-id="3ce1a-124">To adjust fog quality, use [**glHint**](glhint.md)( GL\_FOG\_HINT ).</span></span>

<span data-ttu-id="3ce1a-125">下表列出用來管理霧化的鳶尾花 GL 函數及其對等的 OpenGL 函數。</span><span class="sxs-lookup"><span data-stu-id="3ce1a-125">The following table lists the IRIS GL functions for managing fog and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="3ce1a-126">鳶尾花 GL 函數</span><span class="sxs-lookup"><span data-stu-id="3ce1a-126">IRIS GL function</span></span>         | <span data-ttu-id="3ce1a-127">OpenGL 函數</span><span class="sxs-lookup"><span data-stu-id="3ce1a-127">OpenGL function</span></span>                                     | <span data-ttu-id="3ce1a-128">意義</span><span class="sxs-lookup"><span data-stu-id="3ce1a-128">Meaning</span></span>                           |
|--------------------------|-----------------------------------------------------|-----------------------------------|
| <span data-ttu-id="3ce1a-129">**fogvertex**</span><span class="sxs-lookup"><span data-stu-id="3ce1a-129">**fogvertex**</span></span>            | [<span data-ttu-id="3ce1a-130">**glFog**</span><span class="sxs-lookup"><span data-stu-id="3ce1a-130">**glFog**</span></span>](glfog.md)                              | <span data-ttu-id="3ce1a-131">設定各種霧化參數。</span><span class="sxs-lookup"><span data-stu-id="3ce1a-131">Sets various fog parameters.</span></span>      |
| <span data-ttu-id="3ce1a-132"> \_ ) 上的 fogvertex ( FG</span><span class="sxs-lookup"><span data-stu-id="3ce1a-132">**fogvertex**( FG\_ON )</span></span>  | <span data-ttu-id="3ce1a-133">[**glEnable**](glenable.md) ( GL \_ 霧化 ) </span><span class="sxs-lookup"><span data-stu-id="3ce1a-133">[**glEnable**](glenable.md) ( GL\_FOG )</span></span>            | <span data-ttu-id="3ce1a-134">開啟霧化。</span><span class="sxs-lookup"><span data-stu-id="3ce1a-134">Turns on fog.</span></span>                     |
| <span data-ttu-id="3ce1a-135">**fogvertex** ( FG \_ OFF ) </span><span class="sxs-lookup"><span data-stu-id="3ce1a-135">**fogvertex**( FG\_OFF )</span></span> | <span data-ttu-id="3ce1a-136">[**glDisable**](gldisable.md) ( GL \_ 霧化 ) </span><span class="sxs-lookup"><span data-stu-id="3ce1a-136">[**glDisable**](gldisable.md) ( GL\_FOG )</span></span>          | <span data-ttu-id="3ce1a-137">關閉霧化。</span><span class="sxs-lookup"><span data-stu-id="3ce1a-137">Turns off fog.</span></span>                    |
| <span data-ttu-id="3ce1a-138">**depthcue**</span><span class="sxs-lookup"><span data-stu-id="3ce1a-138">**depthcue**</span></span>             | <span data-ttu-id="3ce1a-139">[**glFog**](glfog.md) ( gl \_ 霧化 \_ MOD，gl \_ 線性 ) </span><span class="sxs-lookup"><span data-stu-id="3ce1a-139">[**glFog**](glfog.md) ( GL\_FOG\_MOD, GL\_LINEAR )</span></span> | <span data-ttu-id="3ce1a-140">使用線性霧化進行深度提示。</span><span class="sxs-lookup"><span data-stu-id="3ce1a-140">Uses linear fog for depth cueing.</span></span> |



 

<span data-ttu-id="3ce1a-141">下表列出可傳遞至 **glFog** 的參數。</span><span class="sxs-lookup"><span data-stu-id="3ce1a-141">The following table lists the parameters you can pass to **glFog**.</span></span>



| <span data-ttu-id="3ce1a-142">霧化參數</span><span class="sxs-lookup"><span data-stu-id="3ce1a-142">Fog parameter</span></span>    | <span data-ttu-id="3ce1a-143">意義</span><span class="sxs-lookup"><span data-stu-id="3ce1a-143">Meaning</span></span>                       | <span data-ttu-id="3ce1a-144">預設</span><span class="sxs-lookup"><span data-stu-id="3ce1a-144">Default</span></span>                  |
|------------------|-------------------------------|--------------------------|
| <span data-ttu-id="3ce1a-145">GL \_ 霧化 \_ 密度</span><span class="sxs-lookup"><span data-stu-id="3ce1a-145">GL\_FOG\_DENSITY</span></span> | <span data-ttu-id="3ce1a-146">霧化密度。</span><span class="sxs-lookup"><span data-stu-id="3ce1a-146">Fog density.</span></span>                  | <span data-ttu-id="3ce1a-147">1.0</span><span class="sxs-lookup"><span data-stu-id="3ce1a-147">1.0</span></span>                      |
| <span data-ttu-id="3ce1a-148">GL \_ 霧化 \_ 開始</span><span class="sxs-lookup"><span data-stu-id="3ce1a-148">GL\_FOG\_START</span></span>   | <span data-ttu-id="3ce1a-149">線性模糊的近距離。</span><span class="sxs-lookup"><span data-stu-id="3ce1a-149">Near distance for linear fog.</span></span> | <span data-ttu-id="3ce1a-150">0.0</span><span class="sxs-lookup"><span data-stu-id="3ce1a-150">0.0</span></span>                      |
| <span data-ttu-id="3ce1a-151">GL \_ 霧化 \_ 結束</span><span class="sxs-lookup"><span data-stu-id="3ce1a-151">GL\_FOG\_END</span></span>     | <span data-ttu-id="3ce1a-152">線性模糊的遠距離。</span><span class="sxs-lookup"><span data-stu-id="3ce1a-152">Far distance for linear fog.</span></span>  | <span data-ttu-id="3ce1a-153">1.0</span><span class="sxs-lookup"><span data-stu-id="3ce1a-153">1.0</span></span>                      |
| <span data-ttu-id="3ce1a-154">GL \_ 霧化 \_ 索引</span><span class="sxs-lookup"><span data-stu-id="3ce1a-154">GL\_FOG\_INDEX</span></span>   | <span data-ttu-id="3ce1a-155">霧化色彩索引。</span><span class="sxs-lookup"><span data-stu-id="3ce1a-155">Fog color index.</span></span>              | <span data-ttu-id="3ce1a-156">0.0</span><span class="sxs-lookup"><span data-stu-id="3ce1a-156">0.0</span></span>                      |
| <span data-ttu-id="3ce1a-157">GL \_ 霧化 \_ 色彩</span><span class="sxs-lookup"><span data-stu-id="3ce1a-157">GL\_FOG\_COLOR</span></span>   | <span data-ttu-id="3ce1a-158">霧化 RGBA 色彩。</span><span class="sxs-lookup"><span data-stu-id="3ce1a-158">Fog RGBA color.</span></span>               | <span data-ttu-id="3ce1a-159"> (0、0、0、0) </span><span class="sxs-lookup"><span data-stu-id="3ce1a-159">(0, 0, 0, 0)</span></span>             |
| <span data-ttu-id="3ce1a-160">GL \_ 霧化 \_ 模式</span><span class="sxs-lookup"><span data-stu-id="3ce1a-160">GL\_FOG\_MODE</span></span>    | <span data-ttu-id="3ce1a-161">霧化模式。</span><span class="sxs-lookup"><span data-stu-id="3ce1a-161">Fog mode.</span></span>                     | <span data-ttu-id="3ce1a-162">請參閱下表。</span><span class="sxs-lookup"><span data-stu-id="3ce1a-162">See the following table.</span></span> |



 

<span data-ttu-id="3ce1a-163">OpenGL 的霧化密度參數與鳶尾花 GL 中的霧化密度參數不同。</span><span class="sxs-lookup"><span data-stu-id="3ce1a-163">The fog-density parameter of OpenGL differs from the one in IRIS GL.</span></span> <span data-ttu-id="3ce1a-164">它們的關聯如下：</span><span class="sxs-lookup"><span data-stu-id="3ce1a-164">They are related as follows:</span></span>

-   <span data-ttu-id="3ce1a-165">if *fogMode* = EXP2</span><span class="sxs-lookup"><span data-stu-id="3ce1a-165">if *fogMode* = EXP2</span></span>
     

    <span data-ttu-id="3ce1a-166">*openGLfogDensity* = (*irisGLfogDensity* )  ( **sqrt** ( **記錄** ( 1/255 ) ) ) </span><span class="sxs-lookup"><span data-stu-id="3ce1a-166">*openGLfogDensity* = (*irisGLfogDensity* ) ( **sqrt** ( **log** ( 1 / 255 ) ))</span></span>
-   <span data-ttu-id="3ce1a-167">如果 *fogMode* = EXP</span><span class="sxs-lookup"><span data-stu-id="3ce1a-167">if *fogMode* = EXP</span></span>
     

    <span data-ttu-id="3ce1a-168">*openGLfogDensity* = (*irisGLfogDensity* )  ( **記錄** ( 1/255 ) ) </span><span class="sxs-lookup"><span data-stu-id="3ce1a-168">*openGLfogDensity* = (*irisGLfogDensity* ) ( **log** ( 1 / 255 ) )</span></span>

<span data-ttu-id="3ce1a-169">其中 **sqrt** 是平方根運算， **log** 是自然對數、 *irisGLfogDensity* 是鳶尾花 GL 霧密度，而 *openGLfogDensity* 是 OpenGL 霧化密度。</span><span class="sxs-lookup"><span data-stu-id="3ce1a-169">where **sqrt** is the square root operation, **log** is the natural logarithm, *irisGLfogDensity* is the IRIS GL fog density, and *openGLfogDensity* is the OpenGL fog density.</span></span>

<span data-ttu-id="3ce1a-170">若要在計算每圖元模式和每個頂點模式的霧化之間切換，請使用 [**glHint**](glhint.md) ( GL \_ 霧化 \_ 提示， *hintMode*) 。</span><span class="sxs-lookup"><span data-stu-id="3ce1a-170">To switch between calculating fog in per-pixel mode and per-vertex mode, use [**glHint**](glhint.md)( GL\_FOG\_HINT, *hintMode*).</span></span> <span data-ttu-id="3ce1a-171">有兩個提示模式可用：</span><span class="sxs-lookup"><span data-stu-id="3ce1a-171">Two hint modes are available:</span></span>

-   <span data-ttu-id="3ce1a-172">GL \_ 最好每圖元霧化計算</span><span class="sxs-lookup"><span data-stu-id="3ce1a-172">GL\_NICEST per-pixel fog calculation</span></span>
-   <span data-ttu-id="3ce1a-173">GL \_ 每個頂點的最快速霧化計算</span><span class="sxs-lookup"><span data-stu-id="3ce1a-173">GL\_FASTEST per-vertex fog calculation</span></span>

<span data-ttu-id="3ce1a-174">下表列出鳶尾花 GL 霧化模式及其 OpenGL 對等專案。</span><span class="sxs-lookup"><span data-stu-id="3ce1a-174">The following table lists the IRIS GL fog modes and their OpenGL equivalents.</span></span>



| <span data-ttu-id="3ce1a-175">鳶尾花 GL 霧化模式</span><span class="sxs-lookup"><span data-stu-id="3ce1a-175">IRIS GL fog mode</span></span>                       | <span data-ttu-id="3ce1a-176">OpenGL 霧化模式</span><span class="sxs-lookup"><span data-stu-id="3ce1a-176">OpenGL fog mode</span></span> | <span data-ttu-id="3ce1a-177">提示模式</span><span class="sxs-lookup"><span data-stu-id="3ce1a-177">Hint mode</span></span>                         | <span data-ttu-id="3ce1a-178">意義</span><span class="sxs-lookup"><span data-stu-id="3ce1a-178">Meaning</span></span>                                  |
|----------------------------------------|-----------------|-----------------------------------|------------------------------------------|
| <span data-ttu-id="3ce1a-179">FG \_ ANALYSTS.VTX \_ EXP、FG \_ PIX \_ EXP</span><span class="sxs-lookup"><span data-stu-id="3ce1a-179">FG\_VTX\_EXP,FG\_PIX\_EXP</span></span><br/>   | <span data-ttu-id="3ce1a-180">GL \_ EXP</span><span class="sxs-lookup"><span data-stu-id="3ce1a-180">GL\_EXP</span></span>         | <span data-ttu-id="3ce1a-181">GL \_ 最快、GL \_ 最好</span><span class="sxs-lookup"><span data-stu-id="3ce1a-181">GL\_FASTEST,GL\_NICEST</span></span><br/> | <span data-ttu-id="3ce1a-182">繁重的霧化模式 (預設) 。</span><span class="sxs-lookup"><span data-stu-id="3ce1a-182">Heavy fog mode (default).</span></span>                |
| <span data-ttu-id="3ce1a-183">FG \_ Analysts.vtx \_ EXP2、FG \_ PIX \_ EXP2</span><span class="sxs-lookup"><span data-stu-id="3ce1a-183">FG\_VTX\_EXP2,FG\_PIX\_EXP2</span></span><br/> | <span data-ttu-id="3ce1a-184">GL \_ EXP2</span><span class="sxs-lookup"><span data-stu-id="3ce1a-184">GL\_EXP2</span></span>        | <span data-ttu-id="3ce1a-185">GL \_ 最快、GL \_ 最好</span><span class="sxs-lookup"><span data-stu-id="3ce1a-185">GL\_FASTEST,GL\_NICEST</span></span><br/> | <span data-ttu-id="3ce1a-186">迷霧模式。</span><span class="sxs-lookup"><span data-stu-id="3ce1a-186">Haze mode.</span></span>                               |
| <span data-ttu-id="3ce1a-187">FG \_ ANALYSTS.VTX \_ LIN、FG \_ PIX \_ LIN</span><span class="sxs-lookup"><span data-stu-id="3ce1a-187">FG\_VTX\_LIN,FG\_PIX\_LIN</span></span><br/>   | <span data-ttu-id="3ce1a-188">GL \_ 線性</span><span class="sxs-lookup"><span data-stu-id="3ce1a-188">GL\_LINEAR</span></span>      | <span data-ttu-id="3ce1a-189">GL \_ 最快、GL \_ 最好</span><span class="sxs-lookup"><span data-stu-id="3ce1a-189">GL\_FASTEST,GL\_NICEST</span></span><br/> | <span data-ttu-id="3ce1a-190">線性霧化模式。</span><span class="sxs-lookup"><span data-stu-id="3ce1a-190">Linear fog mode.</span></span> <span data-ttu-id="3ce1a-191"> (用於深度提示。 ) </span><span class="sxs-lookup"><span data-stu-id="3ce1a-191">(Use for depth cueing.)</span></span> |



 

<span data-ttu-id="3ce1a-192">下列程式碼範例示範 OpenGL 中的深度提示：</span><span class="sxs-lookup"><span data-stu-id="3ce1a-192">The following code example demonstrates depth cueing in OpenGL:</span></span>


```C++
/* 
 *  depthcue.c 
 *  This program draws a wire frame model, which uses 
 *  intensity (brightness) to give clues to distance 
 *  Fog is used to achieve this effect 
 */ 
#include <GL/gl.h> 
#include <GL/glu.h> 
#include "aux.h" 
 
/*  Initialize linear fog for depth cueing 
 */ 
void myinit(void) 
{ 
    GLfloat fogColor[4] = {0.0, 0.0, 0.0, 1.0}; 
 
    glEnable(GL_FOG); 
    glFogi (GL_FOG_MODE, GL_LINEAR); 
    glHint (GL_FOG_HINT, GL_NICEST);  /*  per pixel  */ 
    glFogf (GL_FOG_START, 3.0); 
    glFogf (GL_FOG_END, 5.0); 
    glFogfv (GL_FOG_COLOR, fogColor); 
    glClearColor(0.0, 0.0, 0.0, 1.0); 
 
    glDepthFunc(GL_LEQUAL); 
    glEnable(GL_DEPTH_TEST); 
    glShadeModel(GL_FLAT); 
} 
 
/*  display() draws an icosahedron 
 */ 
void display(void) 
{ 
    glClear(GL_COLOR_BUFFER_BIT | GL_DEPTH_BUFFER_BIT); 
    glColor3f (1.0, 1.0, 1.0); 
    auxWireIcosahedron(1.0); 
    glFlush(); 
} 
 
void myReshape(GLsizei w, GLsizei h) 
{ 
    glViewport(0, 0, w, h); 
    glMatrixMode(GL_PROJECTION); 
    glLoadIdentity(); 
    gluPerspective (45.0, (GLfloat) w/(GLfloat) h, 3.0, 5.0); 
    glMatrixMode(GL_MODELVIEW); 
    glLoadIdentity (); 
    glTranslatef (0.0, 0.0, -4.0); /*move object into view*/ 
} 
/*  Main Loop 
 */ 
int main(int argc, char** argv) 
{ 
    auxInitDisplayMode (AUX_SINGLE | AUX_RGBA | AUX_DEPTH); 
    auxInitPosition (0, 0, 400, 400); 
    auxInitWindow (argv[0]); 
    myinit(); 
    auxReshapeFunc (myReshape); 
    auxMainLoop(display); 
}
```



 

 





