---
title: 移植網底模型
description: OpenGL 與鳶尾花 GL 一樣，可讓您在平滑 (Gouraud) 陰影和平坦陰影之間切換。 下表列出鳶尾花 GL 陰影和遞色函式，以及其對等的 OpenGL 函數。
ms.assetid: 93e8f437-381f-4620-ad6f-52ce830d99b6
keywords:
- 鳶尾花 GL 移植，網底
- 從鳶尾花 GL 進行移植，網底
- 從鳶尾花 GL 移植至 OpenGL，網底
- 從鳶尾花 GL 的 OpenGL 移植，網底
- 平滑陰影
- Gouraud 網底
- 平面網底
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 124bb002f6f133b4d47dd40e1a0e8738c512ce99
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301380"
---
# <a name="porting-shading-models"></a><span data-ttu-id="adf03-111">移植網底模型</span><span class="sxs-lookup"><span data-stu-id="adf03-111">Porting Shading Models</span></span>

<span data-ttu-id="adf03-112">OpenGL 與鳶尾花 GL 一樣，可讓您在平滑 (Gouraud) 陰影和平坦陰影之間切換。</span><span class="sxs-lookup"><span data-stu-id="adf03-112">Like IRIS GL, OpenGL lets you switch between smooth (Gouraud) shading and flat shading.</span></span> <span data-ttu-id="adf03-113">下表列出鳶尾花 GL 陰影和遞色函式，以及其對等的 OpenGL 函數。</span><span class="sxs-lookup"><span data-stu-id="adf03-113">The following table lists the IRIS GL shading and dithering functions and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="adf03-114">鳶尾花 GL 函數</span><span class="sxs-lookup"><span data-stu-id="adf03-114">IRIS GL function</span></span>                                   | <span data-ttu-id="adf03-115">OpenGL 函數</span><span class="sxs-lookup"><span data-stu-id="adf03-115">OpenGL function</span></span>                                                                                    | <span data-ttu-id="adf03-116">意義</span><span class="sxs-lookup"><span data-stu-id="adf03-116">Meaning</span></span>                      |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------|------------------------------|
| <span data-ttu-id="adf03-117">**shademodel** (一般) </span><span class="sxs-lookup"><span data-stu-id="adf03-117">**shademodel**(FLAT)</span></span>                               | <span data-ttu-id="adf03-118">[**glShadeModel**](glshademodel.md) ( GL 一般 \_ ) </span><span class="sxs-lookup"><span data-stu-id="adf03-118">[**glShadeModel**](glshademodel.md) ( GL\_FLAT )</span></span>                                                  | <span data-ttu-id="adf03-119">會進行平面陰影。</span><span class="sxs-lookup"><span data-stu-id="adf03-119">Does flat shading.</span></span>           |
| <span data-ttu-id="adf03-120">**shademodel** (GOURAUD) </span><span class="sxs-lookup"><span data-stu-id="adf03-120">**shademodel**(GOURAUD)</span></span>                            | <span data-ttu-id="adf03-121">**glShadeModel** ( GL \_ 平滑 ) </span><span class="sxs-lookup"><span data-stu-id="adf03-121">**glShadeModel**( GL\_SMOOTH )</span></span>                                                                     | <span data-ttu-id="adf03-122">會順暢地陰影。</span><span class="sxs-lookup"><span data-stu-id="adf03-122">Does smooth shading.</span></span>         |
| <span data-ttu-id="adf03-123">**getsm**</span><span class="sxs-lookup"><span data-stu-id="adf03-123">**getsm**</span></span>                                          | <span data-ttu-id="adf03-124">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( GL \_ 網底 \_ 模型 ) </span><span class="sxs-lookup"><span data-stu-id="adf03-124">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( GL\_SHADE\_MODEL )</span></span>      | <span data-ttu-id="adf03-125">傳回目前的陰影模型。</span><span class="sxs-lookup"><span data-stu-id="adf03-125">Returns current shade model.</span></span> |
| <span data-ttu-id="adf03-126"> \_) **遞色** 上的遞色 (dt (DT \_ 關閉) </span><span class="sxs-lookup"><span data-stu-id="adf03-126">**dither**(DT\_ON) **dither**(DT\_OFF)</span></span> <br/> | <span data-ttu-id="adf03-127">[**glEnable**](glenable.md) ( gl \_ 遞色 ) [**glDisable**](gldisable.md) ( gl \_ 遞色 ) </span><span class="sxs-lookup"><span data-stu-id="adf03-127">[**glEnable**](glenable.md) ( GL\_DITHER )[**glDisable**](gldisable.md)( GL\_DITHER )</span></span><br/> | <span data-ttu-id="adf03-128">開啟/關閉遞色。</span><span class="sxs-lookup"><span data-stu-id="adf03-128">Turns dithering on/off.</span></span>      |



 

<span data-ttu-id="adf03-129">??</span><span class="sxs-lookup"><span data-stu-id="adf03-129">??</span></span>

 

 





