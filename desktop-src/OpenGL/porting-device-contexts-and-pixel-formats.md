---
title: 移植裝置內容和像素格式
description: 移植裝置內容和像素格式
ms.assetid: b60cac27-1e2e-4da5-81c4-69446b92f820
keywords:
- 移植至 OpenGL，圖元
- OpenGL 移植，圖元
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d793c139c6d7a0a0fc85b2e2c36f30176ce9ab6e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106969842"
---
# <a name="porting-device-contexts-and-pixel-formats"></a><span data-ttu-id="e27b7-105">移植裝置內容和像素格式</span><span class="sxs-lookup"><span data-stu-id="e27b7-105">Porting Device Contexts and Pixel Formats</span></span>

<span data-ttu-id="e27b7-106">Microsoft 適用于 Windows 之 OpenGL 的每個視窗都有自己目前的像素格式。</span><span class="sxs-lookup"><span data-stu-id="e27b7-106">Each window in the Microsoft implementation of OpenGL for Windows has its own current pixel format.</span></span> <span data-ttu-id="e27b7-107">像素格式是由 [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) 資料結構所定義。</span><span class="sxs-lookup"><span data-stu-id="e27b7-107">A pixel format is defined by a [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) data structure.</span></span> <span data-ttu-id="e27b7-108">因為每個視窗都有自己的像素格式，所以您會取得裝置內容、設定裝置內容的像素格式，然後建立裝置內容的 OpenGL 轉譯內容。</span><span class="sxs-lookup"><span data-stu-id="e27b7-108">Because each window has its own pixel format, you obtain a device context, set the pixel format of the device context, and then create an OpenGL rendering context for the device context.</span></span> <span data-ttu-id="e27b7-109">轉譯內容會自動使用其裝置內容的像素格式。</span><span class="sxs-lookup"><span data-stu-id="e27b7-109">The rendering context automatically uses the pixel format of its device context.</span></span>

<span data-ttu-id="e27b7-110">X 視窗系統也會使用資料結構 **XVisualInfo**，在視窗中指定圖元的屬性。</span><span class="sxs-lookup"><span data-stu-id="e27b7-110">The X Window System also uses a data structure, **XVisualInfo**, to specify the properties of pixels in a window.</span></span> <span data-ttu-id="e27b7-111">**XVisualInfo** 結構包含 **視覺化** 資料結構，描述如何在特定螢幕中使用色彩資源。</span><span class="sxs-lookup"><span data-stu-id="e27b7-111">**XVisualInfo** structures contain a **Visual** data structure that describes how color resources are used in a specific screen.</span></span>

<span data-ttu-id="e27b7-112">在 X 視窗系統中， **XVisualInfo** 是用來建立視窗，方法是將視窗設定為您想要的像素格式。</span><span class="sxs-lookup"><span data-stu-id="e27b7-112">In the X Window System, **XVisualInfo** is used to create a window by setting the window to the pixel format you want.</span></span> <span data-ttu-id="e27b7-113">傳回的結構會用來建立視窗和轉譯內容。</span><span class="sxs-lookup"><span data-stu-id="e27b7-113">The returned structure is used to create the window and a rendering context.</span></span> <span data-ttu-id="e27b7-114">在 Windows 中，您會先建立一個視窗，並取得視窗的控制碼 (HDC) 。</span><span class="sxs-lookup"><span data-stu-id="e27b7-114">In Windows, you first create a window and get a handle to a device context (HDC) of the window.</span></span> <span data-ttu-id="e27b7-115">然後，會使用 HDC 來設定視窗的像素格式。</span><span class="sxs-lookup"><span data-stu-id="e27b7-115">The HDC is then used to set the pixel format for the window.</span></span> <span data-ttu-id="e27b7-116">轉譯內容會使用視窗的像素格式。</span><span class="sxs-lookup"><span data-stu-id="e27b7-116">The rendering context uses the pixel format of the window.</span></span>

<span data-ttu-id="e27b7-117">下表比較 X 視窗系統和 GLX 視覺化函式與其對等的 Windows 像素格式函數。</span><span class="sxs-lookup"><span data-stu-id="e27b7-117">The following table compares the X Window System and GLX visual functions with their equivalent Windows pixel format functions.</span></span>



| <span data-ttu-id="e27b7-118">X 視窗/GLX 視覺化函式</span><span class="sxs-lookup"><span data-stu-id="e27b7-118">X window/GLX visual function</span></span>                                                                                     | <span data-ttu-id="e27b7-119">Windows 像素格式函數</span><span class="sxs-lookup"><span data-stu-id="e27b7-119">Windows pixel format function</span></span>                                                                                                      |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e27b7-120">XVisualInfo \* **GlXChooseVisual** ( 顯示 *\* dpy*、int *screen*、int *\* attribList*) </span><span class="sxs-lookup"><span data-stu-id="e27b7-120">XVisualInfo\***glXChooseVisual**( Display *\*dpy*,int *screen*,int *\*attribList*)</span></span>                               | <span data-ttu-id="e27b7-121">int [**ChoosePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat) ( HDC *hdc*，PIXELFORMATDESCRIPTOR *\* ppfd*) </span><span class="sxs-lookup"><span data-stu-id="e27b7-121">int [**ChoosePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat)( HDC *hdc*,PIXELFORMATDESCRIPTOR *\*ppfd*)</span></span>                                      |
| <span data-ttu-id="e27b7-122">int **glXGetConfig** ( 顯示 *\* dpy*、XVisualInfo *\* vis*、int *\* attribList*、int *\* 值*) </span><span class="sxs-lookup"><span data-stu-id="e27b7-122">int **glXGetConfig**( Display *\*dpy*,XVisualInfo *\*vis*,int *\*attribList*,int *\*value*)</span></span>                      | <span data-ttu-id="e27b7-123">int [**DescribePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-describepixelformat) ( HDC *Hdc*、Int *iPixelFormat*、UINT *n*、LPPIXELFORMATDESCRIPTOR *ppfd*) </span><span class="sxs-lookup"><span data-stu-id="e27b7-123">int [**DescribePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-describepixelformat)( HDC *hdc*,int *iPixelFormat*,UINT *nBytes*,LPPIXELFORMATDESCRIPTOR *ppfd*)</span></span> |
| <span data-ttu-id="e27b7-124">XVisualInfo \* **XGetVisualInfo** ( 顯示 *\* dpy*、long *vinfo \_ mask*、XVisualInfo *\* vinfo \_ templ*、int *\* nitems*) </span><span class="sxs-lookup"><span data-stu-id="e27b7-124">XVisualInfo\***XGetVisualInfo**( Display *\*dpy*,long *vinfo\_mask*,XVisualInfo *\*vinfo\_templ*,int *\*nitems*)</span></span> | <span data-ttu-id="e27b7-125">int [**GetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-getpixelformat) ( HDC *hdc*) </span><span class="sxs-lookup"><span data-stu-id="e27b7-125">int [**GetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-getpixelformat)( HDC *hdc*)</span></span>                                                                           |
| <span data-ttu-id="e27b7-126">建立視窗時，會使用 **glxChooseVisual** 所傳回的 *視覺效果*。</span><span class="sxs-lookup"><span data-stu-id="e27b7-126">The *visual* returned by **glxChooseVisual** is used when a window is created.</span></span>                                   | <span data-ttu-id="e27b7-127">BOOL [**SetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-setpixelformat) ( HDC *Hdc*、int *iPixelFormat*、PIXELFORMATDESCRIPTOR *\* ppfd*) </span><span class="sxs-lookup"><span data-stu-id="e27b7-127">BOOL [**SetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-setpixelformat)( HDC *hdc*,int *iPixelFormat*,PIXELFORMATDESCRIPTOR *\*ppfd*)</span></span>                        |



 

<span data-ttu-id="e27b7-128">下列各節提供 X 視窗系統程式的像素格式程式碼片段範例，以及將程式碼移植到 Windows 之後的相同程式碼。</span><span class="sxs-lookup"><span data-stu-id="e27b7-128">The following sections give examples of pixel format code fragments for an X Window System program, and the same code after it has been ported to Windows.</span></span>

-   [<span data-ttu-id="e27b7-129">GLX 像素格式的程式碼範例</span><span class="sxs-lookup"><span data-stu-id="e27b7-129">GLX Pixel Format Code Sample</span></span>](glx-pixel-format-code-sample.md)
-   [<span data-ttu-id="e27b7-130">Windows 像素格式的程式碼範例</span><span class="sxs-lookup"><span data-stu-id="e27b7-130">Windows Pixel Format Code Sample</span></span>](win32-pixel-format-code-sample.md)

<span data-ttu-id="e27b7-131">如需像素格式的詳細資訊，請參閱 [像素格式](pixel-formats.md)。</span><span class="sxs-lookup"><span data-stu-id="e27b7-131">For more information on pixel formats, see [Pixel Formats](pixel-formats.md).</span></span>

 

 




