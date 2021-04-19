---
description: 當出現無線封包時發生。
ms.assetid: 30bc423d-0642-4515-9e51-a8b8b36aecad
title: 'InkPicture. NewInAirPackets 事件 (Msinkaut .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0331eb4e855e2051cd8b2b6d7b312d7f32e76096
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106989474"
---
# <a name="inkpicturenewinairpackets-event"></a><span data-ttu-id="1dce9-103">InkPicture. NewInAirPackets 事件</span><span class="sxs-lookup"><span data-stu-id="1dce9-103">InkPicture.NewInAirPackets event</span></span>

<span data-ttu-id="1dce9-104">當出現無線封包時發生。</span><span class="sxs-lookup"><span data-stu-id="1dce9-104">Occurs when an in-air packet is seen.</span></span>

## <a name="syntax"></a><span data-ttu-id="1dce9-105">語法</span><span class="sxs-lookup"><span data-stu-id="1dce9-105">Syntax</span></span>


```C++
void NewInAirPackets(
  [in]      IInkCursor *Cursor,
  [in]      long       PacketCount,
  [in, out] VARIANT    *PacketData
);
```



## <a name="parameters"></a><span data-ttu-id="1dce9-106">參數</span><span class="sxs-lookup"><span data-stu-id="1dce9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1dce9-107">資料 *指標* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1dce9-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1dce9-108">產生 **NewInAirPackets** 事件的 [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)物件。</span><span class="sxs-lookup"><span data-stu-id="1dce9-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the **NewInAirPackets** event.</span></span>

</dd> <dt>

<span data-ttu-id="1dce9-109">*PacketCount* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1dce9-109">*PacketCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1dce9-110">收到的無線封包數目。</span><span class="sxs-lookup"><span data-stu-id="1dce9-110">The number of in-air packets received.</span></span>

</dd> <dt>

<span data-ttu-id="1dce9-111">*PacketData* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="1dce9-111">*PacketData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1dce9-112">陣列，其中包含所選取的封包資料。</span><span class="sxs-lookup"><span data-stu-id="1dce9-112">An array that contains the selected data for the packet.</span></span>

<span data-ttu-id="1dce9-113">如需 VARIANT 結構的詳細資訊，請參閱 [使用 COM 程式庫](using-the-com-library.md)。</span><span class="sxs-lookup"><span data-stu-id="1dce9-113">For more information about the VARIANT structure, see [Using the COM Library](using-the-com-library.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1dce9-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="1dce9-114">Return value</span></span>

<span data-ttu-id="1dce9-115">此事件不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="1dce9-115">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1dce9-116">備註</span><span class="sxs-lookup"><span data-stu-id="1dce9-116">Remarks</span></span>

<span data-ttu-id="1dce9-117">當使用者將畫筆移近 tablet，而游標位於筆墨收集器物件的視窗內，或使用者在筆跡收集器物件的相關視窗內移動滑鼠時，就會建立無線封包。</span><span class="sxs-lookup"><span data-stu-id="1dce9-117">An in-air packet is created when a user moves a pen near the tablet and the cursor is within the ink collector object's window or the user moves a mouse within the ink collector object's associated window.</span></span> <span data-ttu-id="1dce9-118">**NewInAirPackets** 事件會快速產生，而事件處理常式必須快速或效能受到影響。</span><span class="sxs-lookup"><span data-stu-id="1dce9-118">**NewInAirPackets** events are generated rapidly, and the event handler must be fast or performance suffers.</span></span>

<span data-ttu-id="1dce9-119">此事件方法是在 **\_ IInkCollectorEvents**、 **\_ IInkOverlayEvents** 和 **\_ IInkPictureEvents** 分派專用介面中定義， (具有 DISPID ICENewInAirPackets 識別碼的) \_ 。</span><span class="sxs-lookup"><span data-stu-id="1dce9-119">This event method is defined in the **\_IInkCollectorEvents**, **\_IInkOverlayEvents**, and **\_IInkPictureEvents** dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICENewInAirPackets.</span></span>

<span data-ttu-id="1dce9-120">即使在選取或清除模式下，也不只是在插入筆墨時，也會引發 **NewInAirPackets** 事件。</span><span class="sxs-lookup"><span data-stu-id="1dce9-120">The **NewInAirPackets** event is fired even when in select or erase mode, not just when inserting ink.</span></span> <span data-ttu-id="1dce9-121">這需要您監視編輯模式 (您負責設定) 並在解讀事件之前留意模式。</span><span class="sxs-lookup"><span data-stu-id="1dce9-121">This requires that you monitor the editing mode (which you are responsible for setting) and be aware of the mode before interpreting the event.</span></span> <span data-ttu-id="1dce9-122">這項需求的優點是透過更清楚地瞭解平臺事件，更能自由地在平臺上進行創新。</span><span class="sxs-lookup"><span data-stu-id="1dce9-122">The advantage of this requirement is greater freedom to innovate on the platform through greater awareness of platform events.</span></span>

<span data-ttu-id="1dce9-123">若要設定包含在此陣列中的屬性，請使用筆墨收集器物件的 [**DesiredPacketDescription**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_desiredpacketdescription) 屬性。</span><span class="sxs-lookup"><span data-stu-id="1dce9-123">To set which properties are contained in this array, use the [**DesiredPacketDescription**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_desiredpacketdescription) property of the ink collector object.</span></span> <span data-ttu-id="1dce9-124">*PacketData* 參數傳回的陣列包含這些屬性的資料。</span><span class="sxs-lookup"><span data-stu-id="1dce9-124">The array that the *PacketData* parameter returns contains the data for those properties.</span></span>

> [!Note]  
> <span data-ttu-id="1dce9-125">雖然您可以修改封包資料，但不會保存或使用這些修改。</span><span class="sxs-lookup"><span data-stu-id="1dce9-125">Although you can modify the packet data, these modifications are not persisted or used.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="1dce9-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="1dce9-126">Requirements</span></span>



| <span data-ttu-id="1dce9-127">需求</span><span class="sxs-lookup"><span data-stu-id="1dce9-127">Requirement</span></span> | <span data-ttu-id="1dce9-128">值</span><span class="sxs-lookup"><span data-stu-id="1dce9-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1dce9-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1dce9-129">Minimum supported client</span></span><br/> | <span data-ttu-id="1dce9-130">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1dce9-130">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="1dce9-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1dce9-131">Minimum supported server</span></span><br/> | <span data-ttu-id="1dce9-132">都不支援</span><span class="sxs-lookup"><span data-stu-id="1dce9-132">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="1dce9-133">標頭</span><span class="sxs-lookup"><span data-stu-id="1dce9-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="1dce9-134"><dt>Msinkaut (也需要 Msinkaut \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="1dce9-134"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="1dce9-135">程式庫</span><span class="sxs-lookup"><span data-stu-id="1dce9-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="1dce9-136"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1dce9-136"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="1dce9-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1dce9-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1dce9-138">InkPicture</span><span class="sxs-lookup"><span data-stu-id="1dce9-138">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> <dt>

[<span data-ttu-id="1dce9-139">**DesiredPacketDescription 屬性**</span><span class="sxs-lookup"><span data-stu-id="1dce9-139">**DesiredPacketDescription Property**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_desiredpacketdescription)
</dt> <dt>

[<span data-ttu-id="1dce9-140">**NewPackets 事件**</span><span class="sxs-lookup"><span data-stu-id="1dce9-140">**NewPackets Event**</span></span>](inkpicture-newpackets.md)
</dt> <dt>

[<span data-ttu-id="1dce9-141">**IInkCursor 介面**</span><span class="sxs-lookup"><span data-stu-id="1dce9-141">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> </dl>

 

 




