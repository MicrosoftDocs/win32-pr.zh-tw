---
description: 啟用或停用音訊解碼器或數位訊號處理器 (DSP) 的說話者填滿。
ms.assetid: 5a42d4c9-d593-4d7f-bfee-37271c48e5cf
title: 'AVDSPSpeakerFill 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16bcdda053439b76c9445f2f9c866ee26afb4858
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106966622"
---
# <a name="avdspspeakerfill-property"></a><span data-ttu-id="317fc-103">AVDSPSpeakerFill 屬性</span><span class="sxs-lookup"><span data-stu-id="317fc-103">AVDSPSpeakerFill property</span></span>

<span data-ttu-id="317fc-104">啟用或停用音訊解碼器或數位訊號處理器 (DSP) 的說話者填滿。</span><span class="sxs-lookup"><span data-stu-id="317fc-104">Enables or disables speaker fill in an audio decoder or digital signal processor (DSP).</span></span>

<span data-ttu-id="317fc-105">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="317fc-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="317fc-106">資料類型</span><span class="sxs-lookup"><span data-stu-id="317fc-106">Data type</span></span>

<span data-ttu-id="317fc-107">**UINT32** (**VT \_ UI4**) </span><span class="sxs-lookup"><span data-stu-id="317fc-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="317fc-108">屬性 GUID</span><span class="sxs-lookup"><span data-stu-id="317fc-108">Property GUID</span></span>

<span data-ttu-id="317fc-109">**CODECAPI \_ AVDSPSpeakerFill**</span><span class="sxs-lookup"><span data-stu-id="317fc-109">**CODECAPI\_AVDSPSpeakerFill**</span></span>

## <a name="property-value"></a><span data-ttu-id="317fc-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="317fc-110">Property value</span></span>

<span data-ttu-id="317fc-111">這個屬性的值是 [**eAVDSPSpeakerFill**](/windows/desktop/api/codecapi/ne-codecapi-eavdspspeakerfill) 列舉的成員。</span><span class="sxs-lookup"><span data-stu-id="317fc-111">The value of this property is a member of the [**eAVDSPSpeakerFill**](/windows/desktop/api/codecapi/ne-codecapi-eavdspspeakerfill) enumeration.</span></span>

## <a name="remarks"></a><span data-ttu-id="317fc-112">備註</span><span class="sxs-lookup"><span data-stu-id="317fc-112">Remarks</span></span>

<span data-ttu-id="317fc-113">說話者填滿是將 mono 或身歷聲音訊轉換成多頻道音訊的 DSP 流程。</span><span class="sxs-lookup"><span data-stu-id="317fc-113">Speaker fill is a DSP process that converts mono or stereo audio into multichannel audio.</span></span>

## <a name="requirements"></a><span data-ttu-id="317fc-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="317fc-114">Requirements</span></span>



| <span data-ttu-id="317fc-115">需求</span><span class="sxs-lookup"><span data-stu-id="317fc-115">Requirement</span></span> | <span data-ttu-id="317fc-116">值</span><span class="sxs-lookup"><span data-stu-id="317fc-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="317fc-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="317fc-117">Minimum supported client</span></span><br/> | <span data-ttu-id="317fc-118">Windows 2000 專業版傳統型 \[ 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="317fc-118">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="317fc-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="317fc-119">Minimum supported server</span></span><br/> | <span data-ttu-id="317fc-120">Windows 2000 Server \[ desktop 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="317fc-120">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="317fc-121">標頭</span><span class="sxs-lookup"><span data-stu-id="317fc-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="317fc-122"><dt>Codecapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="317fc-122"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="317fc-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="317fc-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="317fc-124">編解碼器 API 屬性</span><span class="sxs-lookup"><span data-stu-id="317fc-124">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="317fc-125">**ICodecAPI 介面**</span><span class="sxs-lookup"><span data-stu-id="317fc-125">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




