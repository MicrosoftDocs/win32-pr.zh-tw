---
description: 傳回可供 CPU 或匯流排存取之前，用來加密內容的其中一種加密類型。
ms.assetid: 263c6f00-8bc9-4e9c-8b98-fb8f87c6c008
title: 'D3DAUTHENTICATEDQUERY_ENCRYPTIONWHENACCESSIBLEGUID (D3d9types) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_ENCRYPTIONWHENACCESSIBLEGUID
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: b5755a2707ec9d7440cda9b4692eed36ac6deff1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106998053"
---
# <a name="d3dauthenticatedquery_encryptionwhenaccessibleguid"></a><span data-ttu-id="769b4-103">D3DAUTHENTICATEDQUERY \_ ENCRYPTIONWHENACCESSIBLEGUID</span><span class="sxs-lookup"><span data-stu-id="769b4-103">D3DAUTHENTICATEDQUERY\_ENCRYPTIONWHENACCESSIBLEGUID</span></span>

<span data-ttu-id="769b4-104">傳回可供 CPU 或匯流排存取之前，用來加密內容的其中一種加密類型。</span><span class="sxs-lookup"><span data-stu-id="769b4-104">Returns one of the encryption types that can be used to encrypt content before it becomes accessible to the CPU or bus.</span></span>



| <span data-ttu-id="769b4-105">需求</span><span class="sxs-lookup"><span data-stu-id="769b4-105">Requirement</span></span> | <span data-ttu-id="769b4-106">值</span><span class="sxs-lookup"><span data-stu-id="769b4-106">Value</span></span> |
|-------------|------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="769b4-107">查詢 GUID</span><span class="sxs-lookup"><span data-stu-id="769b4-107">Query GUID</span></span>  | <span data-ttu-id="769b4-108">**D3DAUTHENTICATEDQUERY \_ ENCRYPTIONWHENACCESSIBLEGUID**</span><span class="sxs-lookup"><span data-stu-id="769b4-108">**D3DAUTHENTICATEDQUERY\_ENCRYPTIONWHENACCESSIBLEGUID**</span></span>                                                                            |
| <span data-ttu-id="769b4-109">輸入資料</span><span class="sxs-lookup"><span data-stu-id="769b4-109">Input data</span></span>  | [<span data-ttu-id="769b4-110">**D3DAUTHENTICATEDCHANNEL \_ QUERYEVICTIONENCRYPTIONGUID \_ 輸入**</span><span class="sxs-lookup"><span data-stu-id="769b4-110">**D3DAUTHENTICATEDCHANNEL\_QUERYEVICTIONENCRYPTIONGUID\_INPUT**</span></span>](d3dauthenticatedchannel-queryevictionencryptionguid-input.md)   |
| <span data-ttu-id="769b4-111">傳回資料</span><span class="sxs-lookup"><span data-stu-id="769b4-111">Return data</span></span> | [<span data-ttu-id="769b4-112">**D3DAUTHENTICATEDCHANNEL \_ QUERYEVICTIONENCRYPTIONGUID \_ 輸出**</span><span class="sxs-lookup"><span data-stu-id="769b4-112">**D3DAUTHENTICATEDCHANNEL\_QUERYEVICTIONENCRYPTIONGUID\_OUTPUT**</span></span>](d3dauthenticatedchannel-queryevictionencryptionguid-output.md) |



 

## <a name="remarks"></a><span data-ttu-id="769b4-113">備註</span><span class="sxs-lookup"><span data-stu-id="769b4-113">Remarks</span></span>

<span data-ttu-id="769b4-114">下列通道類型支援此查詢：</span><span class="sxs-lookup"><span data-stu-id="769b4-114">The following channel types support this query:</span></span>

-   <span data-ttu-id="769b4-115">**D3DAUTHENTICATEDCHANNEL \_ 驅動程式 \_ 硬體**</span><span class="sxs-lookup"><span data-stu-id="769b4-115">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_HARDWARE**</span></span>
-   <span data-ttu-id="769b4-116">**D3DAUTHENTICATEDCHANNEL \_ 驅動程式 \_ 軟體**</span><span class="sxs-lookup"><span data-stu-id="769b4-116">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_SOFTWARE**</span></span>

## <a name="requirements"></a><span data-ttu-id="769b4-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="769b4-117">Requirements</span></span>



| <span data-ttu-id="769b4-118">需求</span><span class="sxs-lookup"><span data-stu-id="769b4-118">Requirement</span></span> | <span data-ttu-id="769b4-119">值</span><span class="sxs-lookup"><span data-stu-id="769b4-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="769b4-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="769b4-120">Minimum supported client</span></span><br/> | <span data-ttu-id="769b4-121">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="769b4-121">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="769b4-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="769b4-122">Minimum supported server</span></span><br/> | <span data-ttu-id="769b4-123">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="769b4-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="769b4-124">標頭</span><span class="sxs-lookup"><span data-stu-id="769b4-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="769b4-125"><dt>D3d9types。h</dt></span><span class="sxs-lookup"><span data-stu-id="769b4-125"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="769b4-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="769b4-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="769b4-127">內容保護查詢</span><span class="sxs-lookup"><span data-stu-id="769b4-127">Content Protection Queries</span></span>](content-protection-queries.md)
</dt> <dt>

[<span data-ttu-id="769b4-128">以 GPU 為基礎的內容保護</span><span class="sxs-lookup"><span data-stu-id="769b4-128">GPU-Based Content Protection</span></span>](gpu-based-content-protection.md)
</dt> <dt>

[<span data-ttu-id="769b4-129">**IDirect3DAuthenticatedChannel9：： Query**</span><span class="sxs-lookup"><span data-stu-id="769b4-129">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




