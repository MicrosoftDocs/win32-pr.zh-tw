---
description: 指定在執行雙向 VBR 編碼時，編碼器是否應該檢查跨行程的資料一致性。 讀寫。
ms.assetid: 68750820-e931-41c2-9d12-89ab83b4b97e
title: 'MFPKEY_CHECKDATACONSISTENCY2P 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abc706712ef1e8bff36a118031fde155bb9bda31
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982507"
---
# <a name="mfpkey_checkdataconsistency2p-property"></a><span data-ttu-id="e470d-104">MFPKEY \_ CHECKDATACONSISTENCY2P 屬性</span><span class="sxs-lookup"><span data-stu-id="e470d-104">MFPKEY\_CHECKDATACONSISTENCY2P Property</span></span>

<span data-ttu-id="e470d-105">指定在執行雙向 VBR 編碼時，編碼器是否應該檢查跨行程的資料一致性。</span><span class="sxs-lookup"><span data-stu-id="e470d-105">Specifies whether whether the encoder should check for data consistency across passes when performing two-pass VBR encoding.</span></span> <span data-ttu-id="e470d-106">讀寫。</span><span class="sxs-lookup"><span data-stu-id="e470d-106">Read-write.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="e470d-107">IPropertyBag 的常數</span><span class="sxs-lookup"><span data-stu-id="e470d-107">Constant for IPropertyBag</span></span>

<span data-ttu-id="e470d-108">僅可使用 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)。</span><span class="sxs-lookup"><span data-stu-id="e470d-108">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="e470d-109">資料類型</span><span class="sxs-lookup"><span data-stu-id="e470d-109">Data Type</span></span>

<span data-ttu-id="e470d-110">**VT \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="e470d-110">**VT\_BOOL**</span></span>

## <a name="default-value"></a><span data-ttu-id="e470d-111">預設值</span><span class="sxs-lookup"><span data-stu-id="e470d-111">Default Value</span></span>

<span data-ttu-id="e470d-112">**VARIANT \_ TRUE**</span><span class="sxs-lookup"><span data-stu-id="e470d-112">**VARIANT\_TRUE**</span></span>

## <a name="remarks"></a><span data-ttu-id="e470d-113">備註</span><span class="sxs-lookup"><span data-stu-id="e470d-113">Remarks</span></span>

<span data-ttu-id="e470d-114">如果您將此屬性保留 **\_ 為 VARIANT TRUE** 的預設值，則編碼器會確認輸入範例在兩個階段之間相符，如果偵測到不一致，則會失敗。</span><span class="sxs-lookup"><span data-stu-id="e470d-114">If you leave this property at its default value of **VARIANT\_TRUE**, the encoder verifies that the input samples match between the two passes, and fails if it detects a discrepancy.</span></span> <span data-ttu-id="e470d-115">導致差異的主要案例是當輸入來自裝置時。</span><span class="sxs-lookup"><span data-stu-id="e470d-115">The main scenario that leads to a discrepancy is when the input comes from a device.</span></span>

## <a name="requirements"></a><span data-ttu-id="e470d-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="e470d-116">Requirements</span></span>



| <span data-ttu-id="e470d-117">需求</span><span class="sxs-lookup"><span data-stu-id="e470d-117">Requirement</span></span> | <span data-ttu-id="e470d-118">值</span><span class="sxs-lookup"><span data-stu-id="e470d-118">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e470d-119">用戶端</span><span class="sxs-lookup"><span data-stu-id="e470d-119">Client</span></span><br/> | <span data-ttu-id="e470d-120">Windows Vista 或 Windows 7</span><span class="sxs-lookup"><span data-stu-id="e470d-120">Windows Vista or Windows 7</span></span><br/>                                                   |
| <span data-ttu-id="e470d-121">標頭</span><span class="sxs-lookup"><span data-stu-id="e470d-121">Header</span></span><br/> | <dl> <span data-ttu-id="e470d-122"><dt>Wmcodecdsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="e470d-122"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e470d-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e470d-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e470d-124">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="e470d-124">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
