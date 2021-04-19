---
description: 指定最新列舉輸出類型的 VBR 品質層級。
ms.assetid: 7d67e41f-060b-49a1-9e17-5db081ef4210
title: 'MFPKEY_MOST_RECENT_ENUMERATED_VBRQUALITY 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ccd3b5f3aae6dc5347672cf6697c3431163dcbd1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991007"
---
# <a name="mfpkey_most_recent_enumerated_vbrquality-property"></a><span data-ttu-id="8d1c3-103">MFPKEY \_ 最 \_ 新的 \_ 列舉 \_ VBRQUALITY 屬性</span><span class="sxs-lookup"><span data-stu-id="8d1c3-103">MFPKEY\_MOST\_RECENT\_ENUMERATED\_VBRQUALITY Property</span></span>

<span data-ttu-id="8d1c3-104">指定最新列舉輸出類型的 VBR 品質層級。</span><span class="sxs-lookup"><span data-stu-id="8d1c3-104">Specifies the VBR quality level of the most recently enumerated output type.</span></span> <span data-ttu-id="8d1c3-105">唯讀。</span><span class="sxs-lookup"><span data-stu-id="8d1c3-105">Read-only.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="8d1c3-106">IPropertyBag 的常數</span><span class="sxs-lookup"><span data-stu-id="8d1c3-106">Constant for IPropertyBag</span></span>

<span data-ttu-id="8d1c3-107">僅可使用 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)。</span><span class="sxs-lookup"><span data-stu-id="8d1c3-107">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="8d1c3-108">資料類型</span><span class="sxs-lookup"><span data-stu-id="8d1c3-108">Data Type</span></span>

<span data-ttu-id="8d1c3-109">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="8d1c3-109">**VT\_UI4**</span></span>

## <a name="remarks"></a><span data-ttu-id="8d1c3-110">備註</span><span class="sxs-lookup"><span data-stu-id="8d1c3-110">Remarks</span></span>

<span data-ttu-id="8d1c3-111">當編碼器做為媒體基礎轉換 (MFT) ，且它會在呼叫 [**IMFTransform：： GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype)時列舉輸出類型時，您可以針對 **MFPKEY \_ \_ 最近 \_ 列舉的 \_ VBRQUALITY** 屬性查詢 MFT。</span><span class="sxs-lookup"><span data-stu-id="8d1c3-111">When the encoder is acting as an Media Foundation Transform (MFT) and it enumerates an output type on a call to [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype), you can query the MFT for the **MFPKEY\_MOST\_RECENTLY\_ENUMERATED\_VBRQUALITY** property.</span></span> <span data-ttu-id="8d1c3-112">傳回的值表示最近傳回之輸出媒體類型的 VBR 品質。</span><span class="sxs-lookup"><span data-stu-id="8d1c3-112">The value returned indicates the VBR quality of the most recently returned output media type.</span></span> <span data-ttu-id="8d1c3-113">然後您可以使用該值來設定編碼器的 [**MFPKEY \_ 所需 \_ VBRQUALITY**](mfpkey-desired-vbrqualityproperty.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="8d1c3-113">Then you can use that value to set the [**MFPKEY\_DESIRED\_VBRQUALITY**](mfpkey-desired-vbrqualityproperty.md) property of the encoder.</span></span>

## <a name="requirements"></a><span data-ttu-id="8d1c3-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="8d1c3-114">Requirements</span></span>



| <span data-ttu-id="8d1c3-115">需求</span><span class="sxs-lookup"><span data-stu-id="8d1c3-115">Requirement</span></span> | <span data-ttu-id="8d1c3-116">值</span><span class="sxs-lookup"><span data-stu-id="8d1c3-116">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8d1c3-117">用戶端</span><span class="sxs-lookup"><span data-stu-id="8d1c3-117">Client</span></span><br/> | <span data-ttu-id="8d1c3-118">Windows Vista 或 Windows 7</span><span class="sxs-lookup"><span data-stu-id="8d1c3-118">Windows Vista or Windows 7</span></span><br/>                                                   |
| <span data-ttu-id="8d1c3-119">標頭</span><span class="sxs-lookup"><span data-stu-id="8d1c3-119">Header</span></span><br/> | <dl> <span data-ttu-id="8d1c3-120"><dt>Wmcodecdsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="8d1c3-120"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8d1c3-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8d1c3-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d1c3-122">**MFPKEY \_ VBRENABLED**</span><span class="sxs-lookup"><span data-stu-id="8d1c3-122">**MFPKEY\_VBRENABLED**</span></span>](mfpkey-vbrenabledproperty.md)
</dt> <dt>

[<span data-ttu-id="8d1c3-123">**MFPKEY \_ 限制 \_ 列舉 \_ VBRQUALITY**</span><span class="sxs-lookup"><span data-stu-id="8d1c3-123">**MFPKEY\_CONSTRAIN\_ENUMERATED\_VBRQUALITY**</span></span>](mfpkey-constrain-enumerated-vbrqualityproperty.md)
</dt> <dt>

[<span data-ttu-id="8d1c3-124">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="8d1c3-124">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
