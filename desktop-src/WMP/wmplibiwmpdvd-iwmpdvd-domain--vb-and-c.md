---
title: IWMPDVD 網域屬性
description: 網域屬性會取得 DVD 的目前網域。
ms.assetid: 0b7b39fe-2b04-44e2-aa5e-cab7be9a06b1
keywords:
- 網域屬性 Windows Media Player
- 網域屬性 Windows Media Player、IWMPDVD 介面
- IWMPDVD 介面 Windows Media Player，網域屬性
topic_type:
- apiref
api_name:
- IWMPDVD.domain
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6546a8288160fe80f7df4a7c41ea79a0edc905f4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996051"
---
# <a name="iwmpdvddomain-property"></a><span data-ttu-id="c5d52-106">IWMPDVD：:d omain 屬性</span><span class="sxs-lookup"><span data-stu-id="c5d52-106">IWMPDVD::domain property</span></span>

<span data-ttu-id="c5d52-107">**網域** 屬性會取得 DVD 的目前網域。</span><span class="sxs-lookup"><span data-stu-id="c5d52-107">The **domain** property gets the current domain of the DVD.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5d52-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="c5d52-108">Syntax</span></span>


```CSharp
public System.String domain {get; set;}
```


```VB

Public ReadOnly Property domain As System.String
```





## <a name="property-value"></a><span data-ttu-id="c5d52-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="c5d52-109">Property value</span></span>

<span data-ttu-id="c5d52-110">**System.string** ，這是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="c5d52-110">A **System.String** that is one of the following values.</span></span>



| <span data-ttu-id="c5d52-111">值</span><span class="sxs-lookup"><span data-stu-id="c5d52-111">Value</span></span>                                                                                        | <span data-ttu-id="c5d52-112">意義</span><span class="sxs-lookup"><span data-stu-id="c5d52-112">Meaning</span></span>                                                                                                                                          |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c5d52-113"><dt>firstPlay</dt></span><span class="sxs-lookup"><span data-stu-id="c5d52-113"><dt>firstPlay</dt></span></span> </dl>         | <span data-ttu-id="c5d52-114">執行 DVD 光碟的預設初始化。</span><span class="sxs-lookup"><span data-stu-id="c5d52-114">Performing default initialization of a DVD disc.</span></span><br/>                                                                                      |
| <dl> <span data-ttu-id="c5d52-115"><dt>videoManagerMenu</dt></span><span class="sxs-lookup"><span data-stu-id="c5d52-115"><dt>videoManagerMenu</dt></span></span> </dl>  | <span data-ttu-id="c5d52-116">顯示整個光碟的功能表。也稱為 Windows Media Player 的 topMenu。</span><span class="sxs-lookup"><span data-stu-id="c5d52-116">Displaying menus for the entire disc. Also known as topMenu for Windows Media Player.</span></span> <span data-ttu-id="c5d52-117">通常稱為標題功能表或頂端功能表。</span><span class="sxs-lookup"><span data-stu-id="c5d52-117">Commonly called the title menu or the top menu.</span></span><br/> |
| <dl> <span data-ttu-id="c5d52-118"><dt>videoTitleSetMenu</dt></span><span class="sxs-lookup"><span data-stu-id="c5d52-118"><dt>videoTitleSetMenu</dt></span></span> </dl> | <span data-ttu-id="c5d52-119">顯示目前標題集的功能表。</span><span class="sxs-lookup"><span data-stu-id="c5d52-119">Displaying menus for the current title set.</span></span> <span data-ttu-id="c5d52-120">也稱為 Windows Media Player 的 titleMenu。</span><span class="sxs-lookup"><span data-stu-id="c5d52-120">Also known as titleMenu for Windows Media Player.</span></span> <span data-ttu-id="c5d52-121">通常稱為根功能表。</span><span class="sxs-lookup"><span data-stu-id="c5d52-121">Commonly called the root menu.</span></span><br/>          |
| <dl> <span data-ttu-id="c5d52-122"><dt>title</dt></span><span class="sxs-lookup"><span data-stu-id="c5d52-122"><dt>title</dt></span></span> </dl>             | <span data-ttu-id="c5d52-123">通常會顯示目前的標題。</span><span class="sxs-lookup"><span data-stu-id="c5d52-123">Usually, displaying the current title.</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="c5d52-124"><dt>停止</dt></span><span class="sxs-lookup"><span data-stu-id="c5d52-124"><dt>stop</dt></span></span> </dl>              | <span data-ttu-id="c5d52-125">DVD 導覽器位於 DVD 停止網域中。</span><span class="sxs-lookup"><span data-stu-id="c5d52-125">The DVD Navigator is in the DVD Stop domain.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="c5d52-126"><dt>定義</dt></span><span class="sxs-lookup"><span data-stu-id="c5d52-126"><dt>undefined</dt></span></span> </dl>         | <span data-ttu-id="c5d52-127">Windows Media Player 不在任何 DVD 網域中。</span><span class="sxs-lookup"><span data-stu-id="c5d52-127">Windows Media Player is not in any DVD domain.</span></span><br/>                                                                                        |



 

## <a name="remarks"></a><span data-ttu-id="c5d52-128">備註</span><span class="sxs-lookup"><span data-stu-id="c5d52-128">Remarks</span></span>

<span data-ttu-id="c5d52-129">每個 DVD 的撰寫方式不同。</span><span class="sxs-lookup"><span data-stu-id="c5d52-129">Every DVD is authored differently.</span></span> <span data-ttu-id="c5d52-130">某些 Dvd 不包含 firstPlay、videoManagerMenu 或 videoTitleSetMenu 網域。</span><span class="sxs-lookup"><span data-stu-id="c5d52-130">Some DVDs do not contain the firstPlay, videoManagerMenu, or videoTitleSetMenu domains.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5d52-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="c5d52-131">Requirements</span></span>



| <span data-ttu-id="c5d52-132">需求</span><span class="sxs-lookup"><span data-stu-id="c5d52-132">Requirement</span></span> | <span data-ttu-id="c5d52-133">值</span><span class="sxs-lookup"><span data-stu-id="c5d52-133">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5d52-134">版本</span><span class="sxs-lookup"><span data-stu-id="c5d52-134">Version</span></span><br/>   | <span data-ttu-id="c5d52-135">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="c5d52-135">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="c5d52-136">命名空間</span><span class="sxs-lookup"><span data-stu-id="c5d52-136">Namespace</span></span><br/> | <span data-ttu-id="c5d52-137">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="c5d52-137">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="c5d52-138">組件</span><span class="sxs-lookup"><span data-stu-id="c5d52-138">Assembly</span></span><br/>  | <dl> <span data-ttu-id="c5d52-139"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="c5d52-139"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5d52-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c5d52-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5d52-141">**IWMPDVD 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="c5d52-141">**IWMPDVD Interface (VB and C#)**</span></span>](iwmpdvd--vb-and-c.md)
</dt> </dl>

 

 





