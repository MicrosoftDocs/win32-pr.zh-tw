---
description: 指定編碼器是否使用平均可控的 VBR 編碼。
ms.assetid: 2c150eb1-4ffe-4f77-8ef8-e3bf29b17b10
title: 'MFPKEY_AVGCONSTRAINED 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0623fb4a73e3721f9079f2a1e5e330ecb466a774
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970802"
---
# <a name="mfpkey_avgconstrained-property"></a><span data-ttu-id="c9128-103">MFPKEY \_ AVGCONSTRAINED 屬性</span><span class="sxs-lookup"><span data-stu-id="c9128-103">MFPKEY\_AVGCONSTRAINED Property</span></span>

<span data-ttu-id="c9128-104">指定編碼器是否使用平均可控的 VBR 編碼。</span><span class="sxs-lookup"><span data-stu-id="c9128-104">Specifies whether the encoder uses average-controllable VBR encoding.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="c9128-105">IPropertyBag 的常數</span><span class="sxs-lookup"><span data-stu-id="c9128-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="c9128-106">僅可使用 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)。</span><span class="sxs-lookup"><span data-stu-id="c9128-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="c9128-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="c9128-107">Data Type</span></span>

<span data-ttu-id="c9128-108">**VT \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="c9128-108">**VT\_BOOL**</span></span>

## <a name="default-value"></a><span data-ttu-id="c9128-109">預設值</span><span class="sxs-lookup"><span data-stu-id="c9128-109">Default Value</span></span>

<span data-ttu-id="c9128-110">**VARIANT \_ FALSE**</span><span class="sxs-lookup"><span data-stu-id="c9128-110">**VARIANT\_FALSE**</span></span>

## <a name="remarks"></a><span data-ttu-id="c9128-111">備註</span><span class="sxs-lookup"><span data-stu-id="c9128-111">Remarks</span></span>

<span data-ttu-id="c9128-112">如果此屬性和 [**MFPKEY \_ VBRENABLED**](mfpkey-vbrenabledproperty.md) 屬性都設定為 **VARIANT \_ TRUE**，編碼器會使用可進行平均控制的 VBR 編碼。</span><span class="sxs-lookup"><span data-stu-id="c9128-112">If this property and the [**MFPKEY\_VBRENABLED**](mfpkey-vbrenabledproperty.md) property are both set to **VARIANT\_TRUE**, the encoder uses average-controllable VBR encoding.</span></span> <span data-ttu-id="c9128-113">在此情況下，編碼器會根據 [**MFPKEY \_ DYN \_ Vbr \_ BAVG**](mfpkey-dyn-vbr-bavgproperty.md) 和 [**MFPKEY \_ DYN \_ vbr \_ RAVG**](mfpkey-dyn-vbr-ravgproperty.md)的值來設定本身。</span><span class="sxs-lookup"><span data-stu-id="c9128-113">In that case, the encoder configures itself according to the values of [**MFPKEY\_DYN\_VBR\_BAVG**](mfpkey-dyn-vbr-bavgproperty.md) and [**MFPKEY\_DYN\_VBR\_RAVG**](mfpkey-dyn-vbr-ravgproperty.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c9128-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="c9128-114">Requirements</span></span>



| <span data-ttu-id="c9128-115">需求</span><span class="sxs-lookup"><span data-stu-id="c9128-115">Requirement</span></span> | <span data-ttu-id="c9128-116">值</span><span class="sxs-lookup"><span data-stu-id="c9128-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c9128-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c9128-117">Minimum supported client</span></span><br/> | <span data-ttu-id="c9128-118">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c9128-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="c9128-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c9128-119">Minimum supported server</span></span><br/> | <span data-ttu-id="c9128-120">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c9128-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c9128-121">標頭</span><span class="sxs-lookup"><span data-stu-id="c9128-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="c9128-122"><dt>Wmcodecdsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="c9128-122"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9128-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c9128-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9128-124">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="c9128-124">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
