---
description: 指定編碼器是否產生開啟的圖片群組 (Gop) 或已關閉的 Gop。 這個屬性會套用至 MPEG 視頻編碼器。
ms.assetid: 424751cd-65d2-4cab-9f7b-cad50c09c767
title: 'AVEncMPVGOPOpen 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6dd971a6cc9926245b97794868f58758af814803
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103688140"
---
# <a name="avencmpvgopopen-property"></a><span data-ttu-id="32b9b-104">AVEncMPVGOPOpen 屬性</span><span class="sxs-lookup"><span data-stu-id="32b9b-104">AVEncMPVGOPOpen property</span></span>

<span data-ttu-id="32b9b-105">指定編碼器是否產生開啟的圖片群組 (Gop) 或已關閉的 Gop。</span><span class="sxs-lookup"><span data-stu-id="32b9b-105">Specifies whether the encoder produces open groups of pictures (GOPs) or closed GOPs.</span></span> <span data-ttu-id="32b9b-106">這個屬性會套用至 MPEG 視頻編碼器。</span><span class="sxs-lookup"><span data-stu-id="32b9b-106">This property applies to MPEG video encoders.</span></span>

<span data-ttu-id="32b9b-107">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="32b9b-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="32b9b-108">資料類型</span><span class="sxs-lookup"><span data-stu-id="32b9b-108">Data type</span></span>

<span data-ttu-id="32b9b-109">**變異 \_BOOL** (**VT \_ bool**) </span><span class="sxs-lookup"><span data-stu-id="32b9b-109">**VARIANT\_BOOL** (**VT\_BOOL**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="32b9b-110">屬性 GUID</span><span class="sxs-lookup"><span data-stu-id="32b9b-110">Property GUID</span></span>

<span data-ttu-id="32b9b-111">**CODECAPI \_ AVEncMPVGOPOpen**</span><span class="sxs-lookup"><span data-stu-id="32b9b-111">**CODECAPI\_AVEncMPVGOPOpen**</span></span>

## <a name="property-value"></a><span data-ttu-id="32b9b-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="32b9b-112">Property value</span></span>



| <span data-ttu-id="32b9b-113">值</span><span class="sxs-lookup"><span data-stu-id="32b9b-113">Value</span></span>          | <span data-ttu-id="32b9b-114">描述</span><span class="sxs-lookup"><span data-stu-id="32b9b-114">Description</span></span> |
|----------------|-------------|
| <span data-ttu-id="32b9b-115">VARIANT \_ FALSE</span><span class="sxs-lookup"><span data-stu-id="32b9b-115">VARIANT\_FALSE</span></span> | <span data-ttu-id="32b9b-116">封閉式 Gop</span><span class="sxs-lookup"><span data-stu-id="32b9b-116">Closed GOPs</span></span> |
| <span data-ttu-id="32b9b-117">VARIANT \_ TRUE</span><span class="sxs-lookup"><span data-stu-id="32b9b-117">VARIANT\_TRUE</span></span>  | <span data-ttu-id="32b9b-118">開啟 Gop</span><span class="sxs-lookup"><span data-stu-id="32b9b-118">Open GOPs</span></span>   |



 

## <a name="remarks"></a><span data-ttu-id="32b9b-119">備註</span><span class="sxs-lookup"><span data-stu-id="32b9b-119">Remarks</span></span>

<span data-ttu-id="32b9b-120">開啟的 GOP 包含從上一個 GOP 參考框架的差異框架。</span><span class="sxs-lookup"><span data-stu-id="32b9b-120">An open GOP contains delta frames that reference frames from the previous GOP.</span></span> <span data-ttu-id="32b9b-121">封閉的 GOP 不包含任何參考先前 GOP 的 delta 框架。</span><span class="sxs-lookup"><span data-stu-id="32b9b-121">A closed GOP does not contain any delta frames that reference the previous GOP.</span></span>

## <a name="requirements"></a><span data-ttu-id="32b9b-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="32b9b-122">Requirements</span></span>



| <span data-ttu-id="32b9b-123">需求</span><span class="sxs-lookup"><span data-stu-id="32b9b-123">Requirement</span></span> | <span data-ttu-id="32b9b-124">值</span><span class="sxs-lookup"><span data-stu-id="32b9b-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="32b9b-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="32b9b-125">Minimum supported client</span></span><br/> | <span data-ttu-id="32b9b-126">Windows 2000 專業版傳統型 \[ 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="32b9b-126">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="32b9b-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="32b9b-127">Minimum supported server</span></span><br/> | <span data-ttu-id="32b9b-128">Windows 2000 Server \[ desktop 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="32b9b-128">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="32b9b-129">標頭</span><span class="sxs-lookup"><span data-stu-id="32b9b-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="32b9b-130"><dt>Codecapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="32b9b-130"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32b9b-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="32b9b-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32b9b-132">編解碼器 API 屬性</span><span class="sxs-lookup"><span data-stu-id="32b9b-132">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="32b9b-133">**ICodecAPI 介面**</span><span class="sxs-lookup"><span data-stu-id="32b9b-133">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




