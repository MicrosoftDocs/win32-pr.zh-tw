---
description: 傳回用來將資料傳送至 GPU 的 i/o 匯流排類型。
ms.assetid: 5a180a5c-6798-40ba-9e2c-ce1f755fcc08
title: 'D3DAUTHENTICATEDQUERY_ACCESSIBILITYATTRIBUTES (D3d9types) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_ACCESSIBILITYATTRIBUTES
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 5119da4e7efaf0c27db1065dacc56e3388a77474
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104386036"
---
# <a name="d3dauthenticatedquery_accessibilityattributes"></a><span data-ttu-id="3b7aa-103">D3DAUTHENTICATEDQUERY \_ ACCESSIBILITYATTRIBUTES</span><span class="sxs-lookup"><span data-stu-id="3b7aa-103">D3DAUTHENTICATEDQUERY\_ACCESSIBILITYATTRIBUTES</span></span>

<span data-ttu-id="3b7aa-104">傳回用來將資料傳送至 GPU 的 i/o 匯流排類型。</span><span class="sxs-lookup"><span data-stu-id="3b7aa-104">Returns the type of I/O bus used to send data to the GPU.</span></span>



| <span data-ttu-id="3b7aa-105">需求</span><span class="sxs-lookup"><span data-stu-id="3b7aa-105">Requirement</span></span> | <span data-ttu-id="3b7aa-106">值</span><span class="sxs-lookup"><span data-stu-id="3b7aa-106">Value</span></span> |
|-------------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b7aa-107">查詢 GUID</span><span class="sxs-lookup"><span data-stu-id="3b7aa-107">Query GUID</span></span>  | <span data-ttu-id="3b7aa-108">**D3DAUTHENTICATEDQUERY \_ ACCESSIBILITYATTRIBUTES**</span><span class="sxs-lookup"><span data-stu-id="3b7aa-108">**D3DAUTHENTICATEDQUERY\_ACCESSIBILITYATTRIBUTES**</span></span>                                                           |
| <span data-ttu-id="3b7aa-109">輸入資料</span><span class="sxs-lookup"><span data-stu-id="3b7aa-109">Input data</span></span>  | [<span data-ttu-id="3b7aa-110">**D3DAUTHENTICATEDCHANNEL \_ 查詢 \_ 輸入**</span><span class="sxs-lookup"><span data-stu-id="3b7aa-110">**D3DAUTHENTICATEDCHANNEL\_QUERY\_INPUT**</span></span>](d3dauthenticatedchannel-query-input.md)                         |
| <span data-ttu-id="3b7aa-111">傳回資料</span><span class="sxs-lookup"><span data-stu-id="3b7aa-111">Return data</span></span> | [<span data-ttu-id="3b7aa-112">**D3DAUTHENTICATEDCHANNEL \_ QUERYINFOBUSTYPE \_ 輸出**</span><span class="sxs-lookup"><span data-stu-id="3b7aa-112">**D3DAUTHENTICATEDCHANNEL\_QUERYINFOBUSTYPE\_OUTPUT**</span></span>](d3dauthenticatedchannel-queryinfobustype-output.md) |



 

## <a name="remarks"></a><span data-ttu-id="3b7aa-113">備註</span><span class="sxs-lookup"><span data-stu-id="3b7aa-113">Remarks</span></span>

<span data-ttu-id="3b7aa-114">此查詢也會傳回將內容放入視訊記憶體時可存取的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="3b7aa-114">This query also returns information about how accessible the content is when put into video memory.</span></span>

<span data-ttu-id="3b7aa-115">下列通道類型支援此查詢：</span><span class="sxs-lookup"><span data-stu-id="3b7aa-115">The following channel types support this query:</span></span>

-   <span data-ttu-id="3b7aa-116">**D3DAUTHENTICATEDCHANNEL \_ 驅動程式 \_ 硬體**</span><span class="sxs-lookup"><span data-stu-id="3b7aa-116">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_HARDWARE**</span></span>
-   <span data-ttu-id="3b7aa-117">**D3DAUTHENTICATEDCHANNEL \_ 驅動程式 \_ 軟體**</span><span class="sxs-lookup"><span data-stu-id="3b7aa-117">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_SOFTWARE**</span></span>

## <a name="requirements"></a><span data-ttu-id="3b7aa-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="3b7aa-118">Requirements</span></span>



| <span data-ttu-id="3b7aa-119">需求</span><span class="sxs-lookup"><span data-stu-id="3b7aa-119">Requirement</span></span> | <span data-ttu-id="3b7aa-120">值</span><span class="sxs-lookup"><span data-stu-id="3b7aa-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3b7aa-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3b7aa-121">Minimum supported client</span></span><br/> | <span data-ttu-id="3b7aa-122">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3b7aa-122">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="3b7aa-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3b7aa-123">Minimum supported server</span></span><br/> | <span data-ttu-id="3b7aa-124">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3b7aa-124">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="3b7aa-125">標頭</span><span class="sxs-lookup"><span data-stu-id="3b7aa-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="3b7aa-126"><dt>D3d9types。h</dt></span><span class="sxs-lookup"><span data-stu-id="3b7aa-126"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b7aa-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3b7aa-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b7aa-128">內容保護查詢</span><span class="sxs-lookup"><span data-stu-id="3b7aa-128">Content Protection Queries</span></span>](content-protection-queries.md)
</dt> <dt>

[<span data-ttu-id="3b7aa-129">以 GPU 為基礎的內容保護</span><span class="sxs-lookup"><span data-stu-id="3b7aa-129">GPU-Based Content Protection</span></span>](gpu-based-content-protection.md)
</dt> <dt>

[<span data-ttu-id="3b7aa-130">**IDirect3DAuthenticatedChannel9：： Query**</span><span class="sxs-lookup"><span data-stu-id="3b7aa-130">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




