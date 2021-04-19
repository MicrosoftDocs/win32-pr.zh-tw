---
description: 指定編碼器是否受限於最大的解碼器延遲需求。
ms.assetid: 054e445e-fc71-4d4f-9e9f-f5ff71f0b4ee
title: 'MFPKEY_CONSTRAINDECLATENCY 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 343bcc9bd365b9f1321b200baa203fc27784594c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106969319"
---
# <a name="mfpkey_constraindeclatency-property"></a><span data-ttu-id="31486-103">MFPKEY \_ CONSTRAINDECLATENCY 屬性</span><span class="sxs-lookup"><span data-stu-id="31486-103">MFPKEY\_CONSTRAINDECLATENCY Property</span></span>

<span data-ttu-id="31486-104">指定編碼器是否受限於最大的解碼器延遲需求。</span><span class="sxs-lookup"><span data-stu-id="31486-104">Specifies whether the encoder is constrained by a maximum decoder latency requirement.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="31486-105">IPropertyBag 的常數</span><span class="sxs-lookup"><span data-stu-id="31486-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="31486-106">僅可使用 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)。</span><span class="sxs-lookup"><span data-stu-id="31486-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="31486-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="31486-107">Data Type</span></span>

<span data-ttu-id="31486-108">**VT \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="31486-108">**VT\_BOOL**</span></span>

## <a name="default-value"></a><span data-ttu-id="31486-109">預設值</span><span class="sxs-lookup"><span data-stu-id="31486-109">Default Value</span></span>

<span data-ttu-id="31486-110">**VARIANT \_ FALSE**</span><span class="sxs-lookup"><span data-stu-id="31486-110">**VARIANT\_FALSE**</span></span>

## <a name="remarks"></a><span data-ttu-id="31486-111">備註</span><span class="sxs-lookup"><span data-stu-id="31486-111">Remarks</span></span>

<span data-ttu-id="31486-112">如果您將此屬性保留為預設值 [ **VARIANT \_ FALSE**]，則編碼器會列舉一組預設的模式，其中大約有1500毫秒的解碼器延遲。</span><span class="sxs-lookup"><span data-stu-id="31486-112">If you leave this property at its default value of **VARIANT\_FALSE**, the encoder enumerates a default set of modes that have about 1500 milliseconds of decoder latency.</span></span> <span data-ttu-id="31486-113">如果您將此屬性設定為 **VARIANT \_ TRUE**，您也必須藉由設定 [**MFPKEY \_ MAXDECLATENCYMS**](mfpkey-maxdeclatencymsproperty.md) 屬性來指定最大的解碼器延遲。</span><span class="sxs-lookup"><span data-stu-id="31486-113">If you set this property to **VARIANT\_TRUE**, you must also specify a maximum decoder latency by setting the [**MFPKEY\_MAXDECLATENCYMS**](mfpkey-maxdeclatencymsproperty.md) property.</span></span> <span data-ttu-id="31486-114">在此情況下，編碼器會建立符合延遲需求的模式，並只列舉這些模式。</span><span class="sxs-lookup"><span data-stu-id="31486-114">In that case, the encoder creates modes that satisfy the latency requirement and enumerates only those modes.</span></span> <span data-ttu-id="31486-115">編碼器可確保預先 (的) 解碼器緩衝區大小的需求小於或等於 **MFPKEY \_ MAXDECLATENCYMS**。</span><span class="sxs-lookup"><span data-stu-id="31486-115">The encoder ensures that the preroll requirements (decoder buffer size) are less than or equal to **MFPKEY\_MAXDECLATENCYMS**.</span></span>

## <a name="requirements"></a><span data-ttu-id="31486-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="31486-116">Requirements</span></span>



| <span data-ttu-id="31486-117">需求</span><span class="sxs-lookup"><span data-stu-id="31486-117">Requirement</span></span> | <span data-ttu-id="31486-118">值</span><span class="sxs-lookup"><span data-stu-id="31486-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="31486-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="31486-119">Minimum supported client</span></span><br/> | <span data-ttu-id="31486-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="31486-120">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="31486-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="31486-121">Minimum supported server</span></span><br/> | <span data-ttu-id="31486-122">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="31486-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="31486-123">標頭</span><span class="sxs-lookup"><span data-stu-id="31486-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="31486-124"><dt>Wmcodecdsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="31486-124"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31486-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="31486-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31486-126">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="31486-126">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
