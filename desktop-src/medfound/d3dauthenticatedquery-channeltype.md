---
description: 傳回已驗證通道的類型。
ms.assetid: eec4b117-a9f2-479d-99d7-e5d4053cf6b4
title: 'D3DAUTHENTICATEDQUERY_CHANNELTYPE (D3d9types) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_CHANNELTYPE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 58ac84a0caca5a5709c74adbca567633e12daa10
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106989903"
---
# <a name="d3dauthenticatedquery_channeltype"></a><span data-ttu-id="530b4-103">D3DAUTHENTICATEDQUERY \_ CHANNELTYPE</span><span class="sxs-lookup"><span data-stu-id="530b4-103">D3DAUTHENTICATEDQUERY\_CHANNELTYPE</span></span>

<span data-ttu-id="530b4-104">傳回已驗證通道的類型。</span><span class="sxs-lookup"><span data-stu-id="530b4-104">Returns the type of authenticated channel.</span></span>



| <span data-ttu-id="530b4-105">需求</span><span class="sxs-lookup"><span data-stu-id="530b4-105">Requirement</span></span> | <span data-ttu-id="530b4-106">值</span><span class="sxs-lookup"><span data-stu-id="530b4-106">Value</span></span> |
|-------------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="530b4-107">查詢 GUID</span><span class="sxs-lookup"><span data-stu-id="530b4-107">Query GUID</span></span>  | <span data-ttu-id="530b4-108">**D3DAUTHENTICATEDQUERY \_ CHANNELTYPE**</span><span class="sxs-lookup"><span data-stu-id="530b4-108">**D3DAUTHENTICATEDQUERY\_CHANNELTYPE**</span></span>                                                                       |
| <span data-ttu-id="530b4-109">輸入資料</span><span class="sxs-lookup"><span data-stu-id="530b4-109">Input data</span></span>  | [<span data-ttu-id="530b4-110">**D3DAUTHENTICATEDCHANNEL \_ 查詢 \_ 輸入**</span><span class="sxs-lookup"><span data-stu-id="530b4-110">**D3DAUTHENTICATEDCHANNEL\_QUERY\_INPUT**</span></span>](d3dauthenticatedchannel-query-input.md)                         |
| <span data-ttu-id="530b4-111">傳回資料</span><span class="sxs-lookup"><span data-stu-id="530b4-111">Return data</span></span> | [<span data-ttu-id="530b4-112">**D3DAUTHENTICATEDCHANNEL \_ QUERYCHANNELTYPE \_ 輸出**</span><span class="sxs-lookup"><span data-stu-id="530b4-112">**D3DAUTHENTICATEDCHANNEL\_QUERYCHANNELTYPE\_OUTPUT**</span></span>](d3dauthenticatedchannel-querychanneltype-output.md) |



 

## <a name="remarks"></a><span data-ttu-id="530b4-113">備註</span><span class="sxs-lookup"><span data-stu-id="530b4-113">Remarks</span></span>

<span data-ttu-id="530b4-114">此查詢對於所有通道類型都有效。</span><span class="sxs-lookup"><span data-stu-id="530b4-114">This query is valid for all channel types.</span></span>

## <a name="requirements"></a><span data-ttu-id="530b4-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="530b4-115">Requirements</span></span>



| <span data-ttu-id="530b4-116">需求</span><span class="sxs-lookup"><span data-stu-id="530b4-116">Requirement</span></span> | <span data-ttu-id="530b4-117">值</span><span class="sxs-lookup"><span data-stu-id="530b4-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="530b4-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="530b4-118">Minimum supported client</span></span><br/> | <span data-ttu-id="530b4-119">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="530b4-119">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="530b4-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="530b4-120">Minimum supported server</span></span><br/> | <span data-ttu-id="530b4-121">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="530b4-121">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="530b4-122">標頭</span><span class="sxs-lookup"><span data-stu-id="530b4-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="530b4-123"><dt>D3d9types。h</dt></span><span class="sxs-lookup"><span data-stu-id="530b4-123"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="530b4-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="530b4-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="530b4-125">內容保護查詢</span><span class="sxs-lookup"><span data-stu-id="530b4-125">Content Protection Queries</span></span>](content-protection-queries.md)
</dt> <dt>

[<span data-ttu-id="530b4-126">以 GPU 為基礎的內容保護</span><span class="sxs-lookup"><span data-stu-id="530b4-126">GPU-Based Content Protection</span></span>](gpu-based-content-protection.md)
</dt> <dt>

[<span data-ttu-id="530b4-127">**IDirect3DAuthenticatedChannel9：： Query**</span><span class="sxs-lookup"><span data-stu-id="530b4-127">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




