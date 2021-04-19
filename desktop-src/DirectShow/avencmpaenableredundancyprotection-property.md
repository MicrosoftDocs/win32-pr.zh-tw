---
description: 指定是否要將迴圈冗余檢查 (CRC) 新增至框架頁首。 這個屬性會套用至 MPEG 音訊編碼器。
ms.assetid: 55f0de8b-26dd-4d48-b7ed-2ddcef630227
title: 'AVEncMPAEnableRedundancyProtection 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2028b5adaad55d46cc53c61f9d65a73819cc899
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106972931"
---
# <a name="avencmpaenableredundancyprotection-property"></a><span data-ttu-id="80499-104">AVEncMPAEnableRedundancyProtection 屬性</span><span class="sxs-lookup"><span data-stu-id="80499-104">AVEncMPAEnableRedundancyProtection property</span></span>

<span data-ttu-id="80499-105">指定是否要將迴圈冗余檢查 (CRC) 新增至框架頁首。</span><span class="sxs-lookup"><span data-stu-id="80499-105">Specifies whether to add a cyclic redundancy check (CRC) to the frame header.</span></span> <span data-ttu-id="80499-106">這個屬性會套用至 MPEG 音訊編碼器。</span><span class="sxs-lookup"><span data-stu-id="80499-106">This property applies to MPEG audio encoders.</span></span>

<span data-ttu-id="80499-107">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="80499-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="80499-108">資料類型</span><span class="sxs-lookup"><span data-stu-id="80499-108">Data type</span></span>

<span data-ttu-id="80499-109">**變異 \_BOOL** (**VT \_ bool**) </span><span class="sxs-lookup"><span data-stu-id="80499-109">**VARIANT\_BOOL** (**VT\_BOOL**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="80499-110">屬性 GUID</span><span class="sxs-lookup"><span data-stu-id="80499-110">Property GUID</span></span>

<span data-ttu-id="80499-111">**CODECAPI \_ AVEncMPAEnableRedundancyProtection**</span><span class="sxs-lookup"><span data-stu-id="80499-111">**CODECAPI\_AVEncMPAEnableRedundancyProtection**</span></span>

## <a name="property-value"></a><span data-ttu-id="80499-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="80499-112">Property value</span></span>

<span data-ttu-id="80499-113">這個屬性可以具有下列值。</span><span class="sxs-lookup"><span data-stu-id="80499-113">This property can have the following values.</span></span>



| <span data-ttu-id="80499-114">值</span><span class="sxs-lookup"><span data-stu-id="80499-114">Value</span></span>          | <span data-ttu-id="80499-115">描述</span><span class="sxs-lookup"><span data-stu-id="80499-115">Description</span></span>                |
|----------------|----------------------------|
| <span data-ttu-id="80499-116">VARIANT \_ FALSE</span><span class="sxs-lookup"><span data-stu-id="80499-116">VARIANT\_FALSE</span></span> | <span data-ttu-id="80499-117">請勿加入 CRC 總和檢查碼。</span><span class="sxs-lookup"><span data-stu-id="80499-117">Do not add a CRC checksum.</span></span> |
| <span data-ttu-id="80499-118">VARIANT \_ TRUE</span><span class="sxs-lookup"><span data-stu-id="80499-118">VARIANT\_TRUE</span></span>  | <span data-ttu-id="80499-119">加入 CRC 總和檢查碼。</span><span class="sxs-lookup"><span data-stu-id="80499-119">Add a CRC checksum.</span></span>        |



 

## <a name="requirements"></a><span data-ttu-id="80499-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="80499-120">Requirements</span></span>



| <span data-ttu-id="80499-121">需求</span><span class="sxs-lookup"><span data-stu-id="80499-121">Requirement</span></span> | <span data-ttu-id="80499-122">值</span><span class="sxs-lookup"><span data-stu-id="80499-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="80499-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="80499-123">Minimum supported client</span></span><br/> | <span data-ttu-id="80499-124">Windows 2000 專業版傳統型 \[ 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="80499-124">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="80499-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="80499-125">Minimum supported server</span></span><br/> | <span data-ttu-id="80499-126">Windows 2000 Server \[ desktop 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="80499-126">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="80499-127">標頭</span><span class="sxs-lookup"><span data-stu-id="80499-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="80499-128"><dt>Codecapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="80499-128"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="80499-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="80499-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80499-130">編解碼器 API 屬性</span><span class="sxs-lookup"><span data-stu-id="80499-130">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="80499-131">**ICodecAPI 介面**</span><span class="sxs-lookup"><span data-stu-id="80499-131">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




