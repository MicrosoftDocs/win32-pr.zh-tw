---
description: 傳回與指定的密碼編譯會話和 Direct3D 裝置相關聯的其中一個輸出識別碼。
ms.assetid: 7b56055a-fb36-4e54-9bee-ab9401b09267
title: 'D3DAUTHENTICATEDQUERY_OUTPUTID (D3d9types) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_OUTPUTID
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: fa970ae6e7b10f553679376d7a924d1c8b67c595
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689324"
---
# <a name="d3dauthenticatedquery_outputid"></a><span data-ttu-id="65717-103">D3DAUTHENTICATEDQUERY \_ OUTPUTID</span><span class="sxs-lookup"><span data-stu-id="65717-103">D3DAUTHENTICATEDQUERY\_OUTPUTID</span></span>

<span data-ttu-id="65717-104">傳回與指定的密碼編譯會話和 Direct3D 裝置相關聯的其中一個輸出識別碼。</span><span class="sxs-lookup"><span data-stu-id="65717-104">Returns one of the output identifiers that is associated with a specified cryptographic session and Direct3D device.</span></span>



| <span data-ttu-id="65717-105">需求</span><span class="sxs-lookup"><span data-stu-id="65717-105">Requirement</span></span> | <span data-ttu-id="65717-106">值</span><span class="sxs-lookup"><span data-stu-id="65717-106">Value</span></span> |
|-------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="65717-107">查詢 GUID</span><span class="sxs-lookup"><span data-stu-id="65717-107">Query GUID</span></span>  | <span data-ttu-id="65717-108">**D3DAUTHENTICATEDQUERY \_ OUTPUTID**</span><span class="sxs-lookup"><span data-stu-id="65717-108">**D3DAUTHENTICATEDQUERY\_OUTPUTID**</span></span>                                                                    |
| <span data-ttu-id="65717-109">輸入資料</span><span class="sxs-lookup"><span data-stu-id="65717-109">Input data</span></span>  | [<span data-ttu-id="65717-110">**D3DAUTHENTICATEDCHANNEL \_ QUERYOUTPUTID \_ 輸入**</span><span class="sxs-lookup"><span data-stu-id="65717-110">**D3DAUTHENTICATEDCHANNEL\_QUERYOUTPUTID\_INPUT**</span></span>](d3dauthenticatedchannel-queryoutputid-input.md)   |
| <span data-ttu-id="65717-111">傳回資料</span><span class="sxs-lookup"><span data-stu-id="65717-111">Return data</span></span> | [<span data-ttu-id="65717-112">**D3DAUTHENTICATEDCHANNEL \_ QUERYOUTPUTID \_ 輸出**</span><span class="sxs-lookup"><span data-stu-id="65717-112">**D3DAUTHENTICATEDCHANNEL\_QUERYOUTPUTID\_OUTPUT**</span></span>](d3dauthenticatedchannel-queryoutputid-output.md) |



 

## <a name="remarks"></a><span data-ttu-id="65717-113">備註</span><span class="sxs-lookup"><span data-stu-id="65717-113">Remarks</span></span>

<span data-ttu-id="65717-114">下列通道類型支援此查詢：</span><span class="sxs-lookup"><span data-stu-id="65717-114">The following channel types support this query:</span></span>

-   <span data-ttu-id="65717-115">**D3DAUTHENTICATEDCHANNEL \_ 驅動程式 \_ 硬體**</span><span class="sxs-lookup"><span data-stu-id="65717-115">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_HARDWARE**</span></span>
-   <span data-ttu-id="65717-116">**D3DAUTHENTICATEDCHANNEL \_ 驅動程式 \_ 軟體**</span><span class="sxs-lookup"><span data-stu-id="65717-116">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_SOFTWARE**</span></span>

## <a name="requirements"></a><span data-ttu-id="65717-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="65717-117">Requirements</span></span>



| <span data-ttu-id="65717-118">需求</span><span class="sxs-lookup"><span data-stu-id="65717-118">Requirement</span></span> | <span data-ttu-id="65717-119">值</span><span class="sxs-lookup"><span data-stu-id="65717-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="65717-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="65717-120">Minimum supported client</span></span><br/> | <span data-ttu-id="65717-121">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="65717-121">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="65717-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="65717-122">Minimum supported server</span></span><br/> | <span data-ttu-id="65717-123">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="65717-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="65717-124">標頭</span><span class="sxs-lookup"><span data-stu-id="65717-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="65717-125"><dt>D3d9types。h</dt></span><span class="sxs-lookup"><span data-stu-id="65717-125"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65717-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="65717-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65717-127">內容保護查詢</span><span class="sxs-lookup"><span data-stu-id="65717-127">Content Protection Queries</span></span>](content-protection-queries.md)
</dt> <dt>

[<span data-ttu-id="65717-128">以 GPU 為基礎的內容保護</span><span class="sxs-lookup"><span data-stu-id="65717-128">GPU-Based Content Protection</span></span>](gpu-based-content-protection.md)
</dt> <dt>

[<span data-ttu-id="65717-129">**IDirect3DAuthenticatedChannel9：： Query**</span><span class="sxs-lookup"><span data-stu-id="65717-129">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




