---
description: InkPicture. NewPackets 事件-當筆墨收集器收到封包時發生。
ms.assetid: 7d120198-c016-4452-b8a8-22c4ad87d526
title: 'InkPicture. NewPackets 事件 (Msinkaut .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 194fb9bffae07cca561fbfc11ff8a185d63bb9e6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086476"
---
# <a name="inkpicturenewpackets-event"></a><span data-ttu-id="efe66-103">InkPicture. NewPackets 事件</span><span class="sxs-lookup"><span data-stu-id="efe66-103">InkPicture.NewPackets event</span></span>

<span data-ttu-id="efe66-104">當筆墨收集器收到封包時發生。</span><span class="sxs-lookup"><span data-stu-id="efe66-104">Occurs when the ink collector receives a packet.</span></span>

## <a name="syntax"></a><span data-ttu-id="efe66-105">語法</span><span class="sxs-lookup"><span data-stu-id="efe66-105">Syntax</span></span>


```C++
void NewPackets(
  [in]      IInkCursor     *Cursor,
  [in]      IInkStrokeDisp *Stroke,
  [in]      long           PacketCount,
  [in, out] VARIANT        *PacketData
);
```



## <a name="parameters"></a><span data-ttu-id="efe66-106">參數</span><span class="sxs-lookup"><span data-stu-id="efe66-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="efe66-107">資料 *指標* \[在\]</span><span class="sxs-lookup"><span data-stu-id="efe66-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="efe66-108">產生 [**NewInAirPackets**](inkpicture-newinairpackets.md)事件的 [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)物件。</span><span class="sxs-lookup"><span data-stu-id="efe66-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the [**NewInAirPackets**](inkpicture-newinairpackets.md) event.</span></span>

</dd> <dt>

<span data-ttu-id="efe66-109">*筆觸* \[在\]</span><span class="sxs-lookup"><span data-stu-id="efe66-109">*Stroke* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="efe66-110">[**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)物件。</span><span class="sxs-lookup"><span data-stu-id="efe66-110">The [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object.</span></span>

</dd> <dt>

<span data-ttu-id="efe66-111">*PacketCount* \[在\]</span><span class="sxs-lookup"><span data-stu-id="efe66-111">*PacketCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="efe66-112">針對 [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) 物件接收的封包數目。</span><span class="sxs-lookup"><span data-stu-id="efe66-112">The number of packets received for a [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object.</span></span>

</dd> <dt>

<span data-ttu-id="efe66-113">*PacketData* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="efe66-113">*PacketData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="efe66-114">陣列，其中包含所選取的封包資料。</span><span class="sxs-lookup"><span data-stu-id="efe66-114">An array that contains the selected data for the packet.</span></span>

<span data-ttu-id="efe66-115">如需 VARIANT 結構的詳細資訊，請參閱 [使用 COM 程式庫](using-the-com-library.md)。</span><span class="sxs-lookup"><span data-stu-id="efe66-115">For more information about the VARIANT structure, see [Using the COM Library](using-the-com-library.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="efe66-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="efe66-116">Return value</span></span>

<span data-ttu-id="efe66-117">此事件不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="efe66-117">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="efe66-118">備註</span><span class="sxs-lookup"><span data-stu-id="efe66-118">Remarks</span></span>

<span data-ttu-id="efe66-119">在收集筆劃時接收封包。</span><span class="sxs-lookup"><span data-stu-id="efe66-119">Packets are received while a stroke is being collected.</span></span> <span data-ttu-id="efe66-120">封包事件會快速發生，且 **NewPackets** 事件處理常式必須快速或效能受到影響。</span><span class="sxs-lookup"><span data-stu-id="efe66-120">Packet events occur rapidly, and a **NewPackets** event handler must be fast or performance suffers.</span></span>

<span data-ttu-id="efe66-121">此事件方法是在 **\_ IInkCollectorEvents**、 **\_ IInkOverlayEvents** 和 **\_ IInkPictureEvents** 分派專用介面中定義， (具有 DISPID ICENewPackets 識別碼的) \_ 。</span><span class="sxs-lookup"><span data-stu-id="efe66-121">This event method is defined in the **\_IInkCollectorEvents**, **\_IInkOverlayEvents**, and **\_IInkPictureEvents** dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICENewPackets.</span></span>

<span data-ttu-id="efe66-122">應謹慎使用這個事件，因為在事件處理常式中執行太多程式碼時，可能會對筆墨效能造成負面影響。</span><span class="sxs-lookup"><span data-stu-id="efe66-122">This event should be used carefully as it could have an adverse effect on ink performance if too much code is executed in the event handlers.</span></span>

<span data-ttu-id="efe66-123">若要設定包含在此陣列中的屬性，請使用筆墨收集器物件的 [**DesiredPacketDescription**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_desiredpacketdescription) 屬性。</span><span class="sxs-lookup"><span data-stu-id="efe66-123">To set which properties are contained in this array, use the [**DesiredPacketDescription**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_desiredpacketdescription) property of the ink collector object.</span></span> <span data-ttu-id="efe66-124">*PacketData* 參數傳回的陣列包含這些屬性的資料。</span><span class="sxs-lookup"><span data-stu-id="efe66-124">The array that the *PacketData* parameter returns contains the data for those properties.</span></span>

> [!Note]  
> <span data-ttu-id="efe66-125">雖然您可以修改封包資料，但不會保存或使用這些修改。</span><span class="sxs-lookup"><span data-stu-id="efe66-125">Although you can modify the packet data, these modifications are not persisted or used.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="efe66-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="efe66-126">Requirements</span></span>



| <span data-ttu-id="efe66-127">需求</span><span class="sxs-lookup"><span data-stu-id="efe66-127">Requirement</span></span> | <span data-ttu-id="efe66-128">值</span><span class="sxs-lookup"><span data-stu-id="efe66-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="efe66-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="efe66-129">Minimum supported client</span></span><br/> | <span data-ttu-id="efe66-130">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="efe66-130">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="efe66-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="efe66-131">Minimum supported server</span></span><br/> | <span data-ttu-id="efe66-132">都不支援</span><span class="sxs-lookup"><span data-stu-id="efe66-132">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="efe66-133">標頭</span><span class="sxs-lookup"><span data-stu-id="efe66-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="efe66-134"><dt>Msinkaut (也需要 Msinkaut \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="efe66-134"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="efe66-135">程式庫</span><span class="sxs-lookup"><span data-stu-id="efe66-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="efe66-136"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="efe66-136"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="efe66-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="efe66-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="efe66-138">InkPicture</span><span class="sxs-lookup"><span data-stu-id="efe66-138">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> <dt>

[<span data-ttu-id="efe66-139">**NewInAirPackets 事件**</span><span class="sxs-lookup"><span data-stu-id="efe66-139">**NewInAirPackets Event**</span></span>](inkpicture-newinairpackets.md)
</dt> <dt>

[<span data-ttu-id="efe66-140">**IInkCursor 介面**</span><span class="sxs-lookup"><span data-stu-id="efe66-140">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[<span data-ttu-id="efe66-141">**IInkStrokeDisp 介面**</span><span class="sxs-lookup"><span data-stu-id="efe66-141">**IInkStrokeDisp Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

 




