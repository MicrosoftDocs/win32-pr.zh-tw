---
description: 傳回可供 CPU 或匯流排存取之前，用來加密內容的加密類型數目。
ms.assetid: 442b80f5-8467-427d-a01e-5d22f6ddafea
title: 'D3DAUTHENTICATEDQUERY_ENCRYPTIONWHENACCESSIBLEGUIDCOUNT (D3d9types) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_ENCRYPTIONWHENACCESSIBLEGUIDCOUNT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 9cd281836436c1d11fe07f7a43ecceebc8e3b12e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689327"
---
# <a name="d3dauthenticatedquery_encryptionwhenaccessibleguidcount"></a><span data-ttu-id="98d95-103">D3DAUTHENTICATEDQUERY \_ ENCRYPTIONWHENACCESSIBLEGUIDCOUNT</span><span class="sxs-lookup"><span data-stu-id="98d95-103">D3DAUTHENTICATEDQUERY\_ENCRYPTIONWHENACCESSIBLEGUIDCOUNT</span></span>

<span data-ttu-id="98d95-104">傳回可供 CPU 或匯流排存取之前，用來加密內容的加密類型數目。</span><span class="sxs-lookup"><span data-stu-id="98d95-104">Returns the number of encryption types that can be used to encrypt content before it becomes accessible to the CPU or bus.</span></span>



| <span data-ttu-id="98d95-105">需求</span><span class="sxs-lookup"><span data-stu-id="98d95-105">Requirement</span></span> | <span data-ttu-id="98d95-106">值</span><span class="sxs-lookup"><span data-stu-id="98d95-106">Value</span></span> |
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="98d95-107">查詢 GUID</span><span class="sxs-lookup"><span data-stu-id="98d95-107">Query GUID</span></span>  | <span data-ttu-id="98d95-108">**D3DAUTHENTICATEDQUERY \_ ENCRYPTIONWHENACCESSIBLEGUIDCOUNT**</span><span class="sxs-lookup"><span data-stu-id="98d95-108">**D3DAUTHENTICATEDQUERY\_ENCRYPTIONWHENACCESSIBLEGUIDCOUNT**</span></span>                                                                                 |
| <span data-ttu-id="98d95-109">輸入資料</span><span class="sxs-lookup"><span data-stu-id="98d95-109">Input data</span></span>  | [<span data-ttu-id="98d95-110">**D3DAUTHENTICATEDCHANNEL \_ 查詢 \_ 輸入**</span><span class="sxs-lookup"><span data-stu-id="98d95-110">**D3DAUTHENTICATEDCHANNEL\_QUERY\_INPUT**</span></span>](d3dauthenticatedchannel-query-input.md)                                                         |
| <span data-ttu-id="98d95-111">傳回資料</span><span class="sxs-lookup"><span data-stu-id="98d95-111">Return data</span></span> | [<span data-ttu-id="98d95-112">**D3DAUTHENTICATEDCHANNEL \_ QUERYEVICTIONENCRYPTIONGUIDCOUNT \_ 輸出**</span><span class="sxs-lookup"><span data-stu-id="98d95-112">**D3DAUTHENTICATEDCHANNEL\_QUERYEVICTIONENCRYPTIONGUIDCOUNT\_OUTPUT**</span></span>](d3dauthenticatedchannel-queryevictionencryptionguidcount-output.md) |



 

## <a name="remarks"></a><span data-ttu-id="98d95-113">備註</span><span class="sxs-lookup"><span data-stu-id="98d95-113">Remarks</span></span>

<span data-ttu-id="98d95-114">下列通道類型支援此查詢：</span><span class="sxs-lookup"><span data-stu-id="98d95-114">The following channel types support this query:</span></span>

-   <span data-ttu-id="98d95-115">**D3DAUTHENTICATEDCHANNEL \_ 驅動程式 \_ 硬體**</span><span class="sxs-lookup"><span data-stu-id="98d95-115">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_HARDWARE**</span></span>
-   <span data-ttu-id="98d95-116">**D3DAUTHENTICATEDCHANNEL \_ 驅動程式 \_ 軟體**</span><span class="sxs-lookup"><span data-stu-id="98d95-116">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_SOFTWARE**</span></span>

## <a name="requirements"></a><span data-ttu-id="98d95-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="98d95-117">Requirements</span></span>



| <span data-ttu-id="98d95-118">需求</span><span class="sxs-lookup"><span data-stu-id="98d95-118">Requirement</span></span> | <span data-ttu-id="98d95-119">值</span><span class="sxs-lookup"><span data-stu-id="98d95-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="98d95-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="98d95-120">Minimum supported client</span></span><br/> | <span data-ttu-id="98d95-121">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="98d95-121">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="98d95-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="98d95-122">Minimum supported server</span></span><br/> | <span data-ttu-id="98d95-123">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="98d95-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="98d95-124">標頭</span><span class="sxs-lookup"><span data-stu-id="98d95-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="98d95-125"><dt>D3d9types。h</dt></span><span class="sxs-lookup"><span data-stu-id="98d95-125"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98d95-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="98d95-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98d95-127">內容保護查詢</span><span class="sxs-lookup"><span data-stu-id="98d95-127">Content Protection Queries</span></span>](content-protection-queries.md)
</dt> <dt>

[<span data-ttu-id="98d95-128">以 GPU 為基礎的內容保護</span><span class="sxs-lookup"><span data-stu-id="98d95-128">GPU-Based Content Protection</span></span>](gpu-based-content-protection.md)
</dt> <dt>

[<span data-ttu-id="98d95-129">**IDirect3DAuthenticatedChannel9：： Query**</span><span class="sxs-lookup"><span data-stu-id="98d95-129">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




