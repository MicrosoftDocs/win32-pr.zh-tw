---
description: 若要讓應用程式正常執行，主機電腦必須安裝適當的 Dll。 這些 Dll 可能是由作業系統或應用程式的可轉散發套件提供。
ms.assetid: fa5405e9-116f-4b7f-8f8e-791a79942570
title: '將靜態和動態連結程式庫連結 (Direct3D 10) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a7050b8a3b5e1e2544883eb140b67d50bc3cd11
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972550"
---
# <a name="linking-static-and-dynamic-libraries-direct3d-10"></a><span data-ttu-id="47f88-104">將靜態和動態連結程式庫連結 (Direct3D 10) </span><span class="sxs-lookup"><span data-stu-id="47f88-104">Linking Static and Dynamic Libraries (Direct3D 10)</span></span>

<span data-ttu-id="47f88-105">若要讓應用程式正常執行，主機電腦必須安裝適當的 Dll。</span><span class="sxs-lookup"><span data-stu-id="47f88-105">For an application to run properly, the host computer must have the appropriate DLLs installed.</span></span> <span data-ttu-id="47f88-106">這些 Dll 可能是由作業系統或應用程式的可轉散發套件提供。</span><span class="sxs-lookup"><span data-stu-id="47f88-106">These DLLs may be provided by either the operating system, or the applications' redistributable package.</span></span>

## <a name="libraries-load-appropriate-dlls"></a><span data-ttu-id="47f88-107">程式庫載入適當的 Dll</span><span class="sxs-lookup"><span data-stu-id="47f88-107">Libraries Load Appropriate DLLs</span></span>

<span data-ttu-id="47f88-108">DirectX SDK 隨附的程式庫會在執行時間自動載入適當的 Dll。</span><span class="sxs-lookup"><span data-stu-id="47f88-108">The libraries included with the DirectX SDK will automatically load the proper DLLs at runtime.</span></span> <span data-ttu-id="47f88-109">這項規則的例外狀況是 d3dx10 .lib/d3dx10d .lib，它會載入該版本 SDK 隨附的 d3dx10.dll。</span><span class="sxs-lookup"><span data-stu-id="47f88-109">The exception to this rule is d3dx10.lib/d3dx10d.lib, which will load the d3dx10.dll that was shipped with that version of the SDK.</span></span> <span data-ttu-id="47f88-110">例如，如果下載的 SDK 包含 d3dx10 \_33.dll 和 d3dx10 \_34.dll，則隨附于該 sdk 的程式庫 (d3dx10) .lib 將載入 d3dx10 \_34.dll。</span><span class="sxs-lookup"><span data-stu-id="47f88-110">For example, if the downloaded SDK includes d3dx10\_33.dll and d3dx10\_34.dll, then the library (d3dx10.lib) that shipped with that SDK will load d3dx10\_34.dll.</span></span> <span data-ttu-id="47f88-111">如果後續的 SDK 稍後再安裝包含 d3dx10 \_ 35... a sdk，則先前 sdk 的 d3dx10 仍會載入 d3dx10 \_34.dll。</span><span class="sxs-lookup"><span data-stu-id="47f88-111">If a subsequent SDK is installed later containing d3dx10\_35.lib, the d3dx10.lib from the previous SDK will still load d3dx10\_34.dll.</span></span> <span data-ttu-id="47f88-112">較新 SDK 的 d3dx10 會載入 d3dx10 \_35.dll。</span><span class="sxs-lookup"><span data-stu-id="47f88-112">The d3dx10.lib from the newer SDK will load d3dx10\_35.dll.</span></span>

## <a name="redistributing-binaries"></a><span data-ttu-id="47f88-113">轉散發二進位檔</span><span class="sxs-lookup"><span data-stu-id="47f88-113">Redistributing Binaries</span></span>

<span data-ttu-id="47f88-114">您只能重新散發相同檔案) 的 d3dx10.dll (和後續版本。</span><span class="sxs-lookup"><span data-stu-id="47f88-114">Only d3dx10.dll (and subsequent versions of the same file) can be redistributed.</span></span> <span data-ttu-id="47f88-115">若要重新發佈此檔案，您必須使用 **DirectXSetup** 函數。</span><span class="sxs-lookup"><span data-stu-id="47f88-115">To redistribute this file, you must use the **DirectXSetup** function.</span></span> <span data-ttu-id="47f88-116">如需使用此函式並將可轉散發套件放在一起的詳細資訊，請參閱使用 [DirectSetup 安裝 DirectX](https://msdn.microsoft.com/library/Ee418267(v=VS.85).aspx)。</span><span class="sxs-lookup"><span data-stu-id="47f88-116">For details on using this function and putting together a redistributable package, see [Installing DirectX with DirectSetup](https://msdn.microsoft.com/library/Ee418267(v=VS.85).aspx).</span></span> <span data-ttu-id="47f88-117">Windows Vista 中包含所有其他必要的二進位檔。</span><span class="sxs-lookup"><span data-stu-id="47f88-117">All other necessary binaries are included in Windows Vista.</span></span> <span data-ttu-id="47f88-118">唯一可轉散發的二進位檔是位於下列目錄中的二進位檔。</span><span class="sxs-lookup"><span data-stu-id="47f88-118">The only binaries that can be redistributed are those located in the following directory.</span></span>


```
(SDK root)\Redist
```



<span data-ttu-id="47f88-119">下表描述開發人員應該注意的二進位檔。</span><span class="sxs-lookup"><span data-stu-id="47f88-119">The following table describes the binaries developers should be aware of.</span></span>



| <span data-ttu-id="47f88-120">Direct3D 10 二進位檔</span><span class="sxs-lookup"><span data-stu-id="47f88-120">Direct3D 10 Binaries</span></span>   | <span data-ttu-id="47f88-121">Description</span><span class="sxs-lookup"><span data-stu-id="47f88-121">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="47f88-122">d3dx10.dll/d3dx10d.dll</span><span class="sxs-lookup"><span data-stu-id="47f88-122">d3dx10.dll/d3dx10d.dll</span></span> | <span data-ttu-id="47f88-123">零售和 debug D3DX10 元件;零售元件可以在可轉散發套件的封包中轉散發。</span><span class="sxs-lookup"><span data-stu-id="47f88-123">Retail and debug D3DX10 components; the retail components can be redistributed in the REDIST CAB.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="47f88-124">d3d10ref.dll</span><span class="sxs-lookup"><span data-stu-id="47f88-124">d3d10ref.dll</span></span>           | <span data-ttu-id="47f88-125">參考轉譯器。</span><span class="sxs-lookup"><span data-stu-id="47f88-125">Reference Rasterizer.</span></span> <span data-ttu-id="47f88-126">提供圖形管線的軟體執行。</span><span class="sxs-lookup"><span data-stu-id="47f88-126">Provides software implementation of the graphics pipeline.</span></span> <span data-ttu-id="47f88-127">只包含為 Windows SDK 或舊版 DirectX SDK 的一部分，而且無法重新散發。</span><span class="sxs-lookup"><span data-stu-id="47f88-127">Only included as part of the Windows SDK or legacy DirectX SDK and cannot be redistributed.</span></span> <span data-ttu-id="47f88-128">參考轉譯器僅適用于偵錯工具。</span><span class="sxs-lookup"><span data-stu-id="47f88-128">The Reference Rasterizer is intended for debugging only.</span></span> <span data-ttu-id="47f88-129">不需要明確連結;嘗試建立參考設備 (請參閱 [**D3D10CreateDevice**](/windows/desktop/api/D3D10Misc/nf-d3d10misc-d3d10createdevice)) 將會載入此 dll （如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="47f88-129">Explicit linking is not necessary; attempting to create a reference device (see [**D3D10CreateDevice**](/windows/desktop/api/D3D10Misc/nf-d3d10misc-d3d10createdevice)) will load this dll if it is present.</span></span>                                                                                                    |
| <span data-ttu-id="47f88-130">d3d10sdklayers.dll</span><span class="sxs-lookup"><span data-stu-id="47f88-130">d3d10sdklayers.dll</span></span>     | <span data-ttu-id="47f88-131">一系列的 SDK 公用程式，可做為 API 呼叫與執行時間執行之間的一層，包括 [debug 層](d3d10-graphics-programming-guide-api-features-layers.md) 和切換為參考層。</span><span class="sxs-lookup"><span data-stu-id="47f88-131">A series of SDK utilities that act as a layer between API calls and runtime execution, including the [debug layer](d3d10-graphics-programming-guide-api-features-layers.md) and the switch-to-reference layer.</span></span> <span data-ttu-id="47f88-132">不需要明確連結;如果使用適當的圖層旗標建立裝置，則會自動載入此 DLL。</span><span class="sxs-lookup"><span data-stu-id="47f88-132">Explicit linking is not necessary; if a device is created with the appropriate layer flag, this DLL is loaded automatically.</span></span> <span data-ttu-id="47f88-133">此元件僅供開發和偵測之用。</span><span class="sxs-lookup"><span data-stu-id="47f88-133">This component is meant for development and debugging purposes only.</span></span> <span data-ttu-id="47f88-134">只包含為 Windows SDK 或舊版 DirectX SDK 的一部分，而且無法重新散發。</span><span class="sxs-lookup"><span data-stu-id="47f88-134">Only included as part of the Windows SDK or legacy DirectX SDK and cannot be redistributed.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="47f88-135">相關主題</span><span class="sxs-lookup"><span data-stu-id="47f88-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="47f88-136">Direct3D 10 程式設計手冊</span><span class="sxs-lookup"><span data-stu-id="47f88-136">Programming Guide for Direct3D 10</span></span>](d3d10-graphics-programming-guide.md)
</dt> <dt>

[<span data-ttu-id="47f88-137">Direct3D 10 圖形</span><span class="sxs-lookup"><span data-stu-id="47f88-137">Direct3D 10 Graphics</span></span>](d3d10-graphics.md)
</dt> </dl>

 

 



