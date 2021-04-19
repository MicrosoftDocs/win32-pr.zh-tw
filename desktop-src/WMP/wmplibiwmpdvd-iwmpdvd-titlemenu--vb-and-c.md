---
title: IWMPDVD titleMenu 方法
description: TitleMenu 方法會停止播放並顯示標題功能表。
ms.assetid: 28714644-12c4-46eb-95fc-70091624f6dd
keywords:
- titleMenu 方法 Windows Media Player
- titleMenu 方法 Windows Media Player，IWMPDVD 介面
- IWMPDVD 介面 Windows Media Player，titleMenu 方法
topic_type:
- apiref
api_name:
- IWMPDVD.titleMenu
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0889a3f65ccefe4e09bb5ff47a66867681dcc801
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996465"
---
# <a name="iwmpdvdtitlemenu-method"></a><span data-ttu-id="48f9c-106">IWMPDVD：： titleMenu 方法</span><span class="sxs-lookup"><span data-stu-id="48f9c-106">IWMPDVD::titleMenu method</span></span>

<span data-ttu-id="48f9c-107">**TitleMenu** 方法會停止播放並顯示標題功能表。</span><span class="sxs-lookup"><span data-stu-id="48f9c-107">The **titleMenu** method stops playback and displays the title menu.</span></span>

## <a name="syntax"></a><span data-ttu-id="48f9c-108">語法</span><span class="sxs-lookup"><span data-stu-id="48f9c-108">Syntax</span></span>


```CSharp
public void titleMenu();
```


```VB

Public Sub titleMenu()
Implements IWMPDVD.titleMenu
```





## <a name="parameters"></a><span data-ttu-id="48f9c-109">參數</span><span class="sxs-lookup"><span data-stu-id="48f9c-109">Parameters</span></span>

<span data-ttu-id="48f9c-110">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="48f9c-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="48f9c-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="48f9c-111">Return value</span></span>

<span data-ttu-id="48f9c-112">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="48f9c-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="48f9c-113">備註</span><span class="sxs-lookup"><span data-stu-id="48f9c-113">Remarks</span></span>

<span data-ttu-id="48f9c-114">每個 DVD 的撰寫方式不同。</span><span class="sxs-lookup"><span data-stu-id="48f9c-114">Every DVD is authored differently.</span></span> <span data-ttu-id="48f9c-115">DVD 必須包含功能表，這個方法才能運作。</span><span class="sxs-lookup"><span data-stu-id="48f9c-115">The DVD must contain a menu for this method to work.</span></span> <span data-ttu-id="48f9c-116">撰寫一些 Dvd，讓 **IWMPDVD. topMenu** 和 **titleMenu** 方法開啟相同的功能表。</span><span class="sxs-lookup"><span data-stu-id="48f9c-116">Some DVDs are authored so that the **IWMPDVD.topMenu** and **titleMenu** methods open the same menu.</span></span> <span data-ttu-id="48f9c-117">**TitleMenu** 方法通常會叫用標題功能表，但如果沒有可用的標題功能表，它可能會叫用頂端功能表。</span><span class="sxs-lookup"><span data-stu-id="48f9c-117">The **titleMenu** method usually invokes the title menu, but it may invoke the top menu if there is no title menu available.</span></span>

## <a name="requirements"></a><span data-ttu-id="48f9c-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="48f9c-118">Requirements</span></span>



| <span data-ttu-id="48f9c-119">需求</span><span class="sxs-lookup"><span data-stu-id="48f9c-119">Requirement</span></span> | <span data-ttu-id="48f9c-120">值</span><span class="sxs-lookup"><span data-stu-id="48f9c-120">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="48f9c-121">版本</span><span class="sxs-lookup"><span data-stu-id="48f9c-121">Version</span></span><br/>   | <span data-ttu-id="48f9c-122">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="48f9c-122">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="48f9c-123">命名空間</span><span class="sxs-lookup"><span data-stu-id="48f9c-123">Namespace</span></span><br/> | <span data-ttu-id="48f9c-124">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="48f9c-124">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="48f9c-125">組件</span><span class="sxs-lookup"><span data-stu-id="48f9c-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="48f9c-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="48f9c-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48f9c-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="48f9c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48f9c-128">**IWMPDVD 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="48f9c-128">**IWMPDVD Interface (VB and C#)**</span></span>](iwmpdvd--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="48f9c-129">**IWMPDVD. topMenu (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="48f9c-129">**IWMPDVD.topMenu (VB and C#)**</span></span>](wmplibiwmpdvd-iwmpdvd-topmenu--vb-and-c.md)
</dt> </dl>

 

 





