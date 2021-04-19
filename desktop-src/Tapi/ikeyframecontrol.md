---
description: IKeyFrameControl 介面是由 h.264 MSP 所執行，而且只能在 h. 資料流程物件上使用。
ms.assetid: 68cb1df1-f7fa-447a-8ea5-80dc1e802760
title: 'IKeyFrameControl 介面 (H323priv .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c326c6a492777d7c41ae450a1c502c343aeb8cb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989659"
---
# <a name="ikeyframecontrol-interface"></a><span data-ttu-id="f22ab-103">IKeyFrameControl 介面</span><span class="sxs-lookup"><span data-stu-id="f22ab-103">IKeyFrameControl interface</span></span>

<span data-ttu-id="f22ab-104">\[**IKeyFrameControl** 無法在 windows Vista、windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="f22ab-104">\[**IKeyFrameControl** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="f22ab-105">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="f22ab-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="f22ab-106">**IKeyFrameControl** 介面是由 h.264 [MSP](h323-msp.md)所執行，而且只能在 h. 資料流程物件上使用。</span><span class="sxs-lookup"><span data-stu-id="f22ab-106">The **IKeyFrameControl** interface is implemented by the [H.323 MSP](h323-msp.md) and is available only on H.323 stream objects.</span></span> <span data-ttu-id="f22ab-107">此介面會公開方法，以啟用 H323 和 SDP 用戶端間通訊的終端機建立和操作。</span><span class="sxs-lookup"><span data-stu-id="f22ab-107">This interface exposes methods that enable creation and manipulation of terminals that can communicate between H323 and SDP clients.</span></span> <span data-ttu-id="f22ab-108">它有兩種方法可讓應用程式要求遠端端點以主要畫面格更新影片影像。</span><span class="sxs-lookup"><span data-stu-id="f22ab-108">It has two methods that allow the application to ask the remote endpoint to update the video image with a keyframe.</span></span>

## <a name="members"></a><span data-ttu-id="f22ab-109">成員</span><span class="sxs-lookup"><span data-stu-id="f22ab-109">Members</span></span>

<span data-ttu-id="f22ab-110">**IKeyFrameControl** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="f22ab-110">The **IKeyFrameControl** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="f22ab-111">**IKeyFrameControl** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="f22ab-111">**IKeyFrameControl** also has these types of members:</span></span>

-   [<span data-ttu-id="f22ab-112">方法</span><span class="sxs-lookup"><span data-stu-id="f22ab-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="f22ab-113">方法</span><span class="sxs-lookup"><span data-stu-id="f22ab-113">Methods</span></span>

<span data-ttu-id="f22ab-114">**IKeyFrameControl** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="f22ab-114">The **IKeyFrameControl** interface has these methods.</span></span>



| <span data-ttu-id="f22ab-115">方法</span><span class="sxs-lookup"><span data-stu-id="f22ab-115">Method</span></span>                                                                  | <span data-ttu-id="f22ab-116">描述</span><span class="sxs-lookup"><span data-stu-id="f22ab-116">Description</span></span>                                                                                 |
|:------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f22ab-117">**PeriodicUpdatePicture**</span><span class="sxs-lookup"><span data-stu-id="f22ab-117">**PeriodicUpdatePicture**</span></span>](ikeyframecontrol-periodicupdatepicture.md) | <span data-ttu-id="f22ab-118">設定資料流程中的計時器，以定期要求圖片更新。</span><span class="sxs-lookup"><span data-stu-id="f22ab-118">Configures a timer in the stream that will ask for picture updates periodically.</span></span><br/> |
| [<span data-ttu-id="f22ab-119">**UpdatePicture**</span><span class="sxs-lookup"><span data-stu-id="f22ab-119">**UpdatePicture**</span></span>](ikeyframecontrol-updatepicture.md)                 | <span data-ttu-id="f22ab-120">要求影片寄件者更新圖片。</span><span class="sxs-lookup"><span data-stu-id="f22ab-120">Asks the video sender to update the picture.</span></span><br/>                                     |



 

## <a name="requirements"></a><span data-ttu-id="f22ab-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="f22ab-121">Requirements</span></span>



| <span data-ttu-id="f22ab-122">需求</span><span class="sxs-lookup"><span data-stu-id="f22ab-122">Requirement</span></span> | <span data-ttu-id="f22ab-123">值</span><span class="sxs-lookup"><span data-stu-id="f22ab-123">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f22ab-124">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="f22ab-124">TAPI version</span></span><br/> | <span data-ttu-id="f22ab-125">需要 TAPI 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="f22ab-125">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="f22ab-126">標頭</span><span class="sxs-lookup"><span data-stu-id="f22ab-126">Header</span></span><br/>       | <dl> <span data-ttu-id="f22ab-127"><dt>H323priv。h</dt></span><span class="sxs-lookup"><span data-stu-id="f22ab-127"><dt>H323priv.h</dt></span></span> </dl> |
| <span data-ttu-id="f22ab-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="f22ab-128">Library</span></span><br/>      | <dl> <span data-ttu-id="f22ab-129"><dt>Uuid</dt></span><span class="sxs-lookup"><span data-stu-id="f22ab-129"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="f22ab-130">DLL</span><span class="sxs-lookup"><span data-stu-id="f22ab-130">DLL</span></span><br/>          | <dl> <span data-ttu-id="f22ab-131"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f22ab-131"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="f22ab-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f22ab-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f22ab-133">H323 MSP</span><span class="sxs-lookup"><span data-stu-id="f22ab-133">H323 MSP</span></span>](h323-msp.md)
</dt> </dl>

 

