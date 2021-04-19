---
description: 指定語音編解碼器的模式。
ms.assetid: 8425cdab-e43c-41ca-9c20-09ab6a5f06f4
title: 'MFPKEY_WMAVOICE_ENC_MusicSpeechClassMode 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9776c76f2a8863afe73626f5a2940de2c0ccb7cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106979038"
---
# <a name="mfpkey_wmavoice_enc_musicspeechclassmode-property"></a><span data-ttu-id="cbf49-103">MFPKEY \_ WMAVOICE \_ ENC \_ MusicSpeechClassMode 屬性</span><span class="sxs-lookup"><span data-stu-id="cbf49-103">MFPKEY\_WMAVOICE\_ENC\_MusicSpeechClassMode Property</span></span>

<span data-ttu-id="cbf49-104">指定語音編解碼器的模式。</span><span class="sxs-lookup"><span data-stu-id="cbf49-104">Specifies the mode of the voice codec.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="cbf49-105">IPropertyBag 的常數</span><span class="sxs-lookup"><span data-stu-id="cbf49-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="cbf49-106">g \_ wszWMACMusicSpeechClassMode</span><span class="sxs-lookup"><span data-stu-id="cbf49-106">g\_wszWMACMusicSpeechClassMode</span></span>

## <a name="data-type"></a><span data-ttu-id="cbf49-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="cbf49-107">Data Type</span></span>

<span data-ttu-id="cbf49-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="cbf49-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="cbf49-109">預設值</span><span class="sxs-lookup"><span data-stu-id="cbf49-109">Default Value</span></span>

<span data-ttu-id="cbf49-110">1</span><span class="sxs-lookup"><span data-stu-id="cbf49-110">1</span></span>

## <a name="remarks"></a><span data-ttu-id="cbf49-111">備註</span><span class="sxs-lookup"><span data-stu-id="cbf49-111">Remarks</span></span>

<span data-ttu-id="cbf49-112">值為1時，會通知編解碼器內容為純語音，值為2時，編解碼器會自動判斷模式，而任何其他值則會通知編解碼器使用音樂模式。</span><span class="sxs-lookup"><span data-stu-id="cbf49-112">A value of 1 informs the codec that the content is voice-only, a value of 2 has the codec determine the mode automatically, and any other value informs the codec to use music mode.</span></span>

<span data-ttu-id="cbf49-113">如果自動模式未正確地編碼混合語音和音樂，您可以使用 [MFPKEY \_ WMAVOICE \_ ENC \_ EDL](mfpkey-wmavoice-enc-edlproperty.md) 屬性指定檔案個別區段的編碼方式。</span><span class="sxs-lookup"><span data-stu-id="cbf49-113">If automatic mode is not encoding mixed voice and music properly, you can specify encoding for individual sections of the file by using the [MFPKEY\_WMAVOICE\_ENC\_EDL](mfpkey-wmavoice-enc-edlproperty.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="cbf49-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="cbf49-114">Requirements</span></span>



| <span data-ttu-id="cbf49-115">需求</span><span class="sxs-lookup"><span data-stu-id="cbf49-115">Requirement</span></span> | <span data-ttu-id="cbf49-116">值</span><span class="sxs-lookup"><span data-stu-id="cbf49-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cbf49-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cbf49-117">Minimum supported client</span></span><br/> | <span data-ttu-id="cbf49-118">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cbf49-118">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="cbf49-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cbf49-119">Minimum supported server</span></span><br/> | <span data-ttu-id="cbf49-120">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cbf49-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="cbf49-121">標頭</span><span class="sxs-lookup"><span data-stu-id="cbf49-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="cbf49-122"><dt>Wmcodecdsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="cbf49-122"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cbf49-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cbf49-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cbf49-124">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="cbf49-124">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




