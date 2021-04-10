---
description: 傳回裝置目前的保護層級。
ms.assetid: 335d21e8-2a98-4824-a60d-1969a40e8d24
title: 'D3DAUTHENTICATEDQUERY_PROTECTION (D3d9types) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_PROTECTION
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 85147d764d5b6580305723e9b05b127b116a660e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191062"
---
# <a name="d3dauthenticatedquery_protection"></a><span data-ttu-id="bccab-103">D3DAUTHENTICATEDQUERY \_ 保護</span><span class="sxs-lookup"><span data-stu-id="bccab-103">D3DAUTHENTICATEDQUERY\_PROTECTION</span></span>

<span data-ttu-id="bccab-104">傳回裝置目前的保護層級。</span><span class="sxs-lookup"><span data-stu-id="bccab-104">Returns the current protection level for the device.</span></span>



| <span data-ttu-id="bccab-105">需求</span><span class="sxs-lookup"><span data-stu-id="bccab-105">Requirement</span></span> | <span data-ttu-id="bccab-106">值</span><span class="sxs-lookup"><span data-stu-id="bccab-106">Value</span></span> |
|-------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bccab-107">查詢 GUID</span><span class="sxs-lookup"><span data-stu-id="bccab-107">Query GUID</span></span>  | <span data-ttu-id="bccab-108">**D3DAUTHENTICATEDQUERY \_ 保護**</span><span class="sxs-lookup"><span data-stu-id="bccab-108">**D3DAUTHENTICATEDQUERY\_PROTECTION**</span></span>                                                                      |
| <span data-ttu-id="bccab-109">輸入資料</span><span class="sxs-lookup"><span data-stu-id="bccab-109">Input data</span></span>  | [<span data-ttu-id="bccab-110">**D3DAUTHENTICATEDCHANNEL \_ 查詢 \_ 輸入**</span><span class="sxs-lookup"><span data-stu-id="bccab-110">**D3DAUTHENTICATEDCHANNEL\_QUERY\_INPUT**</span></span>](d3dauthenticatedchannel-query-input.md)                       |
| <span data-ttu-id="bccab-111">傳回資料</span><span class="sxs-lookup"><span data-stu-id="bccab-111">Return data</span></span> | [<span data-ttu-id="bccab-112">**D3DAUTHENTICATEDCHANNEL \_ QUERYPROTECTION \_ 輸出**</span><span class="sxs-lookup"><span data-stu-id="bccab-112">**D3DAUTHENTICATEDCHANNEL\_QUERYPROTECTION\_OUTPUT**</span></span>](d3dauthenticatedchannel-queryprotection-output.md) |



 

## <a name="remarks"></a><span data-ttu-id="bccab-113">備註</span><span class="sxs-lookup"><span data-stu-id="bccab-113">Remarks</span></span>

<span data-ttu-id="bccab-114">此查詢對於所有通道類型都有效。</span><span class="sxs-lookup"><span data-stu-id="bccab-114">This query is valid for all channel types.</span></span>

## <a name="requirements"></a><span data-ttu-id="bccab-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="bccab-115">Requirements</span></span>



| <span data-ttu-id="bccab-116">需求</span><span class="sxs-lookup"><span data-stu-id="bccab-116">Requirement</span></span> | <span data-ttu-id="bccab-117">值</span><span class="sxs-lookup"><span data-stu-id="bccab-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bccab-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bccab-118">Minimum supported client</span></span><br/> | <span data-ttu-id="bccab-119">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bccab-119">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="bccab-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bccab-120">Minimum supported server</span></span><br/> | <span data-ttu-id="bccab-121">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bccab-121">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="bccab-122">標頭</span><span class="sxs-lookup"><span data-stu-id="bccab-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="bccab-123"><dt>D3d9types。h</dt></span><span class="sxs-lookup"><span data-stu-id="bccab-123"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bccab-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bccab-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bccab-125">內容保護查詢</span><span class="sxs-lookup"><span data-stu-id="bccab-125">Content Protection Queries</span></span>](content-protection-queries.md)
</dt> <dt>

[<span data-ttu-id="bccab-126">以 GPU 為基礎的內容保護</span><span class="sxs-lookup"><span data-stu-id="bccab-126">GPU-Based Content Protection</span></span>](gpu-based-content-protection.md)
</dt> <dt>

[<span data-ttu-id="bccab-127">**IDirect3DAuthenticatedChannel9：： Query**</span><span class="sxs-lookup"><span data-stu-id="bccab-127">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




