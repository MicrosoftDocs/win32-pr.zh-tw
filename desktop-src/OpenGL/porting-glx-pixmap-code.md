---
title: 移植 GLX Pixmap 程式碼
description: 移植 GLX Pixmap 程式碼
ms.assetid: 5b87d26d-b3ea-4f90-9456-d3f7da462948
keywords:
- pixmaps
- Windows 上的 OpenGL、pixmaps
- 移植至 OpenGL、pixmaps
- OpenGL 移植，pixmaps
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed0dbd7f94736f25346a9136d60feb4fa1bb6c68
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104024015"
---
# <a name="porting-glx-pixmap-code"></a><span data-ttu-id="6e0af-107">移植 GLX Pixmap 程式碼</span><span class="sxs-lookup"><span data-stu-id="6e0af-107">Porting GLX Pixmap Code</span></span>

<span data-ttu-id="6e0af-108">X 視窗系統使用 *pixmaps*，這是以三維位陣列形式呈現的非螢幕虛擬繪圖表面。</span><span class="sxs-lookup"><span data-stu-id="6e0af-108">The X Window System uses *pixmaps*, which are off-screen virtual drawing surfaces in the form of a three-dimensional array of bits.</span></span> <span data-ttu-id="6e0af-109">您可以將 pixmap 視為一堆點陣圖：二維陣列，其中每個圖元的值都是從0到2N1，其中 N 是 pixmap 的深度。</span><span class="sxs-lookup"><span data-stu-id="6e0af-109">You can think of a pixmap as a stack of bitmaps: a two-dimensional array of pixels with each pixel having a value from 0 to 2N1 where N is the depth of the pixmap.</span></span>

<span data-ttu-id="6e0af-110">針對 OpenGL 程式，您可以使用 GLX 函式（ **glXCreateGLXPixmap** 和 **glXDestroyGLXPixmap**）來建立和終結用於關閉螢幕轉譯的 GLX pixmaps。</span><span class="sxs-lookup"><span data-stu-id="6e0af-110">For OpenGL programs you use the GLX functions, **glXCreateGLXPixmap** and **glXDestroyGLXPixmap**, to create and destroy GLX pixmaps used for off-screen rendering.</span></span>

<span data-ttu-id="6e0af-111">Windows 使用與裝置無關的點陣圖，其提供與 X 視窗系統 pixmaps 相同的功能。</span><span class="sxs-lookup"><span data-stu-id="6e0af-111">Windows uses device-independent bitmaps that serve the same function as X Window System pixmaps.</span></span> <span data-ttu-id="6e0af-112">使用標準的 Windows 點陣圖函式來建立和終結點陣圖。</span><span class="sxs-lookup"><span data-stu-id="6e0af-112">Use the standard Windows bitmap functions to create and destroy bitmaps.</span></span>

<span data-ttu-id="6e0af-113">下表列出 GLX pixmap 函數及其對等的 Windows 點陣圖函數。</span><span class="sxs-lookup"><span data-stu-id="6e0af-113">The following table lists the GLX pixmap functions and their equivalent Windows bitmap functions.</span></span>



| <span data-ttu-id="6e0af-114">GLX pixmap 和 font-family 函數</span><span class="sxs-lookup"><span data-stu-id="6e0af-114">GLX pixmap and font function</span></span>                                                          | <span data-ttu-id="6e0af-115">Windows 點陣圖和字型函數</span><span class="sxs-lookup"><span data-stu-id="6e0af-115">Windows bitmap and font function</span></span>                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e0af-116">GLXPixmap **glXCreateGLXPixmap** ( Display *\* dpy*，XVisualInfo *\* vis*，Pixmap *Pixmap*) </span><span class="sxs-lookup"><span data-stu-id="6e0af-116">GLXPixmap **glXCreateGLXPixmap**( Display *\*dpy*,XVisualInfo *\*vis*,Pixmap *pixmap*)</span></span> | <span data-ttu-id="6e0af-117">HBITMAP [CreateDIBitmap](/windows/desktop/api/wingdi/nf-wingdi-createdibitmap) hdc *hdc*、LPBITMAPINFOHEADER *lpbmih*、DWORD *fdwInit*、CONST BYTE *\* lpbInit*、LPBITMAPINFO *lpbmi*、UINT \* fuUsage \***)** HBITMAP [CreateDIBSection](/windows/desktop/api/wingdi/nf-wingdi-createdibsection) hdc *hdc*、LPBITMAPINFO *lpbmi*、dword *fInit*、dword *iUsage*) </span><span class="sxs-lookup"><span data-stu-id="6e0af-117">HBITMAP [CreateDIBitmap](/windows/desktop/api/wingdi/nf-wingdi-createdibitmap) HDC *hdc*,LPBITMAPINFOHEADER *lpbmih*,DWORD *fdwInit*,CONST BYTE *\*lpbInit*,LPBITMAPINFO *lpbmi*,UINT *fuUsage\*\*\*)*\* HBITMAP [CreateDIBSection](/windows/desktop/api/wingdi/nf-wingdi-createdibsection) HDC *hdc*,LPBITMAPINFO *lpbmi*,DWORD *fInit*,DWORD *iUsage*)</span></span><br/> |
| <span data-ttu-id="6e0af-118">void **glXDestroyGLXPixmap** ( 顯示 *\* dpy*、GLXPixmap *pix*) </span><span class="sxs-lookup"><span data-stu-id="6e0af-118">void **glXDestroyGLXPixmap**( Display *\*dpy*,GLXPixmap *pix*)</span></span>                        | <span data-ttu-id="6e0af-119">BOOL [DeleteObject](/windows/desktop/api/wingdi/nf-wingdi-deleteobject) ( HGDIOBJ *hObject*) </span><span class="sxs-lookup"><span data-stu-id="6e0af-119">BOOL [DeleteObject](/windows/desktop/api/wingdi/nf-wingdi-deleteobject)( HGDIOBJ *hObject*)</span></span>                                                                                                                                                                                                                                  |



 

 

