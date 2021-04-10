---
description: 指定 MPEG-2 音訊資料流程中原始位的預設設定。 這個屬性會套用至 MPEG 音訊編碼器。
ms.assetid: 62b56868-684f-4f28-90da-dac19cb07946
title: 'AVEncMPAOriginalBitstream 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a1a49fda5bb605ac8735ebac4be758e7f73efb9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846547"
---
# <a name="avencmpaoriginalbitstream-property"></a><span data-ttu-id="9fc56-104">AVEncMPAOriginalBitstream 屬性</span><span class="sxs-lookup"><span data-stu-id="9fc56-104">AVEncMPAOriginalBitstream property</span></span>

<span data-ttu-id="9fc56-105">指定 MPEG-2 音訊資料流程中原始位的預設設定。</span><span class="sxs-lookup"><span data-stu-id="9fc56-105">Specifies the default setting for the original bit in the MPEG-1 audio stream.</span></span> <span data-ttu-id="9fc56-106">這個屬性會套用至 MPEG 音訊編碼器。</span><span class="sxs-lookup"><span data-stu-id="9fc56-106">This property applies to MPEG audio encoders.</span></span>

<span data-ttu-id="9fc56-107">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="9fc56-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="9fc56-108">資料類型</span><span class="sxs-lookup"><span data-stu-id="9fc56-108">Data type</span></span>

<span data-ttu-id="9fc56-109">**變異 \_BOOL** (**VT \_ bool**) </span><span class="sxs-lookup"><span data-stu-id="9fc56-109">**VARIANT\_BOOL** (**VT\_BOOL**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="9fc56-110">屬性 GUID</span><span class="sxs-lookup"><span data-stu-id="9fc56-110">Property GUID</span></span>

<span data-ttu-id="9fc56-111">**CODECAPI \_ AVEncMPAOriginalBitstream**</span><span class="sxs-lookup"><span data-stu-id="9fc56-111">**CODECAPI\_AVEncMPAOriginalBitstream**</span></span>

## <a name="property-value"></a><span data-ttu-id="9fc56-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="9fc56-112">Property value</span></span>

<span data-ttu-id="9fc56-113">這個屬性可以具有下列值。</span><span class="sxs-lookup"><span data-stu-id="9fc56-113">This property can have the following values.</span></span>



| <span data-ttu-id="9fc56-114">值</span><span class="sxs-lookup"><span data-stu-id="9fc56-114">Value</span></span>          | <span data-ttu-id="9fc56-115">描述</span><span class="sxs-lookup"><span data-stu-id="9fc56-115">Description</span></span>          |
|----------------|----------------------|
| <span data-ttu-id="9fc56-116">VARIANT \_ FALSE</span><span class="sxs-lookup"><span data-stu-id="9fc56-116">VARIANT\_FALSE</span></span> | <span data-ttu-id="9fc56-117">原始位為 off。</span><span class="sxs-lookup"><span data-stu-id="9fc56-117">Original bit is off.</span></span> |
| <span data-ttu-id="9fc56-118">VARIANT \_ TRUE</span><span class="sxs-lookup"><span data-stu-id="9fc56-118">VARIANT\_TRUE</span></span>  | <span data-ttu-id="9fc56-119">原始位為開啟。</span><span class="sxs-lookup"><span data-stu-id="9fc56-119">Original bit is on.</span></span>  |



 

## <a name="remarks"></a><span data-ttu-id="9fc56-120">備註</span><span class="sxs-lookup"><span data-stu-id="9fc56-120">Remarks</span></span>

<span data-ttu-id="9fc56-121">編碼器可能會根據輸入資料流程的內容來覆寫此設定。</span><span class="sxs-lookup"><span data-stu-id="9fc56-121">The encoder might override this setting, based on the contents of the input stream.</span></span>

## <a name="requirements"></a><span data-ttu-id="9fc56-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="9fc56-122">Requirements</span></span>



| <span data-ttu-id="9fc56-123">需求</span><span class="sxs-lookup"><span data-stu-id="9fc56-123">Requirement</span></span> | <span data-ttu-id="9fc56-124">值</span><span class="sxs-lookup"><span data-stu-id="9fc56-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9fc56-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9fc56-125">Minimum supported client</span></span><br/> | <span data-ttu-id="9fc56-126">Windows 2000 專業版傳統型 \[ 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9fc56-126">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="9fc56-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9fc56-127">Minimum supported server</span></span><br/> | <span data-ttu-id="9fc56-128">Windows 2000 Server \[ desktop 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9fc56-128">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="9fc56-129">標頭</span><span class="sxs-lookup"><span data-stu-id="9fc56-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="9fc56-130"><dt>Codecapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="9fc56-130"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9fc56-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9fc56-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9fc56-132">編解碼器 API 屬性</span><span class="sxs-lookup"><span data-stu-id="9fc56-132">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="9fc56-133">**ICodecAPI 介面**</span><span class="sxs-lookup"><span data-stu-id="9fc56-133">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




