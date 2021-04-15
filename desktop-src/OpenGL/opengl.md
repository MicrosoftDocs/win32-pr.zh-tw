---
title: Opengl
description: OpenGL 是圖形硬體的軟體介面，可將多維度物件轉譯成畫面格緩衝區。
ms.assetid: ddd7c8d0-f1d1-4d16-bd0c-99cee3d733c5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02bec69473f937d4dfff9c496d291e8070ffadef
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463609"
---
# <a name="opengl"></a><span data-ttu-id="591a8-103">Opengl</span><span class="sxs-lookup"><span data-stu-id="591a8-103">OpenGL</span></span>

## <a name="purpose"></a><span data-ttu-id="591a8-104">目的</span><span class="sxs-lookup"><span data-stu-id="591a8-104">Purpose</span></span>

<span data-ttu-id="591a8-105">OpenGL 是圖形硬體的軟體介面，可將多維度物件轉譯成畫面格緩衝區。</span><span class="sxs-lookup"><span data-stu-id="591a8-105">As a software interface for graphics hardware, OpenGL renders multidimensional objects into a framebuffer.</span></span> <span data-ttu-id="591a8-106">Microsoft 針對 Windows 作業系統執行 OpenGL 是業界標準的圖形軟體，程式設計人員可以用它來建立高品質的靜止和動畫三維色彩影像。</span><span class="sxs-lookup"><span data-stu-id="591a8-106">The Microsoft implementation of OpenGL for the Windows operating system is industry-standard graphics software with which programmers can create high-quality still and animated three-dimensional color images.</span></span> <span data-ttu-id="591a8-107">本節所述的 OpenGL 版本為1.1。</span><span class="sxs-lookup"><span data-stu-id="591a8-107">The version of OpenGL described in this section is 1.1.</span></span>

<span data-ttu-id="591a8-108">如需在 Windows 上執行之 OpenGL ES 的詳細資訊，請參閱 [Windows Store 的角度](https://github.com/microsoft/angle/wiki)。</span><span class="sxs-lookup"><span data-stu-id="591a8-108">For information about OpenGL ES running on Windows, see [ANGLE for Windows Store](https://github.com/microsoft/angle/wiki).</span></span>

## <a name="where-applicable"></a><span data-ttu-id="591a8-109">適用時</span><span class="sxs-lookup"><span data-stu-id="591a8-109">Where applicable</span></span>

<span data-ttu-id="591a8-110">OpenGL 是針對硬體和作業系統之間的相容性所建立的。</span><span class="sxs-lookup"><span data-stu-id="591a8-110">OpenGL is built for compatibility across hardware and operating systems.</span></span> <span data-ttu-id="591a8-111">此架構可讓您輕鬆地將 OpenGL 程式從某個系統移植到另一個系統。</span><span class="sxs-lookup"><span data-stu-id="591a8-111">This architecture makes it easy to port OpenGL programs from one system to another.</span></span> <span data-ttu-id="591a8-112">雖然每個作業系統都有獨特的需求，但許多程式中的 OpenGL 程式碼可依原樣使用。</span><span class="sxs-lookup"><span data-stu-id="591a8-112">While each operating system has unique requirements, the OpenGL code in many programs can be used as is.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="591a8-113">開發人員對象</span><span class="sxs-lookup"><span data-stu-id="591a8-113">Developer audience</span></span>

<span data-ttu-id="591a8-114">OpenGL 是針對 C/c + + 程式設計人員所設計，需要熟悉 Windows 圖形化使用者介面以及訊息驅動架構。</span><span class="sxs-lookup"><span data-stu-id="591a8-114">Designed for use by C/C++ programmers, OpenGL requires familiarity with the Windows graphical user interface as well as message-driven architecture.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="591a8-115">執行階段需求求</span><span class="sxs-lookup"><span data-stu-id="591a8-115">Run-time requirements</span></span>

<span data-ttu-id="591a8-116">如需特定功能需要哪些作業系統的詳細資訊，請參閱函式檔集的需求一節。</span><span class="sxs-lookup"><span data-stu-id="591a8-116">For more information on which operating systems are required for a particular function, see the Requirements section of the documentation for the function.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="591a8-117">本節內容</span><span class="sxs-lookup"><span data-stu-id="591a8-117">In this section</span></span>



| <span data-ttu-id="591a8-118">主題</span><span class="sxs-lookup"><span data-stu-id="591a8-118">Topic</span></span>                                             | <span data-ttu-id="591a8-119">描述</span><span class="sxs-lookup"><span data-stu-id="591a8-119">Description</span></span>                                                                        |
|---------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="591a8-120">概觀</span><span class="sxs-lookup"><span data-stu-id="591a8-120">Overview</span></span>](basic-opengl-operation.md)<br/> | <span data-ttu-id="591a8-121">OpenGL 運作方式的一般資訊。</span><span class="sxs-lookup"><span data-stu-id="591a8-121">General information about how OpenGL works.</span></span><br/>                             |
| [<span data-ttu-id="591a8-122">參考</span><span class="sxs-lookup"><span data-stu-id="591a8-122">Reference</span></span>](opengl-reference.md)<br/>      | <span data-ttu-id="591a8-123">函數、結構和其他程式設計專案的檔。</span><span class="sxs-lookup"><span data-stu-id="591a8-123">Documentation of functions, structures, and other programming elements.</span></span><br/> |
| [<span data-ttu-id="591a8-124">範例</span><span class="sxs-lookup"><span data-stu-id="591a8-124">Samples</span></span>](a-porting-sample.md)<br/>        | <span data-ttu-id="591a8-125">OpenGL 程式碼的範例。</span><span class="sxs-lookup"><span data-stu-id="591a8-125">Examples of OpenGL code.</span></span><br/>                                                |



 

## <a name="related-topics"></a><span data-ttu-id="591a8-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="591a8-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="591a8-127">DirectX 圖形與遊戲</span><span class="sxs-lookup"><span data-stu-id="591a8-127">DirectX Graphics and Gaming</span></span>](/windows/desktop/directx)
</dt> <dt>

<span data-ttu-id="591a8-128">[靜止影像](/previous-versions/windows/desktop/legacy/cc836557(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="591a8-128">[Still Image](/previous-versions/windows/desktop/legacy/cc836557(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="591a8-129">[Windows Color System (WCS) ](/previous-versions//dd372446(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="591a8-129">[Windows Color System (WCS)](/previous-versions//dd372446(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="591a8-130">Windows GDI</span><span class="sxs-lookup"><span data-stu-id="591a8-130">Windows GDI</span></span>](/windows/desktop/gdi/windows-gdi)
</dt> <dt>

[<span data-ttu-id="591a8-131">Windows 映像取得</span><span class="sxs-lookup"><span data-stu-id="591a8-131">Windows Image Acquisition</span></span>](../wia/-wia-startpage.md)
</dt> <dt>

[<span data-ttu-id="591a8-132">Windows 多媒體</span><span class="sxs-lookup"><span data-stu-id="591a8-132">Windows Multimedia</span></span>](/windows/desktop/Multimedia/windows-multimedia-start-page)
</dt> <dt>

<span data-ttu-id="591a8-133">[Windows 應用程式開發介面](/previous-versions//cc433218(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="591a8-133">[Windows API](/previous-versions//cc433218(v=vs.85))</span></span>
</dt> </dl>

 

