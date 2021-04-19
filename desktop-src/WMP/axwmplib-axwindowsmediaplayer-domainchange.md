---
title: AxWindowsMediaPlayer 物件的 DomainChange 事件
description: 當 DVD 網域變更時，就會發生 DomainChange 事件。 |AxWindowsMediaPlayer 物件的 DomainChange 事件
ms.assetid: a080082e-1ba4-4080-b39c-b84292ecacb0
keywords:
- AxWindowsMediaPlayer 物件的 DomainChange 事件 Windows Media Player
topic_type:
- apiref
api_name:
- DomainChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 342ac559f75c3bb7d65b442bfbdced5e5ed3f690
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000917"
---
# <a name="domainchange-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="34165-105">AxWindowsMediaPlayer 物件的 DomainChange 事件</span><span class="sxs-lookup"><span data-stu-id="34165-105">DomainChange Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="34165-106">當 DVD 網域變更時，就會發生 DomainChange 事件。</span><span class="sxs-lookup"><span data-stu-id="34165-106">The DomainChange event occurs when the DVD domain changes.</span></span>

``` syntax
[C#]
private void player_DomainChange(
  object sender,
  _WMPOCXEvents_DomainChangeEvent e
)

[Visual Basic]
Private Sub player_DomainChange(  
  sender As Object,
  e As _WMPOCXEvents_DomainChangeEvent
) Handles player.DomainChange
```

## <a name="event-data"></a><span data-ttu-id="34165-107">事件資料</span><span class="sxs-lookup"><span data-stu-id="34165-107">Event Data</span></span>

<span data-ttu-id="34165-108">與這個事件相關聯的處理常式屬於 **AxWMPLib 型別。 \_WMPOCXEvents \_ DomainChangeEventHandler**。</span><span class="sxs-lookup"><span data-stu-id="34165-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_DomainChangeEventHandler**.</span></span> <span data-ttu-id="34165-109">這個處理常式會接收 AxWMPLib 型別的引數 **。 \_WMPOCXEvents \_ DomainChangeEvent**，其中包含與這個事件相關的下列屬性。</span><span class="sxs-lookup"><span data-stu-id="34165-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_DomainChangeEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="34165-110">屬性</span><span class="sxs-lookup"><span data-stu-id="34165-110">Property</span></span>  | <span data-ttu-id="34165-111">描述</span><span class="sxs-lookup"><span data-stu-id="34165-111">Description</span></span>                                                                                     |
|-----------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34165-112">strDomain</span><span class="sxs-lookup"><span data-stu-id="34165-112">strDomain</span></span> | <span data-ttu-id="34165-113">StringIndicates 新網域。</span><span class="sxs-lookup"><span data-stu-id="34165-113">System.StringIndicates the new domain.</span></span> <span data-ttu-id="34165-114">如需了解可能的值，請參閱＜備註＞一節。</span><span class="sxs-lookup"><span data-stu-id="34165-114">For possible values, see the Remarks section.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="34165-115">備註</span><span class="sxs-lookup"><span data-stu-id="34165-115">Remarks</span></span>

<span data-ttu-id="34165-116">下表顯示 strDomain 屬性的可能值。</span><span class="sxs-lookup"><span data-stu-id="34165-116">The following table shows the possible values for the strDomain property.</span></span>



| <span data-ttu-id="34165-117">String</span><span class="sxs-lookup"><span data-stu-id="34165-117">String</span></span>            | <span data-ttu-id="34165-118">Description</span><span class="sxs-lookup"><span data-stu-id="34165-118">Description</span></span>                                                          |
|-------------------|----------------------------------------------------------------------|
| <span data-ttu-id="34165-119">firstPlay</span><span class="sxs-lookup"><span data-stu-id="34165-119">firstPlay</span></span>         | <span data-ttu-id="34165-120">執行 DVD 光碟的預設初始化。</span><span class="sxs-lookup"><span data-stu-id="34165-120">Performing default initialization of a DVD disc.</span></span>                     |
| <span data-ttu-id="34165-121">videoManagerMenu</span><span class="sxs-lookup"><span data-stu-id="34165-121">videoManagerMenu</span></span>  | <span data-ttu-id="34165-122">顯示整個光碟的功能表。也稱為根功能表或 topMenu。</span><span class="sxs-lookup"><span data-stu-id="34165-122">Displaying menus for whole disc. Also known as Root Menu or topMenu.</span></span> |
| <span data-ttu-id="34165-123">videoTitleSetMenu</span><span class="sxs-lookup"><span data-stu-id="34165-123">videoTitleSetMenu</span></span> | <span data-ttu-id="34165-124">顯示目前標題集的功能表。</span><span class="sxs-lookup"><span data-stu-id="34165-124">Displaying menus for current title set.</span></span> <span data-ttu-id="34165-125">也稱為 titleMenu。</span><span class="sxs-lookup"><span data-stu-id="34165-125">Also known as titleMenu.</span></span>     |
| <span data-ttu-id="34165-126">title</span><span class="sxs-lookup"><span data-stu-id="34165-126">title</span></span>             | <span data-ttu-id="34165-127">顯示目前的標題。</span><span class="sxs-lookup"><span data-stu-id="34165-127">Displaying the current title.</span></span>                                        |
| <span data-ttu-id="34165-128">stop</span><span class="sxs-lookup"><span data-stu-id="34165-128">stop</span></span>              | <span data-ttu-id="34165-129">DVD 導覽器位於 DVD 停止網域中。</span><span class="sxs-lookup"><span data-stu-id="34165-129">The DVD Navigator is in the DVD Stop domain.</span></span>                         |



 

## <a name="requirements"></a><span data-ttu-id="34165-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="34165-130">Requirements</span></span>



| <span data-ttu-id="34165-131">需求</span><span class="sxs-lookup"><span data-stu-id="34165-131">Requirement</span></span> | <span data-ttu-id="34165-132">值</span><span class="sxs-lookup"><span data-stu-id="34165-132">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34165-133">版本</span><span class="sxs-lookup"><span data-stu-id="34165-133">Version</span></span><br/>   | <span data-ttu-id="34165-134">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="34165-134">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="34165-135">命名空間</span><span class="sxs-lookup"><span data-stu-id="34165-135">Namespace</span></span><br/> | <span data-ttu-id="34165-136">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="34165-136">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="34165-137">組件</span><span class="sxs-lookup"><span data-stu-id="34165-137">Assembly</span></span><br/>  | <dl> <span data-ttu-id="34165-138"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="34165-138"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="34165-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="34165-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34165-140">**AxWindowsMediaPlayer 物件 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="34165-140">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="34165-141">**IWMPDVD 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="34165-141">**IWMPDVD Interface (VB and C#)**</span></span>](iwmpdvd--vb-and-c.md)
</dt> </dl>

 

 





