---
title: 移植轉譯內容
description: 移植轉譯內容
ms.assetid: 8655a81b-9f13-4ee5-ba0d-9aa9da1bfd09
keywords:
- 轉譯內容 OpenGL、移植
- Windows 上的 OpenGL，轉譯內容
- 移植至 OpenGL，轉譯內容
- OpenGL 移植，轉譯內容
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43e72839d04838b3173d772fbbf29a903a295cfd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372362"
---
# <a name="porting-rendering-contexts"></a><span data-ttu-id="a402c-107">移植轉譯內容</span><span class="sxs-lookup"><span data-stu-id="a402c-107">Porting Rendering Contexts</span></span>

<span data-ttu-id="a402c-108">X 視窗系統和 Windows 會透過轉譯內容呈現。</span><span class="sxs-lookup"><span data-stu-id="a402c-108">The X Window System and Windows render through rendering contexts.</span></span> <span data-ttu-id="a402c-109">六個 GLX 函式會管理轉譯內容，其中有五個都有對等的 Windows 函數。</span><span class="sxs-lookup"><span data-stu-id="a402c-109">Six GLX functions manage rendering contexts and five of them have an equivalent Windows function.</span></span>

<span data-ttu-id="a402c-110">下表列出 GLX 轉譯函數及其對等的 Windows 函數。</span><span class="sxs-lookup"><span data-stu-id="a402c-110">The following table lists the GLX rendering functions and their equivalent Windows functions.</span></span>



| <span data-ttu-id="a402c-111">GLX 轉譯內容函式</span><span class="sxs-lookup"><span data-stu-id="a402c-111">GLX rendering context function</span></span>                                                                            | <span data-ttu-id="a402c-112">Windows 轉譯內容函式</span><span class="sxs-lookup"><span data-stu-id="a402c-112">Windows rendering context function</span></span>                                      |
|-----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="a402c-113">GLXCoNtext **glXCopyCoNtext** ( 顯示 *\* dpy*、GLXCoNtext *src*、GLXCoNtext *dst*、GLuint *mask*) </span><span class="sxs-lookup"><span data-stu-id="a402c-113">GLXContext **glXCopyContext**( Display *\*dpy*,GLXContext *src*,GLXContext *dst*,GLuint *mask*)</span></span>            | <span data-ttu-id="a402c-114">不適用。</span><span class="sxs-lookup"><span data-stu-id="a402c-114">Not applicable.</span></span>                                                         |
| <span data-ttu-id="a402c-115">GLXCoNtext **glXCreateCoNtext** ( 顯示 *\* dpy*、XVisualInfo *\* vis*、GLXCoNtext *shareList*、Bool *direct*) </span><span class="sxs-lookup"><span data-stu-id="a402c-115">GLXContext **glXCreateContext**( Display *\*dpy*,XVisualInfo *\*vis*,GLXContext *shareList*,Bool *direct*)</span></span> | <span data-ttu-id="a402c-116">HGLRC [**wglCreateCoNtext**](/windows/desktop/api/wingdi/nf-wingdi-wglcreatecontext) ( HDC *hdc*) </span><span class="sxs-lookup"><span data-stu-id="a402c-116">HGLRC [**wglCreateContext**](/windows/desktop/api/wingdi/nf-wingdi-wglcreatecontext)( HDC *hdc*)</span></span>          |
| <span data-ttu-id="a402c-117">void **glXDeleteCoNtext** ( 顯示 *\* dpy*、GLXCoNtext *ctx*) </span><span class="sxs-lookup"><span data-stu-id="a402c-117">void **glXDeleteContext**( Display *\*dpy*,GLXContext *ctx*)</span></span>                                              | <span data-ttu-id="a402c-118">BOOL [**wglDeleteCoNtext**](/windows/desktop/api/wingdi/nf-wingdi-wgldeletecontext) ( HGLRC *HGLRC*) </span><span class="sxs-lookup"><span data-stu-id="a402c-118">BOOL [**wglDeleteContext**](/windows/desktop/api/wingdi/nf-wingdi-wgldeletecontext)( HGLRC *hglrc*)</span></span>       |
| <span data-ttu-id="a402c-119">GLXCoNtext **glXGetCurrentCoNtext** (*void*) </span><span class="sxs-lookup"><span data-stu-id="a402c-119">GLXContext **glXGetCurrentContext**(*void*)</span></span>                                                               | <span data-ttu-id="a402c-120">HGLRC [**wglGetCurrentCoNtext**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentcontext) (*VOID*) </span><span class="sxs-lookup"><span data-stu-id="a402c-120">HGLRC [**wglGetCurrentContext**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentcontext)(*VOID*)</span></span>      |
| <span data-ttu-id="a402c-121">GLXDrawable **glXGetCurrentDrawable** (*void*) </span><span class="sxs-lookup"><span data-stu-id="a402c-121">GLXDrawable **glXGetCurrentDrawable**(*void*)</span></span>                                                             | <span data-ttu-id="a402c-122">HDC [**wglGetCurrentDC**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentdc) (*VOID*) </span><span class="sxs-lookup"><span data-stu-id="a402c-122">HDC [**wglGetCurrentDC**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentdc)(*VOID*)</span></span>                  |
| <span data-ttu-id="a402c-123">Bool **glXMakeCurrent** ( 顯示 *\* dpy*、GLXDrawable *draw*、GLXCoNtext *ctx*) </span><span class="sxs-lookup"><span data-stu-id="a402c-123">Bool **glXMakeCurrent**( Display *\*dpy*,GLXDrawable *draw*,GLXContext *ctx*)</span></span>                              | <span data-ttu-id="a402c-124">BOOL [**wglMakeCurrent**](/windows/desktop/api/wingdi/nf-wingdi-wglmakecurrent) ( HDC *hdc*，HGLRC *HGLRC*) </span><span class="sxs-lookup"><span data-stu-id="a402c-124">BOOL [**wglMakeCurrent**](/windows/desktop/api/wingdi/nf-wingdi-wglmakecurrent)( HDC *hdc*,HGLRC *hglrc*)</span></span> |



 

<span data-ttu-id="a402c-125">傳回型別和其他類型在 X 視窗系統中的名稱與 Windows 中的名稱不同。</span><span class="sxs-lookup"><span data-stu-id="a402c-125">Return types and other types have different names in the X Window System than in Windows.</span></span> <span data-ttu-id="a402c-126">您可以搜尋 GLXCoNtext 的出現位置，以協助找出需要移植的程式碼部分。</span><span class="sxs-lookup"><span data-stu-id="a402c-126">You can search for occurrences of GLXContext to help find parts of your code that need to be ported.</span></span>

<span data-ttu-id="a402c-127">下列各節比較 X 視窗系統程式中的轉譯內容程式碼範例，以及將程式碼移植到 Windows 之後的相同程式碼。</span><span class="sxs-lookup"><span data-stu-id="a402c-127">The following sections compare rendering context code samples in an X Window System program and the same code after it has been ported to Windows.</span></span>

<span data-ttu-id="a402c-128">如需呈現內容的詳細資訊， [請參閱轉譯](rendering-contexts.md)內容。</span><span class="sxs-lookup"><span data-stu-id="a402c-128">For more information on rendering contexts, see [Rendering Contexts](rendering-contexts.md).</span></span>

 

 




