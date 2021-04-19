---
description: 指定最小位速率（以位/秒為單位）。 這個屬性只適用于常數的位元速率 (CBR) 和變數位元速率 (VBR) 編碼模式。
ms.assetid: 57ef6c08-3bad-4d8d-8daf-61041b878802
title: 'AVEncCommonMinBitRate 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95c9b6e84675994d2aca7548f6c13d6558ebc020
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106967016"
---
# <a name="avenccommonminbitrate-property"></a><span data-ttu-id="0bd67-104">AVEncCommonMinBitRate 屬性</span><span class="sxs-lookup"><span data-stu-id="0bd67-104">AVEncCommonMinBitRate property</span></span>

<span data-ttu-id="0bd67-105">指定最小位速率（以位/秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="0bd67-105">Specifies the minimum bit rate, in bits per second.</span></span> <span data-ttu-id="0bd67-106">這個屬性只適用于常數的位元速率 (CBR) 和變數位元速率 (VBR) 編碼模式。</span><span class="sxs-lookup"><span data-stu-id="0bd67-106">This property applies only to constant bit rate (CBR) and variable bit rate (VBR) encoding modes.</span></span>

<span data-ttu-id="0bd67-107">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="0bd67-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="0bd67-108">資料類型</span><span class="sxs-lookup"><span data-stu-id="0bd67-108">Data type</span></span>

<span data-ttu-id="0bd67-109">**UINT32** (**VT \_ UI4**) </span><span class="sxs-lookup"><span data-stu-id="0bd67-109">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="0bd67-110">屬性 GUID</span><span class="sxs-lookup"><span data-stu-id="0bd67-110">Property GUID</span></span>

<span data-ttu-id="0bd67-111">**CODECAPI \_ AVEncCommonMinBitRate**</span><span class="sxs-lookup"><span data-stu-id="0bd67-111">**CODECAPI\_AVEncCommonMinBitRate**</span></span>

## <a name="property-value"></a><span data-ttu-id="0bd67-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="0bd67-112">Property value</span></span>

<span data-ttu-id="0bd67-113">這個屬性具有線性範圍的值。</span><span class="sxs-lookup"><span data-stu-id="0bd67-113">This property has a linear range of values.</span></span> <span data-ttu-id="0bd67-114">若要取得支援的範圍，請呼叫 [**ICodecAPI：： GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange)。</span><span class="sxs-lookup"><span data-stu-id="0bd67-114">To get the supported range, call [**ICodecAPI::GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span></span>

## <a name="remarks"></a><span data-ttu-id="0bd67-115">備註</span><span class="sxs-lookup"><span data-stu-id="0bd67-115">Remarks</span></span>

<span data-ttu-id="0bd67-116">編碼器會視需要增加編碼品質來強制執行最小位元速率。</span><span class="sxs-lookup"><span data-stu-id="0bd67-116">The encoder enforces the minimum bit rate by increasing the encoding quality as necessary.</span></span>

## <a name="requirements"></a><span data-ttu-id="0bd67-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="0bd67-117">Requirements</span></span>



| <span data-ttu-id="0bd67-118">需求</span><span class="sxs-lookup"><span data-stu-id="0bd67-118">Requirement</span></span> | <span data-ttu-id="0bd67-119">值</span><span class="sxs-lookup"><span data-stu-id="0bd67-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0bd67-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0bd67-120">Minimum supported client</span></span><br/> | <span data-ttu-id="0bd67-121">Windows 2000 專業版傳統型 \[ 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0bd67-121">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="0bd67-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0bd67-122">Minimum supported server</span></span><br/> | <span data-ttu-id="0bd67-123">Windows 2000 Server \[ desktop 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0bd67-123">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="0bd67-124">標頭</span><span class="sxs-lookup"><span data-stu-id="0bd67-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="0bd67-125"><dt>Codecapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="0bd67-125"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0bd67-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0bd67-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0bd67-127">編解碼器 API 屬性</span><span class="sxs-lookup"><span data-stu-id="0bd67-127">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="0bd67-128">**ICodecAPI 介面**</span><span class="sxs-lookup"><span data-stu-id="0bd67-128">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




