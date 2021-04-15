---
description: 指定杜比數位音訊解碼器的身歷聲 downmix 模式。
ms.assetid: 270893C6-8B44-4A4D-AE2B-2E58E260F649
title: 'CODECAPI_AVDecDDStereoDownMixMode 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de7caaed1af804e22b3ec6085241746bdf01eb7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104386046"
---
# <a name="codecapi_avdecddstereodownmixmode-property"></a><span data-ttu-id="38292-103">CODECAPI \_ AVDecDDStereoDownMixMode 屬性</span><span class="sxs-lookup"><span data-stu-id="38292-103">CODECAPI\_AVDecDDStereoDownMixMode property</span></span>

<span data-ttu-id="38292-104">指定杜比數位音訊解碼器的身歷聲 downmix 模式。</span><span class="sxs-lookup"><span data-stu-id="38292-104">Specifies the stereo downmix mode for a Dolby Digital audio decoder.</span></span>

## <a name="data-type"></a><span data-ttu-id="38292-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="38292-105">Data type</span></span>

<span data-ttu-id="38292-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="38292-106">**UINT32**</span></span>

## <a name="property-guid"></a><span data-ttu-id="38292-107">屬性 GUID</span><span class="sxs-lookup"><span data-stu-id="38292-107">Property GUID</span></span>

<span data-ttu-id="38292-108">**CODECAPI \_ AVDecDDStereoDownMixMode**</span><span class="sxs-lookup"><span data-stu-id="38292-108">**CODECAPI\_AVDecDDStereoDownMixMode**</span></span>

## <a name="property-value"></a><span data-ttu-id="38292-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="38292-109">Property value</span></span>

<span data-ttu-id="38292-110">這個屬性的值是 [**eAVDecDDStereoDownMixMode**](/windows/win32/api/codecapi/ne-codecapi-eavdecddstereodownmixmode) 列舉的成員。</span><span class="sxs-lookup"><span data-stu-id="38292-110">The value of this property is a member of the [**eAVDecDDStereoDownMixMode**](/windows/win32/api/codecapi/ne-codecapi-eavdecddstereodownmixmode) enumeration.</span></span>

## <a name="remarks"></a><span data-ttu-id="38292-111">備註</span><span class="sxs-lookup"><span data-stu-id="38292-111">Remarks</span></span>

<span data-ttu-id="38292-112">當對解碼器的輸入是多通道 PCM 音訊，且輸出為身歷聲音訊時，會套用此屬性。</span><span class="sxs-lookup"><span data-stu-id="38292-112">This attribute applies when the input to the decoder is multichannel PCM audio, and the output is stereo audio.</span></span>

## <a name="requirements"></a><span data-ttu-id="38292-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="38292-113">Requirements</span></span>



| <span data-ttu-id="38292-114">需求</span><span class="sxs-lookup"><span data-stu-id="38292-114">Requirement</span></span> | <span data-ttu-id="38292-115">值</span><span class="sxs-lookup"><span data-stu-id="38292-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="38292-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="38292-116">Minimum supported client</span></span><br/> | <span data-ttu-id="38292-117">Windows 8 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="38292-117">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="38292-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="38292-118">Minimum supported server</span></span><br/> | <span data-ttu-id="38292-119">Windows Server 2012 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="38292-119">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="38292-120">標頭</span><span class="sxs-lookup"><span data-stu-id="38292-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="38292-121"><dt>Codecapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="38292-121"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="38292-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="38292-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38292-123">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="38292-123">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="38292-124">**ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="38292-124">**ICodecAPI**</span></span>](/windows/desktop/api/strmif/nn-strmif-icodecapi)
</dt> </dl>

 

