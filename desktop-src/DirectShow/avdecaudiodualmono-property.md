---
description: AVDecAudioDualMono 屬性-指定雙聲道音訊是否編碼為身歷聲或雙 mono。
ms.assetid: 96cb9e17-588c-4a1a-a7ba-7f8439d5b79a
title: 'AVDecAudioDualMono 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: adc84e19d41840b358e3e79576152dbc8527e2bb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096566"
---
# <a name="avdecaudiodualmono-property"></a><span data-ttu-id="aa028-103">AVDecAudioDualMono 屬性</span><span class="sxs-lookup"><span data-stu-id="aa028-103">AVDecAudioDualMono property</span></span>

<span data-ttu-id="aa028-104">指定雙聲道音訊是否編碼為身歷聲或雙 mono。</span><span class="sxs-lookup"><span data-stu-id="aa028-104">Specifies whether 2-channel audio is encoded as stereo or dual mono.</span></span>

<span data-ttu-id="aa028-105">這是唯讀的屬性。</span><span class="sxs-lookup"><span data-stu-id="aa028-105">This property is read-only.</span></span>

## <a name="data-type"></a><span data-ttu-id="aa028-106">資料類型</span><span class="sxs-lookup"><span data-stu-id="aa028-106">Data type</span></span>

<span data-ttu-id="aa028-107">**UINT32** (**VT \_ UI4**) </span><span class="sxs-lookup"><span data-stu-id="aa028-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="aa028-108">屬性 GUID</span><span class="sxs-lookup"><span data-stu-id="aa028-108">Property GUID</span></span>

<span data-ttu-id="aa028-109">**CODECAPI \_ AVDecAudioDualMono**</span><span class="sxs-lookup"><span data-stu-id="aa028-109">**CODECAPI\_AVDecAudioDualMono**</span></span>

## <a name="property-value"></a><span data-ttu-id="aa028-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="aa028-110">Property value</span></span>

<span data-ttu-id="aa028-111">這個屬性的值是 [**eAVDecAudioDualMono**](/windows/desktop/api/codecapi/ne-codecapi-eavdecaudiodualmono) 列舉的成員。</span><span class="sxs-lookup"><span data-stu-id="aa028-111">The value of this property is a member of the [**eAVDecAudioDualMono**](/windows/desktop/api/codecapi/ne-codecapi-eavdecaudiodualmono) enumeration.</span></span>

## <a name="remarks"></a><span data-ttu-id="aa028-112">備註</span><span class="sxs-lookup"><span data-stu-id="aa028-112">Remarks</span></span>

<span data-ttu-id="aa028-113">只有當解碼器的輸入位資料流程包含雙聲道音訊時，才會套用此屬性。</span><span class="sxs-lookup"><span data-stu-id="aa028-113">This property applies only when the decoder's input bit stream contains two-channel audio.</span></span> <span data-ttu-id="aa028-114">雙聲道音訊串流可能會編碼為身歷聲或雙 mono。</span><span class="sxs-lookup"><span data-stu-id="aa028-114">A two-channel audio stream might be encoded as stereo or as dual mono.</span></span> <span data-ttu-id="aa028-115">如果音訊是雙 mono，您可以設定 [**AVDecAudioDualMonoReproMode**](avdecaudiodualmonorepromode-property.md) 屬性來設定解碼器重現音訊的方式。</span><span class="sxs-lookup"><span data-stu-id="aa028-115">If the audio is dual mono, you can set the [**AVDecAudioDualMonoReproMode**](avdecaudiodualmonorepromode-property.md) property to configure how the decoder reproduces the audio.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa028-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="aa028-116">Requirements</span></span>



| <span data-ttu-id="aa028-117">需求</span><span class="sxs-lookup"><span data-stu-id="aa028-117">Requirement</span></span> | <span data-ttu-id="aa028-118">值</span><span class="sxs-lookup"><span data-stu-id="aa028-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="aa028-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="aa028-119">Minimum supported client</span></span><br/> | <span data-ttu-id="aa028-120">Windows 2000 專業版傳統型 \[ 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="aa028-120">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="aa028-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="aa028-121">Minimum supported server</span></span><br/> | <span data-ttu-id="aa028-122">Windows 2000 Server \[ desktop 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="aa028-122">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="aa028-123">標頭</span><span class="sxs-lookup"><span data-stu-id="aa028-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="aa028-124"><dt>Codecapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="aa028-124"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa028-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="aa028-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa028-126">編解碼器 API 屬性</span><span class="sxs-lookup"><span data-stu-id="aa028-126">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="aa028-127">**ICodecAPI 介面**</span><span class="sxs-lookup"><span data-stu-id="aa028-127">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




