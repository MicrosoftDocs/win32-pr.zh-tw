---
description: 傳回允許以限制存取開啟共用資源之進程的相關資訊。
ms.assetid: 669d9623-3a96-4661-9dae-3f283a990fe8
title: 'D3DAUTHENTICATEDQUERY_RESTRICTEDSHAREDRESOURCEPROCESS (D3d9types) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_RESTRICTEDSHAREDRESOURCEPROCESS
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 74bb829510fee4425648412f58d4f7cea74b1f72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106985594"
---
# <a name="d3dauthenticatedquery_restrictedsharedresourceprocess"></a><span data-ttu-id="ee0dc-103">D3DAUTHENTICATEDQUERY \_ RESTRICTEDSHAREDRESOURCEPROCESS</span><span class="sxs-lookup"><span data-stu-id="ee0dc-103">D3DAUTHENTICATEDQUERY\_RESTRICTEDSHAREDRESOURCEPROCESS</span></span>

<span data-ttu-id="ee0dc-104">傳回允許以限制存取開啟共用資源之進程的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="ee0dc-104">Returns information about a process that is allowed to open shared resources with restricted access.</span></span>



| <span data-ttu-id="ee0dc-105">需求</span><span class="sxs-lookup"><span data-stu-id="ee0dc-105">Requirement</span></span> | <span data-ttu-id="ee0dc-106">值</span><span class="sxs-lookup"><span data-stu-id="ee0dc-106">Value</span></span> |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee0dc-107">查詢 GUID</span><span class="sxs-lookup"><span data-stu-id="ee0dc-107">Query GUID</span></span>  | <span data-ttu-id="ee0dc-108">**D3DAUTHENTICATEDQUERY \_ RESTRICTEDSHAREDRESOURCEPROCESS**</span><span class="sxs-lookup"><span data-stu-id="ee0dc-108">**D3DAUTHENTICATEDQUERY\_RESTRICTEDSHAREDRESOURCEPROCESS**</span></span>                                                                                           |
| <span data-ttu-id="ee0dc-109">輸入資料</span><span class="sxs-lookup"><span data-stu-id="ee0dc-109">Input data</span></span>  | [<span data-ttu-id="ee0dc-110">**D3DAUTHENTICATEDCHANNEL \_ QUERYRESTRICTEDSHAREDRESOURCEPROCESS \_ 輸入**</span><span class="sxs-lookup"><span data-stu-id="ee0dc-110">**D3DAUTHENTICATEDCHANNEL\_QUERYRESTRICTEDSHAREDRESOURCEPROCESS\_INPUT**</span></span>](d3dauthenticatedchannel-queryrestrictedsharedresourceprocess-input.md)   |
| <span data-ttu-id="ee0dc-111">傳回資料</span><span class="sxs-lookup"><span data-stu-id="ee0dc-111">Return data</span></span> | [<span data-ttu-id="ee0dc-112">**D3DAUTHENTICATEDCHANNEL \_ QUERYRESTRICTEDSHAREDRESOURCEPROCESS \_ 輸出**</span><span class="sxs-lookup"><span data-stu-id="ee0dc-112">**D3DAUTHENTICATEDCHANNEL\_QUERYRESTRICTEDSHAREDRESOURCEPROCESS\_OUTPUT**</span></span>](d3dauthenticatedchannel-queryrestrictedsharedresourceprocess-output.md) |



 

## <a name="remarks"></a><span data-ttu-id="ee0dc-113">備註</span><span class="sxs-lookup"><span data-stu-id="ee0dc-113">Remarks</span></span>

<span data-ttu-id="ee0dc-114">下列通道類型支援此查詢：</span><span class="sxs-lookup"><span data-stu-id="ee0dc-114">The following channel types support this query:</span></span>

-   <span data-ttu-id="ee0dc-115">**D3DAUTHENTICATEDCHANNEL \_ D3D9**</span><span class="sxs-lookup"><span data-stu-id="ee0dc-115">**D3DAUTHENTICATEDCHANNEL\_D3D9**</span></span>
-   <span data-ttu-id="ee0dc-116">**D3DAUTHENTICATEDCHANNEL \_ 驅動程式 \_ 軟體**</span><span class="sxs-lookup"><span data-stu-id="ee0dc-116">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_SOFTWARE**</span></span>

## <a name="requirements"></a><span data-ttu-id="ee0dc-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="ee0dc-117">Requirements</span></span>



| <span data-ttu-id="ee0dc-118">需求</span><span class="sxs-lookup"><span data-stu-id="ee0dc-118">Requirement</span></span> | <span data-ttu-id="ee0dc-119">值</span><span class="sxs-lookup"><span data-stu-id="ee0dc-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ee0dc-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ee0dc-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ee0dc-121">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ee0dc-121">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="ee0dc-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ee0dc-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ee0dc-123">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ee0dc-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="ee0dc-124">標頭</span><span class="sxs-lookup"><span data-stu-id="ee0dc-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="ee0dc-125"><dt>D3d9types。h</dt></span><span class="sxs-lookup"><span data-stu-id="ee0dc-125"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee0dc-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ee0dc-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee0dc-127">內容保護查詢</span><span class="sxs-lookup"><span data-stu-id="ee0dc-127">Content Protection Queries</span></span>](content-protection-queries.md)
</dt> <dt>

[<span data-ttu-id="ee0dc-128">以 GPU 為基礎的內容保護</span><span class="sxs-lookup"><span data-stu-id="ee0dc-128">GPU-Based Content Protection</span></span>](gpu-based-content-protection.md)
</dt> <dt>

[<span data-ttu-id="ee0dc-129">**IDirect3DAuthenticatedChannel9：： Query**</span><span class="sxs-lookup"><span data-stu-id="ee0dc-129">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




