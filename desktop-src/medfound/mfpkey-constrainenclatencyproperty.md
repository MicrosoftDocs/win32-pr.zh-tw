---
description: 指定編碼器是否受限於最大延遲需求。
ms.assetid: 8148ae1e-239e-40fa-a88d-810a1d93d8e9
title: 'MFPKEY_CONSTRAINENCLATENCY 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6f880006bf2aba04196547a79e74f94a7210edd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106981527"
---
# <a name="mfpkey_constrainenclatency-property"></a><span data-ttu-id="e3f4d-103">MFPKEY \_ CONSTRAINENCLATENCY 屬性</span><span class="sxs-lookup"><span data-stu-id="e3f4d-103">MFPKEY\_CONSTRAINENCLATENCY Property</span></span>

<span data-ttu-id="e3f4d-104">指定編碼器是否受限於最大延遲需求。</span><span class="sxs-lookup"><span data-stu-id="e3f4d-104">Specifies whether the encoder is constrained by a maximum latency requirement.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="e3f4d-105">IPropertyBag 的常數</span><span class="sxs-lookup"><span data-stu-id="e3f4d-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="e3f4d-106">僅可使用 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)。</span><span class="sxs-lookup"><span data-stu-id="e3f4d-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="e3f4d-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="e3f4d-107">Data Type</span></span>

<span data-ttu-id="e3f4d-108">**VT \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="e3f4d-108">**VT\_BOOL**</span></span>

## <a name="default-value"></a><span data-ttu-id="e3f4d-109">預設值</span><span class="sxs-lookup"><span data-stu-id="e3f4d-109">Default Value</span></span>

<span data-ttu-id="e3f4d-110">**VARIANT \_ FALSE**</span><span class="sxs-lookup"><span data-stu-id="e3f4d-110">**VARIANT\_FALSE**</span></span>

## <a name="remarks"></a><span data-ttu-id="e3f4d-111">備註</span><span class="sxs-lookup"><span data-stu-id="e3f4d-111">Remarks</span></span>

<span data-ttu-id="e3f4d-112">如果您將此屬性保留為 **變數 \_ FALSE** 的預設值，則編碼器會列舉一組預設的模式，其具有大約2000毫秒的編碼器延遲。</span><span class="sxs-lookup"><span data-stu-id="e3f4d-112">If you leave this property at its default value of **VARIANT\_FALSE**, the encoder enumerates a default set of modes that have about 2000 milliseconds of encoder latency.</span></span> <span data-ttu-id="e3f4d-113">如果您將此屬性設定為 **VARIANT \_ TRUE**，您也必須藉由設定 [**MFPKEY \_ MAXENCLATENCYMS**](mfpkey-maxenclatencymsproperty.md) 屬性來指定最大編碼器延遲。</span><span class="sxs-lookup"><span data-stu-id="e3f4d-113">If you set this property to **VARIANT\_TRUE**, you must also specify a maximum encoder latency by setting the [**MFPKEY\_MAXENCLATENCYMS**](mfpkey-maxenclatencymsproperty.md) property.</span></span> <span data-ttu-id="e3f4d-114">在此情況下，編碼器會建立符合延遲需求的模式，並只列舉這些模式。</span><span class="sxs-lookup"><span data-stu-id="e3f4d-114">In that case, the encoder creates modes that satisfy the latency requirement and enumerates only those modes.</span></span> <span data-ttu-id="e3f4d-115">編碼器在一段時間內收到等於 **MFPKEY \_ MAXENCLATENCYMS** 的輸入時，就會保證輸出範例。</span><span class="sxs-lookup"><span data-stu-id="e3f4d-115">The encoder guarantees an output sample as soon as the encoder has received input for a time period equal to **MFPKEY\_MAXENCLATENCYMS**.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3f4d-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="e3f4d-116">Requirements</span></span>



| <span data-ttu-id="e3f4d-117">需求</span><span class="sxs-lookup"><span data-stu-id="e3f4d-117">Requirement</span></span> | <span data-ttu-id="e3f4d-118">值</span><span class="sxs-lookup"><span data-stu-id="e3f4d-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e3f4d-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e3f4d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e3f4d-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e3f4d-120">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="e3f4d-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e3f4d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e3f4d-122">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e3f4d-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e3f4d-123">標頭</span><span class="sxs-lookup"><span data-stu-id="e3f4d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="e3f4d-124"><dt>Wmcodecdsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="e3f4d-124"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3f4d-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e3f4d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3f4d-126">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="e3f4d-126">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
