---
description: 指定輸出音訊內容所需的最大音量層級。
ms.assetid: 231b7296-ca80-4918-bae6-674b976db24c
title: 'MFPKEY_WMADRC_PEAKTARGET 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c40fa68e2b580c5d3e8550d6e46c9f6b9fe4bfc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974209"
---
# <a name="mfpkey_wmadrc_peaktarget-property"></a><span data-ttu-id="2bc5b-103">MFPKEY \_ WMADRC \_ PEAKTARGET 屬性</span><span class="sxs-lookup"><span data-stu-id="2bc5b-103">MFPKEY\_WMADRC\_PEAKTARGET Property</span></span>

<span data-ttu-id="2bc5b-104">指定輸出音訊內容所需的最大音量層級。</span><span class="sxs-lookup"><span data-stu-id="2bc5b-104">Specifies the desired maximum volume level of output audio content.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="2bc5b-105">IPropertyBag 的常數</span><span class="sxs-lookup"><span data-stu-id="2bc5b-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="2bc5b-106">g \_ wszWMADRCPeakTarget</span><span class="sxs-lookup"><span data-stu-id="2bc5b-106">g\_wszWMADRCPeakTarget</span></span>

## <a name="data-type"></a><span data-ttu-id="2bc5b-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="2bc5b-107">Data Type</span></span>

<span data-ttu-id="2bc5b-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="2bc5b-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="2bc5b-109">預設值</span><span class="sxs-lookup"><span data-stu-id="2bc5b-109">Default Value</span></span>

<span data-ttu-id="2bc5b-110">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="2bc5b-110">See Remarks.</span></span>

## <a name="remarks"></a><span data-ttu-id="2bc5b-111">備註</span><span class="sxs-lookup"><span data-stu-id="2bc5b-111">Remarks</span></span>

<span data-ttu-id="2bc5b-112">您可以針對動態範圍控制項的目的，在解碼器上設定此值，但只有在已設定 [MFPKEY \_ WMADEC \_ DRCMODE](mfpkey-wmadec-drcmodeproperty.md) 屬性時，才會有作用。</span><span class="sxs-lookup"><span data-stu-id="2bc5b-112">You can set this value on the decoder for the purpose of dynamic range control, but it will have an effect only if the [MFPKEY\_WMADEC\_DRCMODE](mfpkey-wmadec-drcmodeproperty.md) property is set.</span></span>

<span data-ttu-id="2bc5b-113">如果您在未設定此屬性時，從編碼器要求動態範圍控制，則編解碼器會計算預設值。</span><span class="sxs-lookup"><span data-stu-id="2bc5b-113">If you request dynamic range control from the decoder when this property is not set, the codec will compute a default value.</span></span>

<span data-ttu-id="2bc5b-114">您可以使用 [MFPKEY \_ WMADRC \_ AVGREF](mfpkey-wmadrc-avgrefproperty.md) 和 [MFPKEY \_ WMADRC \_ PEAKREF](mfpkey-wmadrc-peakrefproperty.md) 屬性來計算這個屬性的適當值。</span><span class="sxs-lookup"><span data-stu-id="2bc5b-114">Use the [MFPKEY\_WMADRC\_AVGREF](mfpkey-wmadrc-avgrefproperty.md) and [MFPKEY\_WMADRC\_PEAKREF](mfpkey-wmadrc-peakrefproperty.md) properties to compute appropriate values for this property.</span></span>

<span data-ttu-id="2bc5b-115">如需動態範圍控制的詳細資訊，請參閱 web 文章 [Windows Media 音訊 Professional 編解碼器功能](/previous-versions/ms867218(v=msdn.10))。</span><span class="sxs-lookup"><span data-stu-id="2bc5b-115">For more information on dynamic range control, see the web article [Windows Media Audio Professional Codec Features](/previous-versions/ms867218(v=msdn.10)).</span></span>

## <a name="requirements"></a><span data-ttu-id="2bc5b-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="2bc5b-116">Requirements</span></span>



| <span data-ttu-id="2bc5b-117">需求</span><span class="sxs-lookup"><span data-stu-id="2bc5b-117">Requirement</span></span> | <span data-ttu-id="2bc5b-118">值</span><span class="sxs-lookup"><span data-stu-id="2bc5b-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2bc5b-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2bc5b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="2bc5b-120">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2bc5b-120">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="2bc5b-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2bc5b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="2bc5b-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2bc5b-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2bc5b-123">標頭</span><span class="sxs-lookup"><span data-stu-id="2bc5b-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="2bc5b-124"><dt>Wmcodecdsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="2bc5b-124"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2bc5b-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2bc5b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2bc5b-126">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="2bc5b-126">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
