---
title: DX9 舊版硬體支援的變更
description: DX9 舊版硬體支援的變更
ms.assetid: 25C7DFC7-58F4-4F6D-8D26-6DBA92424A0B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc1ae5c4b15a2019450cc5b209f34561d8ec672d
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/01/2020
ms.locfileid: "106966893"
---
# <a name="changes-in-dx9-legacy-hardware-support"></a><span data-ttu-id="2cce8-103">DX9 舊版硬體支援的變更</span><span class="sxs-lookup"><span data-stu-id="2cce8-103">Changes in DX9 legacy hardware support</span></span>

## <a name="platform"></a><span data-ttu-id="2cce8-104">平台</span><span class="sxs-lookup"><span data-stu-id="2cce8-104">Platform</span></span>

<span data-ttu-id="2cce8-105">**用戶端** – Windows 8</span><span class="sxs-lookup"><span data-stu-id="2cce8-105">**Clients** – Windows 8</span></span> 


## <a name="description"></a><span data-ttu-id="2cce8-106">Description</span><span class="sxs-lookup"><span data-stu-id="2cce8-106">Description</span></span>

<span data-ttu-id="2cce8-107">Intel 和 AMD/ATI 不再支援其 DX9 圖形元件，也不會更新這些裝置的驅動程式以進行 Windows 8。</span><span class="sxs-lookup"><span data-stu-id="2cce8-107">Intel and AMD/ATI no longer support their DX9 graphics parts and will not be updating drivers for these devices for Windows 8.</span></span> <span data-ttu-id="2cce8-108">此外，這些裝置不會涵蓋 Windows 8 的現成討論。</span><span class="sxs-lookup"><span data-stu-id="2cce8-108">Furthermore, these devices are not covered in-box for Windows 8.</span></span> <span data-ttu-id="2cce8-109">這些裝置的最後一個驅動程式是在 WU 和 OEM/IHV 網站上提供的驅動程式;來自 Vista 的許多日期，而這些最終版本驅動程式當中有許多是 Windows 8 的問題。</span><span class="sxs-lookup"><span data-stu-id="2cce8-109">The last drivers for these devices are those available on WU and on the OEM/IHV’s websites; many date from Vista, and many of these final version drivers exhibit problems on Windows 8.</span></span> <span data-ttu-id="2cce8-110">此外，nVidia 最近也指出，它們不支援 DX9 (Vista 和舊版) mobile (筆記本) 部分進行 Windows 8。</span><span class="sxs-lookup"><span data-stu-id="2cce8-110">In addition, nVidia has recently stated that they will not support their DX9 (Vista and older) mobile (notebook) parts for Windows 8.</span></span> <span data-ttu-id="2cce8-111">它們會繼續支援其桌面 DX9 元件。</span><span class="sxs-lookup"><span data-stu-id="2cce8-111">They continue to support their desktop DX9 parts.</span></span>

<span data-ttu-id="2cce8-112">這些驅動程式/元件組合全都位於 Internet Explorer 9 軟體回復清單上。</span><span class="sxs-lookup"><span data-stu-id="2cce8-112">All of these driver/part combinations are on the Internet Explorer 9 software fallback list.</span></span> <span data-ttu-id="2cce8-113">這表示基於效能或穩定性的原因，Internet Explorer 9 在這些裝置上使用軟體轉譯。</span><span class="sxs-lookup"><span data-stu-id="2cce8-113">This means that for either performance or stability reasons, Internet Explorer 9 uses software rendering on these devices.</span></span> <span data-ttu-id="2cce8-114">這是很好的指示，Windows Store 應用程式的使用體驗對這些驅動程式和元件並不滿意。</span><span class="sxs-lookup"><span data-stu-id="2cce8-114">This is a good indication that the experience with Windows Store apps will not be satisfactory on these drivers and parts.</span></span>

## <a name="manifestation"></a><span data-ttu-id="2cce8-115">表現</span><span class="sxs-lookup"><span data-stu-id="2cce8-115">Manifestation</span></span>

<span data-ttu-id="2cce8-116">因為這些裝置沒有任何現成的支援，所以具有這些元件的許多使用者將會在 Microsoft 基本顯示器驅動程式上執行。</span><span class="sxs-lookup"><span data-stu-id="2cce8-116">As there is no in-box support for these devices, many users with these parts will wind up running on the Microsoft Basic Display Driver.</span></span> <span data-ttu-id="2cce8-117">這是以變形為基礎的 WDDM 1.2 軟體 GPU，其實比這個類別的部分部分更快，例如 Intel GMA500 系列) 。</span><span class="sxs-lookup"><span data-stu-id="2cce8-117">This is a WARP-based WDDM 1.2 software GPU, and is actually faster than some of the parts in this class, for example, the Intel GMA500 series).</span></span> <span data-ttu-id="2cce8-118">它支援 aero 玻璃和 DWM，並且可以執行 Windows Store 應用程式。</span><span class="sxs-lookup"><span data-stu-id="2cce8-118">It supports aero-glass and DWM, and can run Windows Store apps.</span></span>

<span data-ttu-id="2cce8-119">不過，它有一些重要的限制：</span><span class="sxs-lookup"><span data-stu-id="2cce8-119">However, it has some important limitations:</span></span>

-   <span data-ttu-id="2cce8-120">它不支援多個監視器或投影</span><span class="sxs-lookup"><span data-stu-id="2cce8-120">It doesn’t support multiple monitors or projection</span></span>
-   <span data-ttu-id="2cce8-121">它不支援睡眠，但支援休眠</span><span class="sxs-lookup"><span data-stu-id="2cce8-121">It doesn’t support sleep, though it does support hibernation</span></span>
-   <span data-ttu-id="2cce8-122">它通常不允許變更螢幕解析度</span><span class="sxs-lookup"><span data-stu-id="2cce8-122">It often will not allow changing screen resolution</span></span>

## <a name="mitigation"></a><span data-ttu-id="2cce8-123">降低</span><span class="sxs-lookup"><span data-stu-id="2cce8-123">Mitigation</span></span>

<span data-ttu-id="2cce8-124">測試之後，如果您發現使用者體驗無法接受，您可以選擇設定其產品的硬體需求，以排除這些較舊的 DX9 Intel 和 AMD 元件。</span><span class="sxs-lookup"><span data-stu-id="2cce8-124">If after testing, you find that the user experience is not acceptable, you may choose to set hardware requirements for their products that exclude these older DX9 Intel and AMD parts.</span></span> <span data-ttu-id="2cce8-125">您也可以選擇對客戶發出警示，讓他們在這些部分上可能會有無法接受的體驗。</span><span class="sxs-lookup"><span data-stu-id="2cce8-125">You may also choose to alert your customers that they may have an unacceptable experience on these parts.</span></span>

## <a name="tests"></a><span data-ttu-id="2cce8-126">測試</span><span class="sxs-lookup"><span data-stu-id="2cce8-126">Tests</span></span>

<span data-ttu-id="2cce8-127">評估這些裝置的效能和體驗：</span><span class="sxs-lookup"><span data-stu-id="2cce8-127">Evaluate the performance and experience on these devices:</span></span>

-   <span data-ttu-id="2cce8-128">最終可用驅動程式版本的體驗為何？</span><span class="sxs-lookup"><span data-stu-id="2cce8-128">What is the experience like on the final driver version available?</span></span>
-   <span data-ttu-id="2cce8-129">MSBDD 上的體驗為何？</span><span class="sxs-lookup"><span data-stu-id="2cce8-129">What is the experience like on the MSBDD?</span></span>

 

 




