---
description: 以毫秒為單位，為設定為使用可進行平均控制之 VBR 編碼的編碼器指定緩衝區視窗（以毫秒為單位）。
ms.assetid: ce330ce0-4bda-4340-b21c-63a8b9168cf4
title: 'MFPKEY_DYN_VBR_BAVG 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e117c2852f660b015bcdd95224178730d2e2a1e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106996686"
---
# <a name="mfpkey_dyn_vbr_bavg-property"></a><span data-ttu-id="b8a14-103">MFPKEY \_ DYN \_ VBR \_ BAVG 屬性</span><span class="sxs-lookup"><span data-stu-id="b8a14-103">MFPKEY\_DYN\_VBR\_BAVG Property</span></span>

<span data-ttu-id="b8a14-104">以毫秒為單位，為設定為使用可進行平均控制之 VBR 編碼的編碼器指定緩衝區視窗（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="b8a14-104">Specifies the buffer window, in milliseconds, for an encoder that is configured to use average-controllable VBR encoding.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="b8a14-105">IPropertyBag 的常數</span><span class="sxs-lookup"><span data-stu-id="b8a14-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="b8a14-106">僅可使用 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)。</span><span class="sxs-lookup"><span data-stu-id="b8a14-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="b8a14-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="b8a14-107">Data Type</span></span>

<span data-ttu-id="b8a14-108">**VT \_ I4**</span><span class="sxs-lookup"><span data-stu-id="b8a14-108">**VT\_I4**</span></span>

## <a name="remarks"></a><span data-ttu-id="b8a14-109">備註</span><span class="sxs-lookup"><span data-stu-id="b8a14-109">Remarks</span></span>

<span data-ttu-id="b8a14-110">如果 [**MFPKEY \_ AVGCONSTRAINED**](mfpkey-avgconstrainedproperty.md) 和 [**MFPKEY \_ VBRENABLED**](mfpkey-vbrenabledproperty.md) 屬性都設定為 **VARIANT \_ TRUE**，編碼器會使用可進行平均控制的 VBR 編碼。</span><span class="sxs-lookup"><span data-stu-id="b8a14-110">If the [**MFPKEY\_AVGCONSTRAINED**](mfpkey-avgconstrainedproperty.md) and [**MFPKEY\_VBRENABLED**](mfpkey-vbrenabledproperty.md) properties are both set to **VARIANT\_TRUE**, the encoder uses average-controllable VBR encoding.</span></span> <span data-ttu-id="b8a14-111">在此情況下，編碼器會根據此屬性的值和 [**MFPKEY \_ DYN \_ VBR \_ RAVG**](mfpkey-dyn-vbr-ravgproperty.md) 屬性來設定本身。</span><span class="sxs-lookup"><span data-stu-id="b8a14-111">In that case, the encoder configures itself according to the value of this property and the [**MFPKEY\_DYN\_VBR\_RAVG**](mfpkey-dyn-vbr-ravgproperty.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8a14-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="b8a14-112">Requirements</span></span>



| <span data-ttu-id="b8a14-113">需求</span><span class="sxs-lookup"><span data-stu-id="b8a14-113">Requirement</span></span> | <span data-ttu-id="b8a14-114">值</span><span class="sxs-lookup"><span data-stu-id="b8a14-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b8a14-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b8a14-115">Minimum supported client</span></span><br/> | <span data-ttu-id="b8a14-116">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b8a14-116">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="b8a14-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b8a14-117">Minimum supported server</span></span><br/> | <span data-ttu-id="b8a14-118">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b8a14-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b8a14-119">標頭</span><span class="sxs-lookup"><span data-stu-id="b8a14-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="b8a14-120"><dt>Wmcodecdsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="b8a14-120"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8a14-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b8a14-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8a14-122">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="b8a14-122">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
