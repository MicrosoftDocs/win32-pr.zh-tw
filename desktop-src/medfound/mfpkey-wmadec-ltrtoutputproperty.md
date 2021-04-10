---
description: 指定解碼器是否應該執行 Lt-Rt 折迭。
ms.assetid: ce1dc4ea-4326-40ab-bb30-ff1a34f06d79
title: 'MFPKEY_WMADEC_LTRTOUTPUT 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4f4a83d2529ce3b37282be35924b48288d4df45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114425"
---
# <a name="mfpkey_wmadec_ltrtoutput-property"></a><span data-ttu-id="fa997-103">MFPKEY \_ WMADEC \_ LTRTOUTPUT 屬性</span><span class="sxs-lookup"><span data-stu-id="fa997-103">MFPKEY\_WMADEC\_LTRTOUTPUT Property</span></span>

<span data-ttu-id="fa997-104">指定解碼器是否應該執行 Lt-Rt 折迭。</span><span class="sxs-lookup"><span data-stu-id="fa997-104">Specifies whether the decoder should perform Lt-Rt fold down.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="fa997-105">IPropertyBag 的常數</span><span class="sxs-lookup"><span data-stu-id="fa997-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="fa997-106">僅可使用 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)。</span><span class="sxs-lookup"><span data-stu-id="fa997-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="fa997-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="fa997-107">Data Type</span></span>

<span data-ttu-id="fa997-108">**VT \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="fa997-108">**VT\_BOOL**</span></span>

## <a name="default-value"></a><span data-ttu-id="fa997-109">預設值</span><span class="sxs-lookup"><span data-stu-id="fa997-109">Default Value</span></span>

<span data-ttu-id="fa997-110">**VARIANT \_ FALSE**</span><span class="sxs-lookup"><span data-stu-id="fa997-110">**VARIANT\_FALSE**</span></span>

## <a name="remarks"></a><span data-ttu-id="fa997-111">備註</span><span class="sxs-lookup"><span data-stu-id="fa997-111">Remarks</span></span>

<span data-ttu-id="fa997-112">如果這個屬性的值為 VARIANT \_ FALSE，且輸出為身歷聲，則音訊解碼器會使用簡單的通道折迭。</span><span class="sxs-lookup"><span data-stu-id="fa997-112">If this property has a value of VARIANT\_FALSE and the output is stereo, the audio decoder uses simple channel fold down.</span></span> <span data-ttu-id="fa997-113">如果這個屬性的值為 VARIANT \_ TRUE，音訊解碼器會執行 Lt-Rt (matrixed) 折迭到身歷聲，然後使用任何杜住的範圍解碼器來解碼 matrixed 環繞。</span><span class="sxs-lookup"><span data-stu-id="fa997-113">If this property has a value of VARIANT\_TRUE, the audio decoder performs Lt-Rt (matrixed) fold down to stereo, and then any Dolby Surround decoder can be used to decode the matrixed surround .</span></span> <span data-ttu-id="fa997-114">例如，音訊解碼器可能會在5.1 或7.1 內容上執行 Lt-Rt 折迭。</span><span class="sxs-lookup"><span data-stu-id="fa997-114">For example, the audio decoder could perform Lt-Rt fold down on 5.1 or 7.1 content.</span></span>

<span data-ttu-id="fa997-115">只有當解碼器作為 DirectX 媒體物件 (的) 時，才支援此屬性。</span><span class="sxs-lookup"><span data-stu-id="fa997-115">This property is supported only when the decoder is acting as a DirectX Media Object (DMO).</span></span> <span data-ttu-id="fa997-116">當解碼器作為媒體基礎轉換 (MFT) 時，不支援任何種類的折迭。</span><span class="sxs-lookup"><span data-stu-id="fa997-116">No fold down of any kind is supported when the decoder is acting as a Media Foundation Transform (MFT).</span></span>

<span data-ttu-id="fa997-117">在 Windows Vista 上，如果您在音訊解碼器上取得 **IPropertyStore** 介面，則該解碼器會作為 MFT。</span><span class="sxs-lookup"><span data-stu-id="fa997-117">On Windows Vista, if you obtain an **IPropertyStore** interface on an audio decoder, the decoder acts as an MFT.</span></span> <span data-ttu-id="fa997-118">因此，這個屬性不能用在 Windows Vista 上。</span><span class="sxs-lookup"><span data-stu-id="fa997-118">Consequently, this property cannot be used on Windows Vista.</span></span> <span data-ttu-id="fa997-119">如需何時將某個解碼器作為一或一個 MFT 的詳細資訊，請參閱 [編解碼器物件](codecobjects.md)底下的個別編解碼器參考頁面。</span><span class="sxs-lookup"><span data-stu-id="fa997-119">For information on when a decoder acts as a DMO or an MFT, see the individual codec reference pages under [Codec Objects](codecobjects.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fa997-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="fa997-120">Requirements</span></span>



| <span data-ttu-id="fa997-121">需求</span><span class="sxs-lookup"><span data-stu-id="fa997-121">Requirement</span></span> | <span data-ttu-id="fa997-122">值</span><span class="sxs-lookup"><span data-stu-id="fa997-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fa997-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fa997-123">Minimum supported client</span></span><br/> | <span data-ttu-id="fa997-124">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fa997-124">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="fa997-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fa997-125">Minimum supported server</span></span><br/> | <span data-ttu-id="fa997-126">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fa997-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="fa997-127">標頭</span><span class="sxs-lookup"><span data-stu-id="fa997-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="fa997-128"><dt>Wmcodecdsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="fa997-128"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fa997-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fa997-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa997-130">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="fa997-130">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
