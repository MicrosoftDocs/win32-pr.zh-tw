---
description: LINEMEDIACONTROL \_ 位旗標常數描述一組媒體資料流程的一般作業。
ms.assetid: 1e8aeda8-2810-462a-bfba-0296d854d9aa
title: 'LINEMEDIACONTROL_ 的常數 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3241a3b5f4f8a0363f30ce7aefaded0c63fc4189
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976173"
---
# <a name="linemediacontrol_-constants"></a><span data-ttu-id="ab8e7-103">LINEMEDIACONTROL \_ 常數</span><span class="sxs-lookup"><span data-stu-id="ab8e7-103">LINEMEDIACONTROL\_ Constants</span></span>

<span data-ttu-id="ab8e7-104">**LINEMEDIACONTROL \_** 位旗標常數描述一組媒體資料流程的一般作業。</span><span class="sxs-lookup"><span data-stu-id="ab8e7-104">The **LINEMEDIACONTROL\_** bit-flag constants describe a set of generic operations on media streams.</span></span> <span data-ttu-id="ab8e7-105">這些解釋是由媒體資料流程所決定。</span><span class="sxs-lookup"><span data-stu-id="ab8e7-105">The interpretations are determined by the media stream.</span></span> <span data-ttu-id="ab8e7-106">線路裝置必須具有媒體控制功能，任何媒體控制作業都能有效運作。</span><span class="sxs-lookup"><span data-stu-id="ab8e7-106">The line device must have the media-control capability for any media-control operation to be effective.</span></span>

<dl> <dt>

<span data-ttu-id="ab8e7-107"><span id="LINEMEDIACONTROL_NONE"></span><span id="linemediacontrol_none"></span>**LINEMEDIACONTROL \_ 無**</span><span class="sxs-lookup"><span data-stu-id="ab8e7-107"><span id="LINEMEDIACONTROL_NONE"></span><span id="linemediacontrol_none"></span>**LINEMEDIACONTROL\_NONE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ab8e7-108">媒體資料流程不會進行任何變更。</span><span class="sxs-lookup"><span data-stu-id="ab8e7-108">No change is to be made to the media stream.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ab8e7-109"><span id="LINEMEDIACONTROL_PAUSE"></span><span id="linemediacontrol_pause"></span>**LINEMEDIACONTROL \_ 暫停**</span><span class="sxs-lookup"><span data-stu-id="ab8e7-109"><span id="LINEMEDIACONTROL_PAUSE"></span><span id="linemediacontrol_pause"></span>**LINEMEDIACONTROL\_PAUSE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ab8e7-110">暫時暫停媒體串流。</span><span class="sxs-lookup"><span data-stu-id="ab8e7-110">Temporarily pause the media stream.</span></span>

<span data-ttu-id="ab8e7-111">媒體資料流程的速度會恢復正常。</span><span class="sxs-lookup"><span data-stu-id="ab8e7-111">The speed of the media stream is returned to normal.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ab8e7-112"><span id="LINEMEDIACONTROL_RATEDOWN"></span><span id="linemediacontrol_ratedown"></span>**LINEMEDIACONTROL \_ RATEDOWN**</span><span class="sxs-lookup"><span data-stu-id="ab8e7-112"><span id="LINEMEDIACONTROL_RATEDOWN"></span><span id="linemediacontrol_ratedown"></span>**LINEMEDIACONTROL\_RATEDOWN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ab8e7-113">媒體資料流程的速度會隨著部分資料流程定義數量而減少。</span><span class="sxs-lookup"><span data-stu-id="ab8e7-113">The speed of the media stream is decreased by some stream-defined quantity.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ab8e7-114"><span id="LINEMEDIACONTROL_RATENORMAL"></span><span id="linemediacontrol_ratenormal"></span>**LINEMEDIACONTROL \_ RATENORMAL**</span><span class="sxs-lookup"><span data-stu-id="ab8e7-114"><span id="LINEMEDIACONTROL_RATENORMAL"></span><span id="linemediacontrol_ratenormal"></span>**LINEMEDIACONTROL\_RATENORMAL**</span></span>
</dt> <dd> <dl> <dt>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ab8e7-115"><span id="LINEMEDIACONTROL_RATEUP"></span><span id="linemediacontrol_rateup"></span>**LINEMEDIACONTROL \_ RATEUP**</span><span class="sxs-lookup"><span data-stu-id="ab8e7-115"><span id="LINEMEDIACONTROL_RATEUP"></span><span id="linemediacontrol_rateup"></span>**LINEMEDIACONTROL\_RATEUP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ab8e7-116">媒體資料流程的速度會隨著部分資料流程定義數量而增加。</span><span class="sxs-lookup"><span data-stu-id="ab8e7-116">The speed of the media stream is increased by some stream-defined quantity.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ab8e7-117"><span id="LINEMEDIACONTROL_RESET"></span><span id="linemediacontrol_reset"></span>**LINEMEDIACONTROL \_ 重設**</span><span class="sxs-lookup"><span data-stu-id="ab8e7-117"><span id="LINEMEDIACONTROL_RESET"></span><span id="linemediacontrol_reset"></span>**LINEMEDIACONTROL\_RESET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ab8e7-118">重設媒體資料流程。</span><span class="sxs-lookup"><span data-stu-id="ab8e7-118">Reset the media stream.</span></span> <span data-ttu-id="ab8e7-119">相當於輸入結尾。</span><span class="sxs-lookup"><span data-stu-id="ab8e7-119">Equivalent to an end-of-input.</span></span> <span data-ttu-id="ab8e7-120">釋放所有緩衝區。</span><span class="sxs-lookup"><span data-stu-id="ab8e7-120">All buffers are released.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ab8e7-121"><span id="LINEMEDIACONTROL_RESUME"></span><span id="linemediacontrol_resume"></span>**LINEMEDIACONTROL \_ RESUME**</span><span class="sxs-lookup"><span data-stu-id="ab8e7-121"><span id="LINEMEDIACONTROL_RESUME"></span><span id="linemediacontrol_resume"></span>**LINEMEDIACONTROL\_RESUME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ab8e7-122">繼續已暫停的媒體串流。</span><span class="sxs-lookup"><span data-stu-id="ab8e7-122">Resume a paused media stream.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ab8e7-123"><span id="LINEMEDIACONTROL_START"></span><span id="linemediacontrol_start"></span>**LINEMEDIACONTROL \_ 開始**</span><span class="sxs-lookup"><span data-stu-id="ab8e7-123"><span id="LINEMEDIACONTROL_START"></span><span id="linemediacontrol_start"></span>**LINEMEDIACONTROL\_START**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ab8e7-124">啟動媒體資料流程。</span><span class="sxs-lookup"><span data-stu-id="ab8e7-124">Start the media stream.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ab8e7-125"><span id="LINEMEDIACONTROL_VOLUMEDOWN"></span><span id="linemediacontrol_volumedown"></span>**LINEMEDIACONTROL \_ VOLUMEDOWN**</span><span class="sxs-lookup"><span data-stu-id="ab8e7-125"><span id="LINEMEDIACONTROL_VOLUMEDOWN"></span><span id="linemediacontrol_volumedown"></span>**LINEMEDIACONTROL\_VOLUMEDOWN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ab8e7-126">媒體資料流程的波幅會依部分資料流程定義數量而減少。</span><span class="sxs-lookup"><span data-stu-id="ab8e7-126">The amplitude of the media stream is decreased by some stream-defined quantity.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ab8e7-127"><span id="LINEMEDIACONTROL_VOLUMENORMAL"></span><span id="linemediacontrol_volumenormal"></span>**LINEMEDIACONTROL \_ VOLUMENORMAL**</span><span class="sxs-lookup"><span data-stu-id="ab8e7-127"><span id="LINEMEDIACONTROL_VOLUMENORMAL"></span><span id="linemediacontrol_volumenormal"></span>**LINEMEDIACONTROL\_VOLUMENORMAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ab8e7-128">媒體資料流程的波幅會恢復正常。</span><span class="sxs-lookup"><span data-stu-id="ab8e7-128">The amplitude of the media stream is returned to normal.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ab8e7-129"><span id="LINEMEDIACONTROL_VOLUMEUP"></span><span id="linemediacontrol_volumeup"></span>**LINEMEDIACONTROL \_ VOLUMEUP**</span><span class="sxs-lookup"><span data-stu-id="ab8e7-129"><span id="LINEMEDIACONTROL_VOLUMEUP"></span><span id="linemediacontrol_volumeup"></span>**LINEMEDIACONTROL\_VOLUMEUP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ab8e7-130">媒體資料流程的波幅會依部分資料流程定義數量來增加。</span><span class="sxs-lookup"><span data-stu-id="ab8e7-130">The amplitude of the media stream is increased by some stream-defined quantity.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ab8e7-131">備註</span><span class="sxs-lookup"><span data-stu-id="ab8e7-131">Remarks</span></span>

<span data-ttu-id="ab8e7-132">您可以為裝置專屬的延伸模組指派高序位16位。</span><span class="sxs-lookup"><span data-stu-id="ab8e7-132">The high-order 16 bits can be assigned for device-specific extensions.</span></span> <span data-ttu-id="ab8e7-133">低序位16位是保留的。</span><span class="sxs-lookup"><span data-stu-id="ab8e7-133">The low-order 16 bits are reserved.</span></span>

<span data-ttu-id="ab8e7-134">提供媒體控制項來改善媒體資料流程上動作的效能，以回應電話語音相關事件。</span><span class="sxs-lookup"><span data-stu-id="ab8e7-134">Media control is provided to improve performance of actions on media streams in response to telephony-related events.</span></span> <span data-ttu-id="ab8e7-135">應用程式通常應該透過媒體專屬的 API 來管理媒體串流。</span><span class="sxs-lookup"><span data-stu-id="ab8e7-135">The application should normally manage a media stream through the media-specific API.</span></span> <span data-ttu-id="ab8e7-136">此處提供的媒體控制功能不適合用來取代原生媒體 Api。</span><span class="sxs-lookup"><span data-stu-id="ab8e7-136">The media-control functionality provided here is not intended to replace the native media APIs.</span></span>

<span data-ttu-id="ab8e7-137">媒體控制動作可以與數位偵測、聲音偵測、轉換成通話狀態，以及偵測媒體類型相關聯。</span><span class="sxs-lookup"><span data-stu-id="ab8e7-137">Media-control actions can be associated with the detection of digits, the detection of tones, the transition into a call state, and the detection of a media type.</span></span> <span data-ttu-id="ab8e7-138">請參閱行的裝置功能，以判斷是否可在線上使用媒體控制項。</span><span class="sxs-lookup"><span data-stu-id="ab8e7-138">Consult a line's device capabilities to determine whether media control is available on the line.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab8e7-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="ab8e7-139">Requirements</span></span>



| <span data-ttu-id="ab8e7-140">需求</span><span class="sxs-lookup"><span data-stu-id="ab8e7-140">Requirement</span></span> | <span data-ttu-id="ab8e7-141">值</span><span class="sxs-lookup"><span data-stu-id="ab8e7-141">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="ab8e7-142">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="ab8e7-142">TAPI version</span></span><br/> | <span data-ttu-id="ab8e7-143">需要 TAPI 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="ab8e7-143">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="ab8e7-144">標頭</span><span class="sxs-lookup"><span data-stu-id="ab8e7-144">Header</span></span><br/>       | <dl> <span data-ttu-id="ab8e7-145"><dt>Tapi</dt></span><span class="sxs-lookup"><span data-stu-id="ab8e7-145"><dt>Tapi.h</dt></span></span> </dl> |



 

 




