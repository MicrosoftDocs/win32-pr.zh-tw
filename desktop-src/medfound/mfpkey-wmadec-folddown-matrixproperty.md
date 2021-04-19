---
description: 指定作者提供的折迭係數，可針對比編碼的資料流程所包含的通道更少的通道來解碼多頻道音訊。
ms.assetid: f6737c05-4b39-4209-9985-9402b28cf316
title: 'MFPKEY_WMADEC_FOLDDOWN_MATRIX 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e92cb2495863d319c7f755d7d72f475ccf1eda75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106998082"
---
# <a name="mfpkey_wmadec_folddown_matrix-property"></a><span data-ttu-id="a8fdc-103">MFPKEY \_ WMADEC \_ FOLDDOWN \_ MATRIX 屬性</span><span class="sxs-lookup"><span data-stu-id="a8fdc-103">MFPKEY\_WMADEC\_FOLDDOWN\_MATRIX Property</span></span>

<span data-ttu-id="a8fdc-104">指定作者提供的折迭係數，可針對比編碼的資料流程所包含的通道更少的通道來解碼多頻道音訊。</span><span class="sxs-lookup"><span data-stu-id="a8fdc-104">Specifies the author-supplied fold-down coefficients for decoding multichannel audio for fewer channels than the encoded stream contains.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="a8fdc-105">IPropertyBag 的常數</span><span class="sxs-lookup"><span data-stu-id="a8fdc-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="a8fdc-106">g \_ wszWMACFoldDownXToYChannels</span><span class="sxs-lookup"><span data-stu-id="a8fdc-106">g\_wszWMACFoldDownXToYChannels</span></span>

<span data-ttu-id="a8fdc-107">g \_ wszWMACFoldXToYChannelsZ</span><span class="sxs-lookup"><span data-stu-id="a8fdc-107">g\_wszWMACFoldXToYChannelsZ</span></span>

## <a name="data-type"></a><span data-ttu-id="a8fdc-108">資料類型</span><span class="sxs-lookup"><span data-stu-id="a8fdc-108">Data Type</span></span>

<span data-ttu-id="a8fdc-109">**VT \_ 陣列 \| vt \_ I4**</span><span class="sxs-lookup"><span data-stu-id="a8fdc-109">**VT\_ARRAY \| VT\_I4**</span></span>

## <a name="remarks"></a><span data-ttu-id="a8fdc-110">備註</span><span class="sxs-lookup"><span data-stu-id="a8fdc-110">Remarks</span></span>

<span data-ttu-id="a8fdc-111">音訊解碼器可作為 DirectX 媒體物件 (的) 或媒體基礎轉換 (MFT) 。</span><span class="sxs-lookup"><span data-stu-id="a8fdc-111">An audio decoder can act as a DirectX Media Object (DMO) or as a Media Foundation Transform (MFT).</span></span> <span data-ttu-id="a8fdc-112">如需何時將某個解碼器作為一或一個 MFT 的詳細資訊，請參閱 [編解碼器物件](codecobjects.md)底下的個別編解碼器參考頁面。</span><span class="sxs-lookup"><span data-stu-id="a8fdc-112">For information on when a decoder acts as a DMO or an MFT, see the individual codec reference pages under [Codec Objects](codecobjects.md).</span></span>

<span data-ttu-id="a8fdc-113">當您使用解碼器做為，則此解碼器可以執行通道折迭，而且您可以藉由呼叫 [**IMediaObject：： GetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputtype)來列舉折迭輸出媒體類型。</span><span class="sxs-lookup"><span data-stu-id="a8fdc-113">When you use a decoder as a DMO, the decoder can perform channel fold down, and you can enumerate folded down output media types by calling [**IMediaObject::GetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputtype).</span></span>

<span data-ttu-id="a8fdc-114">當您使用解碼器做為 MFT 時，此解碼器預設不會執行任何折迭，且不會提供折迭輸出媒體類型。</span><span class="sxs-lookup"><span data-stu-id="a8fdc-114">When you use a decoder as an MFT, the decoder by default will not perform any fold down, and will not offer folded down output media types.</span></span> <span data-ttu-id="a8fdc-115">只有當您使用 **MFPKEY \_ WMADEC \_ FOLDDOWN \_ MATRIX** 屬性來設定自訂折迭係數時，才會執行做為 MFT 的解碼器。</span><span class="sxs-lookup"><span data-stu-id="a8fdc-115">A decoder acting as an MFT will perform fold down only if custom fold-down coefficients are set using the **MFPKEY\_WMADEC\_FOLDDOWN\_MATRIX** property.</span></span>

<span data-ttu-id="a8fdc-116">如果音訊解碼器 MFT 上未設定 **MFPKEY \_ WMADEC \_ FOLDDOWN \_ MATRIX** 屬性，而您想要執行折迭，您可以使用 (作為) 音訊 RESAMPLER 數位訊號處理器的 MFT。</span><span class="sxs-lookup"><span data-stu-id="a8fdc-116">If the **MFPKEY\_WMADEC\_FOLDDOWN\_MATRIX** property is not set on the audio decoder MFT, and you want to perform a fold down, you can use (as an MFT) the Audio Resampler digital signal processor.</span></span>

<span data-ttu-id="a8fdc-117">這個屬性的值是一個字串，其中包含以逗號分隔的整數值清單中的折迭係數。</span><span class="sxs-lookup"><span data-stu-id="a8fdc-117">The value for this property is a string containing fold-down coefficients in a comma-separated list of integer values.</span></span> <span data-ttu-id="a8fdc-118">此清單必須針對編碼內容中的每個通道包含一些整數，等於已解碼內容中的通道數目。</span><span class="sxs-lookup"><span data-stu-id="a8fdc-118">The list must contain a number of integers for each channel in the encoded content equal to the number of channels in the decoded content.</span></span>

<span data-ttu-id="a8fdc-119">如果係數為零，要在字串中使用的值必須是 "-2147483648"; 否則，會使用方程式： 20 \* 65536 \* log10 (x) 來計算值。</span><span class="sxs-lookup"><span data-stu-id="a8fdc-119">If the coefficient is zero, the value to be used in the string must be "-2147483648";otherwise the value is computed using the equation: 20 \* 65536 \* log10(x).</span></span>

<span data-ttu-id="a8fdc-120">係數會依通道遮罩順序列出，如同 mmreg .h 標頭檔中包含的通道遮罩常數所定義。</span><span class="sxs-lookup"><span data-stu-id="a8fdc-120">Coefficients are listed in channel mask order, as defined by the channel mask constants that are included in the mmreg.h header file.</span></span> <span data-ttu-id="a8fdc-121">因此，6對2通道中的前兩個值會向下折迭，代表左方輸出通道的部分，以及由6個通道資料流程中中央左邊通道所組成的右側輸出通道。</span><span class="sxs-lookup"><span data-stu-id="a8fdc-121">Therefore, the first two values in a 6-to-2 channel fold-down represent the portions of the left output channel and the right output channel that are made up of the center left channel in the 6 channel stream.</span></span>

<span data-ttu-id="a8fdc-122">只有當作者提供的折迭值與編碼的內容一起保存時，才應該設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="a8fdc-122">You should set this property only if author-supplied fold-down values are persisted with the encoded content.</span></span> <span data-ttu-id="a8fdc-123">否則，請讓該解碼器進行自己的計算。</span><span class="sxs-lookup"><span data-stu-id="a8fdc-123">Otherwise, let the decoder make its own calculations.</span></span>

<span data-ttu-id="a8fdc-124">Windows Media 音訊10專業版編解碼器目前僅支援折迭至兩個通道。</span><span class="sxs-lookup"><span data-stu-id="a8fdc-124">The Windows Media Audio 10 Professional codec currently only supports fold-down to two channels.</span></span>

<span data-ttu-id="a8fdc-125">如果 [ [MFPKEY \_ WMADEC \_ SPKRCFG](mfpkey-wmadec-spkrcfgproperty.md) ] 屬性設定為 [DSSPEAKER 範圍]，則編解碼器會忽略作者提供的折迭係數，並向下折迭為可由接收者的矩陣編解碼器處理的雙聲道信號。 **\_**</span><span class="sxs-lookup"><span data-stu-id="a8fdc-125">If the [MFPKEY\_WMADEC\_SPKRCFG](mfpkey-wmadec-spkrcfgproperty.md) property is set to **DSSPEAKER\_SURROUND**, the codec will ignore author-supplied fold-down coefficients and fold down to a 2-channel signal that can be processed by the matrix decoder of the receiver.</span></span> <span data-ttu-id="a8fdc-126">這可讓環繞設備傳遞四個通道。</span><span class="sxs-lookup"><span data-stu-id="a8fdc-126">This enables surround equipment to deliver four channels.</span></span> <span data-ttu-id="a8fdc-127">只有當來源為5.1 時，才支援此模式。</span><span class="sxs-lookup"><span data-stu-id="a8fdc-127">This mode is supported only if the source is 5.1.</span></span> <span data-ttu-id="a8fdc-128">編解碼器只能將8個通道折迭為2個通道。</span><span class="sxs-lookup"><span data-stu-id="a8fdc-128">The codec can only fold 8 channels to 2 channels.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8fdc-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="a8fdc-129">Requirements</span></span>



| <span data-ttu-id="a8fdc-130">需求</span><span class="sxs-lookup"><span data-stu-id="a8fdc-130">Requirement</span></span> | <span data-ttu-id="a8fdc-131">值</span><span class="sxs-lookup"><span data-stu-id="a8fdc-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a8fdc-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a8fdc-132">Minimum supported client</span></span><br/> | <span data-ttu-id="a8fdc-133">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a8fdc-133">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="a8fdc-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a8fdc-134">Minimum supported server</span></span><br/> | <span data-ttu-id="a8fdc-135">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a8fdc-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a8fdc-136">標頭</span><span class="sxs-lookup"><span data-stu-id="a8fdc-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="a8fdc-137"><dt>Wmcodecdsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="a8fdc-137"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8fdc-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a8fdc-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8fdc-139">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="a8fdc-139">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
