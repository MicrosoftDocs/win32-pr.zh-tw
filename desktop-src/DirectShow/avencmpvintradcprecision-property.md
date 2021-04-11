---
description: 指定 DC 係數的精確度（以位為單位）。 這個屬性會套用至 MPEG 視頻編碼器。
ms.assetid: 2b4d11c1-767c-4466-8291-7959d841ae65
title: 'AVEncMPVIntraDCPrecision 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55d4bdd3c08f49586eb2663829271ae4166d917e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846460"
---
# <a name="avencmpvintradcprecision-property"></a><span data-ttu-id="187f4-104">AVEncMPVIntraDCPrecision 屬性</span><span class="sxs-lookup"><span data-stu-id="187f4-104">AVEncMPVIntraDCPrecision property</span></span>

<span data-ttu-id="187f4-105">指定 DC 係數的精確度（以位為單位）。</span><span class="sxs-lookup"><span data-stu-id="187f4-105">Specifies the precision of the DC coefficients, in bits.</span></span> <span data-ttu-id="187f4-106">這個屬性會套用至 MPEG 視頻編碼器。</span><span class="sxs-lookup"><span data-stu-id="187f4-106">This property applies to MPEG video encoders.</span></span>

<span data-ttu-id="187f4-107">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="187f4-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="187f4-108">資料類型</span><span class="sxs-lookup"><span data-stu-id="187f4-108">Data type</span></span>

<span data-ttu-id="187f4-109">**UINT32** (**VT \_ UI4**) </span><span class="sxs-lookup"><span data-stu-id="187f4-109">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="187f4-110">屬性 GUID</span><span class="sxs-lookup"><span data-stu-id="187f4-110">Property GUID</span></span>

<span data-ttu-id="187f4-111">**CODECAPI \_ AVEncMPVIntraDCPrecision**</span><span class="sxs-lookup"><span data-stu-id="187f4-111">**CODECAPI\_AVEncMPVIntraDCPrecision**</span></span>

## <a name="property-value"></a><span data-ttu-id="187f4-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="187f4-112">Property value</span></span>

<span data-ttu-id="187f4-113">這個屬性具有線性範圍的值。</span><span class="sxs-lookup"><span data-stu-id="187f4-113">This property has a linear range of values.</span></span> <span data-ttu-id="187f4-114">若要取得支援的範圍，請呼叫 [**ICodecAPI：： GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange)。</span><span class="sxs-lookup"><span data-stu-id="187f4-114">To get the supported range, call [**ICodecAPI::GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span></span>

## <a name="remarks"></a><span data-ttu-id="187f4-115">備註</span><span class="sxs-lookup"><span data-stu-id="187f4-115">Remarks</span></span>

<span data-ttu-id="187f4-116">這個屬性的一般範圍是8到11位。</span><span class="sxs-lookup"><span data-stu-id="187f4-116">The usual range for this property is 8 to 11 bits.</span></span> <span data-ttu-id="187f4-117">如果值為零，則編碼器會選取有效位數。</span><span class="sxs-lookup"><span data-stu-id="187f4-117">If the value is zero, the encoder selects the precision.</span></span>

## <a name="requirements"></a><span data-ttu-id="187f4-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="187f4-118">Requirements</span></span>



| <span data-ttu-id="187f4-119">需求</span><span class="sxs-lookup"><span data-stu-id="187f4-119">Requirement</span></span> | <span data-ttu-id="187f4-120">值</span><span class="sxs-lookup"><span data-stu-id="187f4-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="187f4-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="187f4-121">Minimum supported client</span></span><br/> | <span data-ttu-id="187f4-122">Windows 2000 專業版傳統型 \[ 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="187f4-122">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="187f4-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="187f4-123">Minimum supported server</span></span><br/> | <span data-ttu-id="187f4-124">Windows 2000 Server \[ desktop 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="187f4-124">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="187f4-125">標頭</span><span class="sxs-lookup"><span data-stu-id="187f4-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="187f4-126"><dt>Codecapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="187f4-126"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="187f4-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="187f4-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="187f4-128">編解碼器 API 屬性</span><span class="sxs-lookup"><span data-stu-id="187f4-128">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="187f4-129">**ICodecAPI 介面**</span><span class="sxs-lookup"><span data-stu-id="187f4-129">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




