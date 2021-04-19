---
description: 指定在解碼檔案之後，可能會傳回的額外 PCM 樣本數上限。
ms.assetid: 82b3676c-7653-421c-aac7-7f20a642779f
title: 'MFPKEY_Decoder_MaxNumPCMSamplesWithPaddedSilence 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b1f97b55c2eedd8cc7d6d524379569073fa35d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983448"
---
# <a name="mfpkey_decoder_maxnumpcmsampleswithpaddedsilence-property"></a><span data-ttu-id="b98cd-103">MFPKEY \_ 解碼器 \_ MaxNumPCMSamplesWithPaddedSilence 屬性</span><span class="sxs-lookup"><span data-stu-id="b98cd-103">MFPKEY\_Decoder\_MaxNumPCMSamplesWithPaddedSilence Property</span></span>

<span data-ttu-id="b98cd-104">指定在解碼檔案之後，可能會傳回的額外 PCM 樣本數上限。</span><span class="sxs-lookup"><span data-stu-id="b98cd-104">Specifies the maximum number of additional PCM samples that might be returned at the end of after decoding a file.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="b98cd-105">IPropertyBag 的常數</span><span class="sxs-lookup"><span data-stu-id="b98cd-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="b98cd-106">僅可使用 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)。</span><span class="sxs-lookup"><span data-stu-id="b98cd-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="b98cd-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="b98cd-107">Data Type</span></span>

<span data-ttu-id="b98cd-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="b98cd-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="b98cd-109">預設值</span><span class="sxs-lookup"><span data-stu-id="b98cd-109">Default Value</span></span>

<span data-ttu-id="b98cd-110">2048</span><span class="sxs-lookup"><span data-stu-id="b98cd-110">2048</span></span>

## <a name="remarks"></a><span data-ttu-id="b98cd-111">備註</span><span class="sxs-lookup"><span data-stu-id="b98cd-111">Remarks</span></span>

<span data-ttu-id="b98cd-112">您可以使用這個屬性來預估在歌曲之間插入的人工無回應，這會在歌曲的另一次送入解碼器時插入。</span><span class="sxs-lookup"><span data-stu-id="b98cd-112">This property can be used to estimate artificial silence that gets is inserted between songs as they are fed to the decoder one after another.</span></span>

<span data-ttu-id="b98cd-113">針對 Windows Media 音訊10專業版和 Windows Media 音訊9無失真的解碼器，這個屬性一律等於0。</span><span class="sxs-lookup"><span data-stu-id="b98cd-113">For the Windows Media Audio 10 Professional and Windows Media Audio 9 Lossless decoders, this property is always equal to 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="b98cd-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="b98cd-114">Requirements</span></span>



| <span data-ttu-id="b98cd-115">需求</span><span class="sxs-lookup"><span data-stu-id="b98cd-115">Requirement</span></span> | <span data-ttu-id="b98cd-116">值</span><span class="sxs-lookup"><span data-stu-id="b98cd-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b98cd-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b98cd-117">Minimum supported client</span></span><br/> | <span data-ttu-id="b98cd-118">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b98cd-118">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="b98cd-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b98cd-119">Minimum supported server</span></span><br/> | <span data-ttu-id="b98cd-120">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b98cd-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b98cd-121">標頭</span><span class="sxs-lookup"><span data-stu-id="b98cd-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="b98cd-122"><dt>Wmcodecdsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="b98cd-122"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b98cd-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b98cd-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b98cd-124">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="b98cd-124">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
