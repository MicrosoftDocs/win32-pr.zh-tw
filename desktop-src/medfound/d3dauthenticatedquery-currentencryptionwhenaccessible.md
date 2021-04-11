---
description: 傳回在 CPU 或匯流排可以存取內容之前套用的加密類型。
ms.assetid: 89526bb2-1316-4730-b599-3690b1838c3e
title: 'D3DAUTHENTICATEDQUERY_CURRENTENCRYPTIONWHENACCESSIBLE (D3d9types) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_CURRENTENCRYPTIONWHENACCESSIBLE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: a8b3374e6d50a50d32b60113318e5d1099083226
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191065"
---
# <a name="d3dauthenticatedquery_currentencryptionwhenaccessible"></a><span data-ttu-id="627d5-103">D3DAUTHENTICATEDQUERY \_ CURRENTENCRYPTIONWHENACCESSIBLE</span><span class="sxs-lookup"><span data-stu-id="627d5-103">D3DAUTHENTICATEDQUERY\_CURRENTENCRYPTIONWHENACCESSIBLE</span></span>

<span data-ttu-id="627d5-104">傳回在 CPU 或匯流排可以存取內容之前套用的加密類型。</span><span class="sxs-lookup"><span data-stu-id="627d5-104">Returns the encryption type that is applied before content becomes accessible to the CPU or bus.</span></span>



| <span data-ttu-id="627d5-105">需求</span><span class="sxs-lookup"><span data-stu-id="627d5-105">Requirement</span></span> | <span data-ttu-id="627d5-106">值</span><span class="sxs-lookup"><span data-stu-id="627d5-106">Value</span></span> |
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="627d5-107">查詢 GUID</span><span class="sxs-lookup"><span data-stu-id="627d5-107">Query GUID</span></span>  | <span data-ttu-id="627d5-108">**D3DAUTHENTICATEDQUERY \_ CURRENTENCRYPTIONWHENACCESSIBLE**</span><span class="sxs-lookup"><span data-stu-id="627d5-108">**D3DAUTHENTICATEDQUERY\_CURRENTENCRYPTIONWHENACCESSIBLE**</span></span>                                                                                   |
| <span data-ttu-id="627d5-109">輸入資料</span><span class="sxs-lookup"><span data-stu-id="627d5-109">Input data</span></span>  | [<span data-ttu-id="627d5-110">**D3DAUTHENTICATEDCHANNEL \_ 查詢 \_ 輸入**</span><span class="sxs-lookup"><span data-stu-id="627d5-110">**D3DAUTHENTICATEDCHANNEL\_QUERY\_INPUT**</span></span>](d3dauthenticatedchannel-query-input.md)                                                         |
| <span data-ttu-id="627d5-111">傳回資料</span><span class="sxs-lookup"><span data-stu-id="627d5-111">Return data</span></span> | [<span data-ttu-id="627d5-112">**D3DAUTHENTICATEDCHANNEL \_ QUERYUNCOMPRESSEDENCRYPTIONLEVEL \_ 輸出**</span><span class="sxs-lookup"><span data-stu-id="627d5-112">**D3DAUTHENTICATEDCHANNEL\_QUERYUNCOMPRESSEDENCRYPTIONLEVEL\_OUTPUT**</span></span>](d3dauthenticatedchannel-queryuncompressedencryptionlevel-output.md) |



 

## <a name="remarks"></a><span data-ttu-id="627d5-113">備註</span><span class="sxs-lookup"><span data-stu-id="627d5-113">Remarks</span></span>

<span data-ttu-id="627d5-114">下列通道類型支援此查詢：</span><span class="sxs-lookup"><span data-stu-id="627d5-114">The following channel types support this query:</span></span>

-   <span data-ttu-id="627d5-115">**D3DAUTHENTICATEDCHANNEL \_ 驅動程式 \_ 硬體**</span><span class="sxs-lookup"><span data-stu-id="627d5-115">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_HARDWARE**</span></span>
-   <span data-ttu-id="627d5-116">**D3DAUTHENTICATEDCHANNEL \_ 驅動程式 \_ 軟體**</span><span class="sxs-lookup"><span data-stu-id="627d5-116">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_SOFTWARE**</span></span>

## <a name="requirements"></a><span data-ttu-id="627d5-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="627d5-117">Requirements</span></span>



| <span data-ttu-id="627d5-118">需求</span><span class="sxs-lookup"><span data-stu-id="627d5-118">Requirement</span></span> | <span data-ttu-id="627d5-119">值</span><span class="sxs-lookup"><span data-stu-id="627d5-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="627d5-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="627d5-120">Minimum supported client</span></span><br/> | <span data-ttu-id="627d5-121">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="627d5-121">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="627d5-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="627d5-122">Minimum supported server</span></span><br/> | <span data-ttu-id="627d5-123">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="627d5-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="627d5-124">標頭</span><span class="sxs-lookup"><span data-stu-id="627d5-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="627d5-125"><dt>D3d9types。h</dt></span><span class="sxs-lookup"><span data-stu-id="627d5-125"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="627d5-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="627d5-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="627d5-127">內容保護查詢</span><span class="sxs-lookup"><span data-stu-id="627d5-127">Content Protection Queries</span></span>](content-protection-queries.md)
</dt> <dt>

[<span data-ttu-id="627d5-128">以 GPU 為基礎的內容保護</span><span class="sxs-lookup"><span data-stu-id="627d5-128">GPU-Based Content Protection</span></span>](gpu-based-content-protection.md)
</dt> <dt>

[<span data-ttu-id="627d5-129">**IDirect3DAuthenticatedChannel9：： Query**</span><span class="sxs-lookup"><span data-stu-id="627d5-129">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




