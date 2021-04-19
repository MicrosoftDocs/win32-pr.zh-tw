---
description: 傳回任何進程可以開啟的受保護共用資源數目，而不受限制。
ms.assetid: afbd7bb9-de71-4992-919e-e1517228dc69
title: 'D3DAUTHENTICATEDQUERY_UNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT (D3d9types) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_UNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: b2d834927d21c59ed5c70dcf3a001d100340405d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973195"
---
# <a name="d3dauthenticatedquery_unrestrictedprotectedsharedresourcecount"></a><span data-ttu-id="836f1-103">D3DAUTHENTICATEDQUERY \_ UNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT</span><span class="sxs-lookup"><span data-stu-id="836f1-103">D3DAUTHENTICATEDQUERY\_UNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT</span></span>

<span data-ttu-id="836f1-104">傳回任何進程可以開啟的受保護共用資源數目，而不受限制。</span><span class="sxs-lookup"><span data-stu-id="836f1-104">Returns the number of protected shared resources that can be opened by any process without restrictions.</span></span>



| <span data-ttu-id="836f1-105">需求</span><span class="sxs-lookup"><span data-stu-id="836f1-105">Requirement</span></span> | <span data-ttu-id="836f1-106">值</span><span class="sxs-lookup"><span data-stu-id="836f1-106">Value</span></span> |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="836f1-107">查詢 GUID</span><span class="sxs-lookup"><span data-stu-id="836f1-107">Query GUID</span></span>  | <span data-ttu-id="836f1-108">**D3DAUTHENTICATEDQUERY \_ UNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT**</span><span class="sxs-lookup"><span data-stu-id="836f1-108">**D3DAUTHENTICATEDQUERY\_UNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT**</span></span>                                                                                                    |
| <span data-ttu-id="836f1-109">輸入資料</span><span class="sxs-lookup"><span data-stu-id="836f1-109">Input data</span></span>  | [<span data-ttu-id="836f1-110">**D3DAUTHENTICATEDCHANNEL \_ 查詢 \_ 輸入**</span><span class="sxs-lookup"><span data-stu-id="836f1-110">**D3DAUTHENTICATEDCHANNEL\_QUERY\_INPUT**</span></span>](d3dauthenticatedchannel-query-input.md)                                                                                   |
| <span data-ttu-id="836f1-111">傳回資料</span><span class="sxs-lookup"><span data-stu-id="836f1-111">Return data</span></span> | [<span data-ttu-id="836f1-112">**D3DAUTHENTICATEDCHANNEL \_ QUERYUNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT \_ 輸出**</span><span class="sxs-lookup"><span data-stu-id="836f1-112">**D3DAUTHENTICATEDCHANNEL\_QUERYUNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT\_OUTPUT**</span></span>](d3dauthenticatedchannel-queryunrestrictedprotectedsharedresourcecount-output.md) |



 

## <a name="remarks"></a><span data-ttu-id="836f1-113">備註</span><span class="sxs-lookup"><span data-stu-id="836f1-113">Remarks</span></span>

<span data-ttu-id="836f1-114">唯一支援此查詢的通道類型是 **D3DAUTHENTICATEDCHANNEL \_ 驅動程式 \_ 軟體**。</span><span class="sxs-lookup"><span data-stu-id="836f1-114">The only channel type that supports this query is **D3DAUTHENTICATEDCHANNEL\_DRIVER\_SOFTWARE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="836f1-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="836f1-115">Requirements</span></span>



| <span data-ttu-id="836f1-116">需求</span><span class="sxs-lookup"><span data-stu-id="836f1-116">Requirement</span></span> | <span data-ttu-id="836f1-117">值</span><span class="sxs-lookup"><span data-stu-id="836f1-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="836f1-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="836f1-118">Minimum supported client</span></span><br/> | <span data-ttu-id="836f1-119">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="836f1-119">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="836f1-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="836f1-120">Minimum supported server</span></span><br/> | <span data-ttu-id="836f1-121">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="836f1-121">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="836f1-122">標頭</span><span class="sxs-lookup"><span data-stu-id="836f1-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="836f1-123"><dt>D3d9types。h</dt></span><span class="sxs-lookup"><span data-stu-id="836f1-123"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="836f1-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="836f1-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="836f1-125">內容保護查詢</span><span class="sxs-lookup"><span data-stu-id="836f1-125">Content Protection Queries</span></span>](content-protection-queries.md)
</dt> <dt>

[<span data-ttu-id="836f1-126">以 GPU 為基礎的內容保護</span><span class="sxs-lookup"><span data-stu-id="836f1-126">GPU-Based Content Protection</span></span>](gpu-based-content-protection.md)
</dt> <dt>

[<span data-ttu-id="836f1-127">**IDirect3DAuthenticatedChannel9：： Query**</span><span class="sxs-lookup"><span data-stu-id="836f1-127">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




