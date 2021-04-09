---
description: 傳回與指定的密碼編譯會話和 Direct3D 裝置相關聯的輸出識別碼數目。
ms.assetid: a5b17250-6a40-40a9-93b6-3b98b56b09d6
title: 'D3DAUTHENTICATEDQUERY_OUTPUTIDCOUNT (D3d9types) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_OUTPUTIDCOUNT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 624b9ca0ee96f71fb9d3cb655aa9c10030a40efe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689323"
---
# <a name="d3dauthenticatedquery_outputidcount"></a><span data-ttu-id="dd0b1-103">D3DAUTHENTICATEDQUERY \_ OUTPUTIDCOUNT</span><span class="sxs-lookup"><span data-stu-id="dd0b1-103">D3DAUTHENTICATEDQUERY\_OUTPUTIDCOUNT</span></span>

<span data-ttu-id="dd0b1-104">傳回與指定的密碼編譯會話和 Direct3D 裝置相關聯的輸出識別碼數目。</span><span class="sxs-lookup"><span data-stu-id="dd0b1-104">Returns the number of output identifiers associated with a specified cryptographic session and Direct3D device.</span></span>



| <span data-ttu-id="dd0b1-105">需求</span><span class="sxs-lookup"><span data-stu-id="dd0b1-105">Requirement</span></span> | <span data-ttu-id="dd0b1-106">值</span><span class="sxs-lookup"><span data-stu-id="dd0b1-106">Value</span></span> |
|-------------|------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd0b1-107">查詢 GUID</span><span class="sxs-lookup"><span data-stu-id="dd0b1-107">Query GUID</span></span>  | <span data-ttu-id="dd0b1-108">**D3DAUTHENTICATEDQUERY \_ OUTPUTIDCOUNT**</span><span class="sxs-lookup"><span data-stu-id="dd0b1-108">**D3DAUTHENTICATEDQUERY\_OUTPUTIDCOUNT**</span></span>                                                                         |
| <span data-ttu-id="dd0b1-109">輸入資料</span><span class="sxs-lookup"><span data-stu-id="dd0b1-109">Input data</span></span>  | [<span data-ttu-id="dd0b1-110">**D3DAUTHENTICATEDCHANNEL \_ QUERYOUTPUTIDCOUNT \_ 輸入**</span><span class="sxs-lookup"><span data-stu-id="dd0b1-110">**D3DAUTHENTICATEDCHANNEL\_QUERYOUTPUTIDCOUNT\_INPUT**</span></span>](d3dauthenticatedchannel-queryoutputidcount-input.md)   |
| <span data-ttu-id="dd0b1-111">傳回資料</span><span class="sxs-lookup"><span data-stu-id="dd0b1-111">Return data</span></span> | [<span data-ttu-id="dd0b1-112">**D3DAUTHENTICATEDCHANNEL \_ QUERYOUTPUTIDCOUNT \_ 輸出**</span><span class="sxs-lookup"><span data-stu-id="dd0b1-112">**D3DAUTHENTICATEDCHANNEL\_QUERYOUTPUTIDCOUNT\_OUTPUT**</span></span>](d3dauthenticatedchannel-queryoutputidcount-output.md) |



 

## <a name="remarks"></a><span data-ttu-id="dd0b1-113">備註</span><span class="sxs-lookup"><span data-stu-id="dd0b1-113">Remarks</span></span>

<span data-ttu-id="dd0b1-114">下列通道類型支援此查詢：</span><span class="sxs-lookup"><span data-stu-id="dd0b1-114">The following channel types support this query:</span></span>

-   <span data-ttu-id="dd0b1-115">**D3DAUTHENTICATEDCHANNEL \_ 驅動程式 \_ 硬體**</span><span class="sxs-lookup"><span data-stu-id="dd0b1-115">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_HARDWARE**</span></span>
-   <span data-ttu-id="dd0b1-116">**D3DAUTHENTICATEDCHANNEL \_ 驅動程式 \_ 軟體**</span><span class="sxs-lookup"><span data-stu-id="dd0b1-116">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_SOFTWARE**</span></span>

## <a name="requirements"></a><span data-ttu-id="dd0b1-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="dd0b1-117">Requirements</span></span>



| <span data-ttu-id="dd0b1-118">需求</span><span class="sxs-lookup"><span data-stu-id="dd0b1-118">Requirement</span></span> | <span data-ttu-id="dd0b1-119">值</span><span class="sxs-lookup"><span data-stu-id="dd0b1-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="dd0b1-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="dd0b1-120">Minimum supported client</span></span><br/> | <span data-ttu-id="dd0b1-121">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dd0b1-121">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="dd0b1-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="dd0b1-122">Minimum supported server</span></span><br/> | <span data-ttu-id="dd0b1-123">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dd0b1-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="dd0b1-124">標頭</span><span class="sxs-lookup"><span data-stu-id="dd0b1-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="dd0b1-125"><dt>D3d9types。h</dt></span><span class="sxs-lookup"><span data-stu-id="dd0b1-125"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dd0b1-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dd0b1-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd0b1-127">內容保護查詢</span><span class="sxs-lookup"><span data-stu-id="dd0b1-127">Content Protection Queries</span></span>](content-protection-queries.md)
</dt> <dt>

[<span data-ttu-id="dd0b1-128">以 GPU 為基礎的內容保護</span><span class="sxs-lookup"><span data-stu-id="dd0b1-128">GPU-Based Content Protection</span></span>](gpu-based-content-protection.md)
</dt> <dt>

[<span data-ttu-id="dd0b1-129">**IDirect3DAuthenticatedChannel9：： Query**</span><span class="sxs-lookup"><span data-stu-id="dd0b1-129">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




