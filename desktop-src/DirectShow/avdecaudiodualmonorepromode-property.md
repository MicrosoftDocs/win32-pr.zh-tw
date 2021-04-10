---
description: 指定解碼器如何重現雙重 mono 音訊。
ms.assetid: 3ef1f52c-13b2-4d9f-99fe-3317846be8a0
title: 'AVDecAudioDualMonoReproMode 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a71ebe7e003b2dc4b6eebc30901525ffb918a9a9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103688219"
---
# <a name="avdecaudiodualmonorepromode-property"></a><span data-ttu-id="4f50d-103">AVDecAudioDualMonoReproMode 屬性</span><span class="sxs-lookup"><span data-stu-id="4f50d-103">AVDecAudioDualMonoReproMode property</span></span>

<span data-ttu-id="4f50d-104">指定解碼器如何重現雙重 mono 音訊。</span><span class="sxs-lookup"><span data-stu-id="4f50d-104">Specifies how the decoder reproduces dual mono audio.</span></span>

<span data-ttu-id="4f50d-105">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="4f50d-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="4f50d-106">資料類型</span><span class="sxs-lookup"><span data-stu-id="4f50d-106">Data type</span></span>

<span data-ttu-id="4f50d-107">**UINT32** (**VT \_ UI4**) </span><span class="sxs-lookup"><span data-stu-id="4f50d-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="4f50d-108">屬性 GUID</span><span class="sxs-lookup"><span data-stu-id="4f50d-108">Property GUID</span></span>

<span data-ttu-id="4f50d-109">**CODECAPI \_ AVDecAudioDualMonoReproMode**</span><span class="sxs-lookup"><span data-stu-id="4f50d-109">**CODECAPI\_AVDecAudioDualMonoReproMode**</span></span>

## <a name="property-value"></a><span data-ttu-id="4f50d-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="4f50d-110">Property value</span></span>

<span data-ttu-id="4f50d-111">這個屬性的值是 [**eAVDecAudioDualMonoReproMode**](/windows/desktop/api/codecapi/ne-codecapi-eavdecaudiodualmonorepromode) 列舉的成員。</span><span class="sxs-lookup"><span data-stu-id="4f50d-111">The value of this property is a member of the [**eAVDecAudioDualMonoReproMode**](/windows/desktop/api/codecapi/ne-codecapi-eavdecaudiodualmonorepromode) enumeration.</span></span>

## <a name="remarks"></a><span data-ttu-id="4f50d-112">備註</span><span class="sxs-lookup"><span data-stu-id="4f50d-112">Remarks</span></span>

<span data-ttu-id="4f50d-113">只有當解碼器的輸入位資料流程包含雙重 mono 音訊時，才會套用此屬性。</span><span class="sxs-lookup"><span data-stu-id="4f50d-113">This properties applies only when the decoder's input bit stream contains dual mono audio.</span></span> <span data-ttu-id="4f50d-114">若要測試這種情況，請取得 [AVDecAudioDualMono](avdecaudiodualmono-property.md) 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="4f50d-114">To test this condition, get the value of the [AVDecAudioDualMono](avdecaudiodualmono-property.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="4f50d-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="4f50d-115">Requirements</span></span>



| <span data-ttu-id="4f50d-116">需求</span><span class="sxs-lookup"><span data-stu-id="4f50d-116">Requirement</span></span> | <span data-ttu-id="4f50d-117">值</span><span class="sxs-lookup"><span data-stu-id="4f50d-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4f50d-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4f50d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="4f50d-119">Windows 2000 專業版傳統型 \[ 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4f50d-119">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="4f50d-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4f50d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="4f50d-121">Windows 2000 Server \[ desktop 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4f50d-121">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="4f50d-122">標頭</span><span class="sxs-lookup"><span data-stu-id="4f50d-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="4f50d-123"><dt>Codecapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="4f50d-123"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f50d-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4f50d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f50d-125">編解碼器 API 屬性</span><span class="sxs-lookup"><span data-stu-id="4f50d-125">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="4f50d-126">**ICodecAPI 介面**</span><span class="sxs-lookup"><span data-stu-id="4f50d-126">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




