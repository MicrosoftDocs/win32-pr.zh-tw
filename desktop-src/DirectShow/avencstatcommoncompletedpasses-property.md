---
description: 指定已完成的編碼傳遞數目。 這個屬性只適用于多重傳遞編碼。
ms.assetid: 19286f26-96f1-429c-9d6a-5e9b98597cd2
title: 'AVEncStatCommonCompletedPasses 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2927e501963d450cbc08106e7860dfbfd2d7d98a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106997464"
---
# <a name="avencstatcommoncompletedpasses-property"></a><span data-ttu-id="d63dc-104">AVEncStatCommonCompletedPasses 屬性</span><span class="sxs-lookup"><span data-stu-id="d63dc-104">AVEncStatCommonCompletedPasses property</span></span>

<span data-ttu-id="d63dc-105">指定已完成的編碼傳遞數目。</span><span class="sxs-lookup"><span data-stu-id="d63dc-105">Specifies the number of completed encoding passes.</span></span> <span data-ttu-id="d63dc-106">這個屬性只適用于多重傳遞編碼。</span><span class="sxs-lookup"><span data-stu-id="d63dc-106">This property applies only to multi-pass encoding.</span></span>

<span data-ttu-id="d63dc-107">這是唯讀的屬性。</span><span class="sxs-lookup"><span data-stu-id="d63dc-107">This property is read-only.</span></span>

## <a name="data-type"></a><span data-ttu-id="d63dc-108">資料類型</span><span class="sxs-lookup"><span data-stu-id="d63dc-108">Data type</span></span>

<span data-ttu-id="d63dc-109">**UINT32** (**VT \_ UI4**) </span><span class="sxs-lookup"><span data-stu-id="d63dc-109">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="d63dc-110">屬性 GUID</span><span class="sxs-lookup"><span data-stu-id="d63dc-110">Property GUID</span></span>

<span data-ttu-id="d63dc-111">**CODECAPI \_ AVEncStatCommonCompletedPasses**</span><span class="sxs-lookup"><span data-stu-id="d63dc-111">**CODECAPI\_AVEncStatCommonCompletedPasses**</span></span>

## <a name="property-value"></a><span data-ttu-id="d63dc-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="d63dc-112">Property value</span></span>

<span data-ttu-id="d63dc-113">這個屬性具有線性範圍的值。</span><span class="sxs-lookup"><span data-stu-id="d63dc-113">This property has a linear range of values.</span></span> <span data-ttu-id="d63dc-114">若要取得支援的範圍，請呼叫 [**ICodecAPI：： GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange)。</span><span class="sxs-lookup"><span data-stu-id="d63dc-114">To get the supported range, call [**ICodecAPI::GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span></span>

## <a name="requirements"></a><span data-ttu-id="d63dc-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="d63dc-115">Requirements</span></span>



| <span data-ttu-id="d63dc-116">需求</span><span class="sxs-lookup"><span data-stu-id="d63dc-116">Requirement</span></span> | <span data-ttu-id="d63dc-117">值</span><span class="sxs-lookup"><span data-stu-id="d63dc-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d63dc-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d63dc-118">Minimum supported client</span></span><br/> | <span data-ttu-id="d63dc-119">Windows 2000 專業版傳統型 \[ 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d63dc-119">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="d63dc-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d63dc-120">Minimum supported server</span></span><br/> | <span data-ttu-id="d63dc-121">Windows 2000 Server \[ desktop 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d63dc-121">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="d63dc-122">標頭</span><span class="sxs-lookup"><span data-stu-id="d63dc-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="d63dc-123"><dt>Codecapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="d63dc-123"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d63dc-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d63dc-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d63dc-125">編解碼器 API 屬性</span><span class="sxs-lookup"><span data-stu-id="d63dc-125">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="d63dc-126">**ICodecAPI 介面**</span><span class="sxs-lookup"><span data-stu-id="d63dc-126">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




