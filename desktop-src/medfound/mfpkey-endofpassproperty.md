---
description: 指定編碼傳遞的結尾。
ms.assetid: 8a7e6e09-766c-4346-8893-eea5614b2aa4
title: 'MFPKEY_ENDOFPASS 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a38e03867e11cde944bf902ae52f98cda7b8313
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848813"
---
# <a name="mfpkey_endofpass-property"></a><span data-ttu-id="6dc4d-103">MFPKEY \_ ENDOFPASS 屬性</span><span class="sxs-lookup"><span data-stu-id="6dc4d-103">MFPKEY\_ENDOFPASS Property</span></span>

<span data-ttu-id="6dc4d-104">指定編碼傳遞的結尾。</span><span class="sxs-lookup"><span data-stu-id="6dc4d-104">Specifies the end of an encoding pass.</span></span>

## <a name="data-type"></a><span data-ttu-id="6dc4d-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="6dc4d-105">Data Type</span></span>

<span data-ttu-id="6dc4d-106">**VT \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="6dc4d-106">**VT\_BOOL**</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="6dc4d-107">IPropertyBag 的常數</span><span class="sxs-lookup"><span data-stu-id="6dc4d-107">Constant for IPropertyBag</span></span>

<span data-ttu-id="6dc4d-108">g \_ wszWMVCEndOfPass</span><span class="sxs-lookup"><span data-stu-id="6dc4d-108">g\_wszWMVCEndOfPass</span></span>

## <a name="data-type-for-ipropertybag"></a><span data-ttu-id="6dc4d-109">IPropertyBag 的資料類型</span><span class="sxs-lookup"><span data-stu-id="6dc4d-109">Data Type for IPropertyBag</span></span>

<span data-ttu-id="6dc4d-110">不需要任何資料類型。</span><span class="sxs-lookup"><span data-stu-id="6dc4d-110">No data type is required.</span></span> <span data-ttu-id="6dc4d-111">若要設定這個屬性，請傳遞未初始化的 **VARIANT**。</span><span class="sxs-lookup"><span data-stu-id="6dc4d-111">To set this property, pass an uninitialized **VARIANT**.</span></span>

## <a name="remarks"></a><span data-ttu-id="6dc4d-112">備註</span><span class="sxs-lookup"><span data-stu-id="6dc4d-112">Remarks</span></span>

<span data-ttu-id="6dc4d-113">這個屬性不是一般屬性，因為不論值為 VARIANT \_ TRUE 或 variant FALSE，它都有相同的效果 \_ 。</span><span class="sxs-lookup"><span data-stu-id="6dc4d-113">This property is not a normal property because it has the same effect regardless of whether the value is VARIANT\_TRUE or VARIANT\_FALSE.</span></span> <span data-ttu-id="6dc4d-114">您必須在處理前置處理傳遞的最後一個輸入範例之後設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="6dc4d-114">You must set this property after you process the last input samples for a preprocessing pass.</span></span> <span data-ttu-id="6dc4d-115">如果您正在執行多個行程，則必須在每個前置處理階段結束時設定此屬性 (目前沒有任何編解碼器支援多個) 。</span><span class="sxs-lookup"><span data-stu-id="6dc4d-115">If you are performing multiple passes, you must set this property at the end of each preprocessing pass (at present none of the codecs supports more than one).</span></span> <span data-ttu-id="6dc4d-116">如果您未設定此屬性，則編解碼器會假設您仍在傳遞範例以進行前置處理。</span><span class="sxs-lookup"><span data-stu-id="6dc4d-116">If you do not set this property, the codec will assume that you are still passing samples for preprocessing.</span></span>

## <a name="requirements"></a><span data-ttu-id="6dc4d-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="6dc4d-117">Requirements</span></span>



| <span data-ttu-id="6dc4d-118">需求</span><span class="sxs-lookup"><span data-stu-id="6dc4d-118">Requirement</span></span> | <span data-ttu-id="6dc4d-119">值</span><span class="sxs-lookup"><span data-stu-id="6dc4d-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6dc4d-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6dc4d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="6dc4d-121">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6dc4d-121">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="6dc4d-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6dc4d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="6dc4d-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6dc4d-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6dc4d-124">標頭</span><span class="sxs-lookup"><span data-stu-id="6dc4d-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="6dc4d-125"><dt>Wmcodecdsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="6dc4d-125"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6dc4d-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6dc4d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6dc4d-127">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="6dc4d-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




