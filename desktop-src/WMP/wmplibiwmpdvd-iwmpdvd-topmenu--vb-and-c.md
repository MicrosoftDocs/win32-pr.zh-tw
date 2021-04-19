---
title: IWMPDVD topMenu 方法
description: TopMenu 方法會停止播放，並顯示目前標題的上方 (或根) 功能表。
ms.assetid: d6eb6311-167d-4cc1-b445-4e3d3e111e43
keywords:
- topMenu 方法 Windows Media Player
- topMenu 方法 Windows Media Player，IWMPDVD 介面
- IWMPDVD 介面 Windows Media Player，topMenu 方法
topic_type:
- apiref
api_name:
- IWMPDVD.topMenu
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d59bf126a026626cc7f1ba87ea9d0eb94bd1a91
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996464"
---
# <a name="iwmpdvdtopmenu-method"></a><span data-ttu-id="d272c-106">IWMPDVD：： topMenu 方法</span><span class="sxs-lookup"><span data-stu-id="d272c-106">IWMPDVD::topMenu method</span></span>

<span data-ttu-id="d272c-107">**TopMenu** 方法會停止播放，並顯示目前標題的上方 (或根) 功能表。</span><span class="sxs-lookup"><span data-stu-id="d272c-107">The **topMenu** method stops playback and displays the top (or root) menu for the current title.</span></span>

## <a name="syntax"></a><span data-ttu-id="d272c-108">語法</span><span class="sxs-lookup"><span data-stu-id="d272c-108">Syntax</span></span>


```CSharp
public void topMenu();
```


```VB

Public Sub topMenu()
Implements IWMPDVD.topMenu
```





## <a name="parameters"></a><span data-ttu-id="d272c-109">參數</span><span class="sxs-lookup"><span data-stu-id="d272c-109">Parameters</span></span>

<span data-ttu-id="d272c-110">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="d272c-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d272c-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="d272c-111">Return value</span></span>

<span data-ttu-id="d272c-112">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="d272c-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d272c-113">備註</span><span class="sxs-lookup"><span data-stu-id="d272c-113">Remarks</span></span>

<span data-ttu-id="d272c-114">每個 DVD 的撰寫方式不同。</span><span class="sxs-lookup"><span data-stu-id="d272c-114">Every DVD is authored differently.</span></span> <span data-ttu-id="d272c-115">DVD 必須包含功能表，這個方法才能運作。</span><span class="sxs-lookup"><span data-stu-id="d272c-115">The DVD must contain a menu for this method to work.</span></span> <span data-ttu-id="d272c-116">某些 Dvd 的撰寫方式是讓 **topMenu** 和 **IWMPDVD titleMenu** 方法開啟相同的功能表。</span><span class="sxs-lookup"><span data-stu-id="d272c-116">Some DVDs are authored so that the **topMenu** and **IWMPDVD.titleMenu** methods open the same menu.</span></span> <span data-ttu-id="d272c-117">**TopMenu** 方法通常會叫用頂端 (或根) 功能表，但如果沒有可用的根功能表，它可能會叫用標題功能表。</span><span class="sxs-lookup"><span data-stu-id="d272c-117">The **topMenu** method usually invokes the top (or root) menu, but it may invoke the title menu if there is no root menu available.</span></span>

## <a name="requirements"></a><span data-ttu-id="d272c-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="d272c-118">Requirements</span></span>



| <span data-ttu-id="d272c-119">需求</span><span class="sxs-lookup"><span data-stu-id="d272c-119">Requirement</span></span> | <span data-ttu-id="d272c-120">值</span><span class="sxs-lookup"><span data-stu-id="d272c-120">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d272c-121">版本</span><span class="sxs-lookup"><span data-stu-id="d272c-121">Version</span></span><br/>   | <span data-ttu-id="d272c-122">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="d272c-122">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="d272c-123">命名空間</span><span class="sxs-lookup"><span data-stu-id="d272c-123">Namespace</span></span><br/> | <span data-ttu-id="d272c-124">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="d272c-124">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="d272c-125">組件</span><span class="sxs-lookup"><span data-stu-id="d272c-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="d272c-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="d272c-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d272c-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d272c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d272c-128">**IWMPDVD 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="d272c-128">**IWMPDVD Interface (VB and C#)**</span></span>](iwmpdvd--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="d272c-129">**IWMPDVD. titleMenu (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="d272c-129">**IWMPDVD.titleMenu (VB and C#)**</span></span>](wmplibiwmpdvd-iwmpdvd-titlemenu--vb-and-c.md)
</dt> </dl>

 

 





