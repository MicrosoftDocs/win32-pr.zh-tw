---
description: 傳回允許以限制存取開啟共用資源的進程數目。
ms.assetid: e1b9ef18-fd08-4639-9ba9-4bccd33f5d16
title: 'D3DAUTHENTICATEDQUERY_RESTRICTEDSHAREDRESOURCEPROCESSCOUNT (D3d9types) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_RESTRICTEDSHAREDRESOURCEPROCESSCOUNT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 5238d027b5fe8ed7ebd1ab941b3877d5b545239b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970742"
---
# <a name="d3dauthenticatedquery_restrictedsharedresourceprocesscount"></a><span data-ttu-id="2937c-103">D3DAUTHENTICATEDQUERY \_ RESTRICTEDSHAREDRESOURCEPROCESSCOUNT</span><span class="sxs-lookup"><span data-stu-id="2937c-103">D3DAUTHENTICATEDQUERY\_RESTRICTEDSHAREDRESOURCEPROCESSCOUNT</span></span>

<span data-ttu-id="2937c-104">傳回允許以限制存取開啟共用資源的進程數目。</span><span class="sxs-lookup"><span data-stu-id="2937c-104">Returns the number of processes that are allowed to open shared resources with restricted access.</span></span>



| <span data-ttu-id="2937c-105">需求</span><span class="sxs-lookup"><span data-stu-id="2937c-105">Requirement</span></span> | <span data-ttu-id="2937c-106">值</span><span class="sxs-lookup"><span data-stu-id="2937c-106">Value</span></span> |
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2937c-107">查詢 GUID</span><span class="sxs-lookup"><span data-stu-id="2937c-107">Query GUID</span></span>  | <span data-ttu-id="2937c-108">**D3DAUTHENTICATEDQUERY \_ RESTRICTEDSHAREDRESOURCEPROCESSCOUNT**</span><span class="sxs-lookup"><span data-stu-id="2937c-108">**D3DAUTHENTICATEDQUERY\_RESTRICTEDSHAREDRESOURCEPROCESSCOUNT**</span></span>                                                                                                |
| <span data-ttu-id="2937c-109">輸入資料</span><span class="sxs-lookup"><span data-stu-id="2937c-109">Input data</span></span>  | [<span data-ttu-id="2937c-110">**D3DAUTHENTICATEDCHANNEL \_ 查詢 \_ 輸入**</span><span class="sxs-lookup"><span data-stu-id="2937c-110">**D3DAUTHENTICATEDCHANNEL\_QUERY\_INPUT**</span></span>](d3dauthenticatedchannel-query-input.md)                                                                           |
| <span data-ttu-id="2937c-111">傳回資料</span><span class="sxs-lookup"><span data-stu-id="2937c-111">Return data</span></span> | [<span data-ttu-id="2937c-112">**D3DAUTHENTICATEDCHANNEL \_ QUERYRESTRICTEDSHAREDRESOURCEPROCESSCOUNT \_ 輸出**</span><span class="sxs-lookup"><span data-stu-id="2937c-112">**D3DAUTHENTICATEDCHANNEL\_QUERYRESTRICTEDSHAREDRESOURCEPROCESSCOUNT\_OUTPUT**</span></span>](d3dauthenticatedchannel-queryrestrictedsharedresourceprocesscount-output.md) |



 

## <a name="remarks"></a><span data-ttu-id="2937c-113">備註</span><span class="sxs-lookup"><span data-stu-id="2937c-113">Remarks</span></span>

<span data-ttu-id="2937c-114">下列通道類型支援此查詢：</span><span class="sxs-lookup"><span data-stu-id="2937c-114">The following channel types support this query:</span></span>

-   <span data-ttu-id="2937c-115">**D3DAUTHENTICATEDCHANNEL \_ D3D9**</span><span class="sxs-lookup"><span data-stu-id="2937c-115">**D3DAUTHENTICATEDCHANNEL\_D3D9**</span></span>
-   <span data-ttu-id="2937c-116">**D3DAUTHENTICATEDCHANNEL \_ 驅動程式 \_ 軟體**</span><span class="sxs-lookup"><span data-stu-id="2937c-116">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_SOFTWARE**</span></span>

## <a name="requirements"></a><span data-ttu-id="2937c-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="2937c-117">Requirements</span></span>



| <span data-ttu-id="2937c-118">需求</span><span class="sxs-lookup"><span data-stu-id="2937c-118">Requirement</span></span> | <span data-ttu-id="2937c-119">值</span><span class="sxs-lookup"><span data-stu-id="2937c-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2937c-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2937c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="2937c-121">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2937c-121">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="2937c-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2937c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="2937c-123">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2937c-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="2937c-124">標頭</span><span class="sxs-lookup"><span data-stu-id="2937c-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="2937c-125"><dt>D3d9types。h</dt></span><span class="sxs-lookup"><span data-stu-id="2937c-125"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2937c-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2937c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2937c-127">內容保護查詢</span><span class="sxs-lookup"><span data-stu-id="2937c-127">Content Protection Queries</span></span>](content-protection-queries.md)
</dt> <dt>

[<span data-ttu-id="2937c-128">以 GPU 為基礎的內容保護</span><span class="sxs-lookup"><span data-stu-id="2937c-128">GPU-Based Content Protection</span></span>](gpu-based-content-protection.md)
</dt> <dt>

[<span data-ttu-id="2937c-129">**IDirect3DAuthenticatedChannel9：： Query**</span><span class="sxs-lookup"><span data-stu-id="2937c-129">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




