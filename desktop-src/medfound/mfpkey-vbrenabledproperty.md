---
description: 指定編碼器是否使用變數位速率 (VBR) 編碼。
ms.assetid: e6826802-99b7-4a38-9b58-8a9cb8b753fb
title: 'MFPKEY_VBRENABLED 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab9061abcc6ac7d7338b63eb5a7cd1a13ad22bf6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848796"
---
# <a name="mfpkey_vbrenabled-property"></a><span data-ttu-id="492b0-103">MFPKEY \_ VBRENABLED 屬性</span><span class="sxs-lookup"><span data-stu-id="492b0-103">MFPKEY\_VBRENABLED Property</span></span>

<span data-ttu-id="492b0-104">指定編碼器是否使用變數位速率 (VBR) 編碼。</span><span class="sxs-lookup"><span data-stu-id="492b0-104">Specifies whether the encoder uses variable-bit-rate (VBR) encoding.</span></span> <span data-ttu-id="492b0-105">讀寫。</span><span class="sxs-lookup"><span data-stu-id="492b0-105">Read-write.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="492b0-106">IPropertyBag 的常數</span><span class="sxs-lookup"><span data-stu-id="492b0-106">Constant for IPropertyBag</span></span>

<span data-ttu-id="492b0-107">**g \_ wszWMVCVBREnabled**、 **g \_ wszWMCPAudioVBRSupported**</span><span class="sxs-lookup"><span data-stu-id="492b0-107">**g\_wszWMVCVBREnabled**, **g\_wszWMCPAudioVBRSupported**</span></span>

## <a name="data-type"></a><span data-ttu-id="492b0-108">資料類型</span><span class="sxs-lookup"><span data-stu-id="492b0-108">Data Type</span></span>

<span data-ttu-id="492b0-109">**VT \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="492b0-109">**VT\_BOOL**</span></span>

## <a name="default-value"></a><span data-ttu-id="492b0-110">預設值</span><span class="sxs-lookup"><span data-stu-id="492b0-110">Default Value</span></span>

<span data-ttu-id="492b0-111">**VARIANT \_ FALSE**</span><span class="sxs-lookup"><span data-stu-id="492b0-111">**VARIANT\_FALSE**</span></span>

## <a name="remarks"></a><span data-ttu-id="492b0-112">備註</span><span class="sxs-lookup"><span data-stu-id="492b0-112">Remarks</span></span>

<span data-ttu-id="492b0-113">針對編解碼器所使用的任何其他 VBR 屬性，此值必須設定為 **VARIANT \_ TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="492b0-113">This value must be set to **VARIANT\_TRUE** for any of the other VBR properties to be used by the codec.</span></span>

<span data-ttu-id="492b0-114">當您在音訊編碼器上將此值設定為 **VARIANT \_ TRUE** 之後，使用 [**IMediaObject：： GetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputtype) 方法取出的輸出類型就是 VBR 類型。</span><span class="sxs-lookup"><span data-stu-id="492b0-114">After you set this value to **VARIANT\_TRUE** on the audio encoder, the output types retrieved by using the [**IMediaObject::GetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputtype) method are VBR types.</span></span>

## <a name="requirements"></a><span data-ttu-id="492b0-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="492b0-115">Requirements</span></span>



| <span data-ttu-id="492b0-116">需求</span><span class="sxs-lookup"><span data-stu-id="492b0-116">Requirement</span></span> | <span data-ttu-id="492b0-117">值</span><span class="sxs-lookup"><span data-stu-id="492b0-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="492b0-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="492b0-118">Minimum supported client</span></span><br/> | <span data-ttu-id="492b0-119">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="492b0-119">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="492b0-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="492b0-120">Minimum supported server</span></span><br/> | <span data-ttu-id="492b0-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="492b0-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="492b0-122">標頭</span><span class="sxs-lookup"><span data-stu-id="492b0-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="492b0-123"><dt>Wmcodecdsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="492b0-123"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="492b0-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="492b0-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="492b0-125">**MFPKEY \_ 限制 \_ 列舉 \_ VBRQUALITY**</span><span class="sxs-lookup"><span data-stu-id="492b0-125">**MFPKEY\_CONSTRAIN\_ENUMERATED\_VBRQUALITY**</span></span>](mfpkey-constrain-enumerated-vbrqualityproperty.md)
</dt> <dt>

[<span data-ttu-id="492b0-126">**MFPKEY \_ 所需的 \_ VBRQUALITY**</span><span class="sxs-lookup"><span data-stu-id="492b0-126">**MFPKEY\_DESIRED\_VBRQUALITY**</span></span>](mfpkey-desired-vbrqualityproperty.md)
</dt> <dt>

[<span data-ttu-id="492b0-127">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="492b0-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
