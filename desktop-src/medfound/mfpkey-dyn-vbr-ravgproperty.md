---
description: 針對設定為使用可進行平均控制的 VBR 編碼的編碼器，指定平均位元速率（以每秒位數為單位）。
ms.assetid: d689a34c-97f7-4b1c-82b6-863ce3b8403f
title: 'MFPKEY_DYN_VBR_RAVG 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8103d36db5a9e946449231943e076c26258eec19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943916"
---
# <a name="mfpkey_dyn_vbr_ravg-property"></a><span data-ttu-id="d2295-103">MFPKEY \_ DYN \_ VBR \_ RAVG 屬性</span><span class="sxs-lookup"><span data-stu-id="d2295-103">MFPKEY\_DYN\_VBR\_RAVG Property</span></span>

<span data-ttu-id="d2295-104">針對設定為使用可進行平均控制的 VBR 編碼的編碼器，指定平均位元速率（以每秒位數為單位）。</span><span class="sxs-lookup"><span data-stu-id="d2295-104">Specifies the average bit rate, in bits per second, for an encoder that is configured to use average-controllable VBR encoding.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="d2295-105">IPropertyBag 的常數</span><span class="sxs-lookup"><span data-stu-id="d2295-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="d2295-106">僅可使用 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)。</span><span class="sxs-lookup"><span data-stu-id="d2295-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="d2295-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="d2295-107">Data Type</span></span>

<span data-ttu-id="d2295-108">**VT \_ I4**</span><span class="sxs-lookup"><span data-stu-id="d2295-108">**VT\_I4**</span></span>

## <a name="remarks"></a><span data-ttu-id="d2295-109">備註</span><span class="sxs-lookup"><span data-stu-id="d2295-109">Remarks</span></span>

<span data-ttu-id="d2295-110">如果 [**MFPKEY \_ AVGCONSTRAINED**](mfpkey-avgconstrainedproperty.md) 和 [**MFPKEY \_ VBRENABLED**](mfpkey-vbrenabledproperty.md) 屬性都設定為 **VARIANT \_ TRUE**，編碼器會使用可進行平均控制的 VBR 編碼。</span><span class="sxs-lookup"><span data-stu-id="d2295-110">If the [**MFPKEY\_AVGCONSTRAINED**](mfpkey-avgconstrainedproperty.md) and [**MFPKEY\_VBRENABLED**](mfpkey-vbrenabledproperty.md) properties are both set to **VARIANT\_TRUE**, the encoder uses average-controllable VBR encoding.</span></span> <span data-ttu-id="d2295-111">在此情況下，編碼器會根據此屬性的值和 [**MFPKEY \_ DYN \_ VBR \_ BAVG**](mfpkey-dyn-vbr-bavgproperty.md) 屬性來設定本身。</span><span class="sxs-lookup"><span data-stu-id="d2295-111">In that case, the encoder configures itself according to the value of this property and the [**MFPKEY\_DYN\_VBR\_BAVG**](mfpkey-dyn-vbr-bavgproperty.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2295-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="d2295-112">Requirements</span></span>



| <span data-ttu-id="d2295-113">需求</span><span class="sxs-lookup"><span data-stu-id="d2295-113">Requirement</span></span> | <span data-ttu-id="d2295-114">值</span><span class="sxs-lookup"><span data-stu-id="d2295-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d2295-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d2295-115">Minimum supported client</span></span><br/> | <span data-ttu-id="d2295-116">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d2295-116">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="d2295-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d2295-117">Minimum supported server</span></span><br/> | <span data-ttu-id="d2295-118">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d2295-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d2295-119">標頭</span><span class="sxs-lookup"><span data-stu-id="d2295-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="d2295-120"><dt>Wmcodecdsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="d2295-120"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d2295-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d2295-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2295-122">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="d2295-122">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
