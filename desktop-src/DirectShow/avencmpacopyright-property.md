---
description: 指定 MPEG-2 音訊串流中的著作權位預設設定。 這個屬性會套用至 MPEG 音訊編碼器。
ms.assetid: 6029c96f-b1dd-402f-9bac-9021bd897ee4
title: 'AVEncMPACopyright 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4449c41448d59ce673e667be7400d4a713236dd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104385774"
---
# <a name="avencmpacopyright-property"></a><span data-ttu-id="df249-104">AVEncMPACopyright 屬性</span><span class="sxs-lookup"><span data-stu-id="df249-104">AVEncMPACopyright property</span></span>

<span data-ttu-id="df249-105">指定 MPEG-2 音訊串流中的著作權位預設設定。</span><span class="sxs-lookup"><span data-stu-id="df249-105">Specifies the default setting for the copyright bit in the MPEG-1 audio stream.</span></span> <span data-ttu-id="df249-106">這個屬性會套用至 MPEG 音訊編碼器。</span><span class="sxs-lookup"><span data-stu-id="df249-106">This property applies to MPEG audio encoders.</span></span>

<span data-ttu-id="df249-107">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="df249-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="df249-108">資料類型</span><span class="sxs-lookup"><span data-stu-id="df249-108">Data type</span></span>

<span data-ttu-id="df249-109">**變異 \_BOOL** (**VT \_ bool**) </span><span class="sxs-lookup"><span data-stu-id="df249-109">**VARIANT\_BOOL** (**VT\_BOOL**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="df249-110">屬性 GUID</span><span class="sxs-lookup"><span data-stu-id="df249-110">Property GUID</span></span>

<span data-ttu-id="df249-111">**CODECAPI \_ AVEncMPACopyright**</span><span class="sxs-lookup"><span data-stu-id="df249-111">**CODECAPI\_AVEncMPACopyright**</span></span>

## <a name="property-value"></a><span data-ttu-id="df249-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="df249-112">Property value</span></span>

<span data-ttu-id="df249-113">這個屬性可以具有下列值。</span><span class="sxs-lookup"><span data-stu-id="df249-113">This property can have the following values.</span></span>



| <span data-ttu-id="df249-114">值</span><span class="sxs-lookup"><span data-stu-id="df249-114">Value</span></span>          | <span data-ttu-id="df249-115">描述</span><span class="sxs-lookup"><span data-stu-id="df249-115">Description</span></span>           |
|----------------|-----------------------|
| <span data-ttu-id="df249-116">VARIANT \_ FALSE</span><span class="sxs-lookup"><span data-stu-id="df249-116">VARIANT\_FALSE</span></span> | <span data-ttu-id="df249-117">著作權位為 off。</span><span class="sxs-lookup"><span data-stu-id="df249-117">Copyright bit is off.</span></span> |
| <span data-ttu-id="df249-118">VARIANT \_ TRUE</span><span class="sxs-lookup"><span data-stu-id="df249-118">VARIANT\_TRUE</span></span>  | <span data-ttu-id="df249-119">著作權位為開啟。</span><span class="sxs-lookup"><span data-stu-id="df249-119">Copyright bit is on.</span></span>  |



 

## <a name="remarks"></a><span data-ttu-id="df249-120">備註</span><span class="sxs-lookup"><span data-stu-id="df249-120">Remarks</span></span>

<span data-ttu-id="df249-121">編碼器可能會根據輸入資料流程的內容來覆寫此設定。</span><span class="sxs-lookup"><span data-stu-id="df249-121">The encoder might override this setting, based on the contents of the input stream.</span></span>

## <a name="requirements"></a><span data-ttu-id="df249-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="df249-122">Requirements</span></span>



| <span data-ttu-id="df249-123">需求</span><span class="sxs-lookup"><span data-stu-id="df249-123">Requirement</span></span> | <span data-ttu-id="df249-124">值</span><span class="sxs-lookup"><span data-stu-id="df249-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="df249-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="df249-125">Minimum supported client</span></span><br/> | <span data-ttu-id="df249-126">Windows 2000 專業版傳統型 \[ 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="df249-126">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="df249-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="df249-127">Minimum supported server</span></span><br/> | <span data-ttu-id="df249-128">Windows 2000 Server \[ desktop 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="df249-128">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="df249-129">標頭</span><span class="sxs-lookup"><span data-stu-id="df249-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="df249-130"><dt>Codecapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="df249-130"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df249-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="df249-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df249-132">編解碼器 API 屬性</span><span class="sxs-lookup"><span data-stu-id="df249-132">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="df249-133">**ICodecAPI 介面**</span><span class="sxs-lookup"><span data-stu-id="df249-133">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




