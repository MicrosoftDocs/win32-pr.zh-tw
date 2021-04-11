---
description: 讓進程開啟共用資源，或停用開啟共用資源的進程。
ms.assetid: 5fa2b88f-e946-436c-953e-04e0e338146c
title: 'D3DAUTHENTICATEDCONFIGURE_SHAREDRESOURCE (D3d9types) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCONFIGURE_SHAREDRESOURCE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 7404a4bed3ac3b1d4002bb03c45d7732500b77e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191066"
---
# <a name="d3dauthenticatedconfigure_sharedresource"></a><span data-ttu-id="3ba49-103">D3DAUTHENTICATEDCONFIGURE \_ SHAREDRESOURCE</span><span class="sxs-lookup"><span data-stu-id="3ba49-103">D3DAUTHENTICATEDCONFIGURE\_SHAREDRESOURCE</span></span>

<span data-ttu-id="3ba49-104">讓進程開啟共用資源，或停用開啟共用資源的進程。</span><span class="sxs-lookup"><span data-stu-id="3ba49-104">Enables a process to open a shared resource, or disables a process from opening shared resources.</span></span>



| <span data-ttu-id="3ba49-105">需求</span><span class="sxs-lookup"><span data-stu-id="3ba49-105">Requirement</span></span> | <span data-ttu-id="3ba49-106">值</span><span class="sxs-lookup"><span data-stu-id="3ba49-106">Value</span></span> |
|--------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ba49-107">命令 GUID</span><span class="sxs-lookup"><span data-stu-id="3ba49-107">Command GUID</span></span> | <span data-ttu-id="3ba49-108">**D3DAUTHENTICATEDCONFIGURE \_ SHAREDRESOURCE**</span><span class="sxs-lookup"><span data-stu-id="3ba49-108">**D3DAUTHENTICATEDCONFIGURE\_SHAREDRESOURCE**</span></span>                                                               |
| <span data-ttu-id="3ba49-109">輸入資料</span><span class="sxs-lookup"><span data-stu-id="3ba49-109">Input data</span></span>   | [<span data-ttu-id="3ba49-110">**D3DAUTHENTICATEDCHANNEL \_ CONFIGURESHAREDRESOURCE**</span><span class="sxs-lookup"><span data-stu-id="3ba49-110">**D3DAUTHENTICATEDCHANNEL\_CONFIGURESHAREDRESOURCE**</span></span>](d3dauthenticatedchannel-configuresharedresource.md) |



 

## <a name="remarks"></a><span data-ttu-id="3ba49-111">備註</span><span class="sxs-lookup"><span data-stu-id="3ba49-111">Remarks</span></span>

<span data-ttu-id="3ba49-112">下列通道類型支援此查詢：</span><span class="sxs-lookup"><span data-stu-id="3ba49-112">The following channel types support this query:</span></span>

-   <span data-ttu-id="3ba49-113">**D3DAUTHENTICATEDCHANNEL \_ 驅動程式 \_ D3D9**</span><span class="sxs-lookup"><span data-stu-id="3ba49-113">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_D3D9**</span></span>
-   <span data-ttu-id="3ba49-114">**D3DAUTHENTICATEDCHANNEL \_ 驅動程式 \_ 軟體**</span><span class="sxs-lookup"><span data-stu-id="3ba49-114">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_SOFTWARE**</span></span>

## <a name="requirements"></a><span data-ttu-id="3ba49-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="3ba49-115">Requirements</span></span>



| <span data-ttu-id="3ba49-116">需求</span><span class="sxs-lookup"><span data-stu-id="3ba49-116">Requirement</span></span> | <span data-ttu-id="3ba49-117">值</span><span class="sxs-lookup"><span data-stu-id="3ba49-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3ba49-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3ba49-118">Minimum supported client</span></span><br/> | <span data-ttu-id="3ba49-119">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3ba49-119">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="3ba49-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3ba49-120">Minimum supported server</span></span><br/> | <span data-ttu-id="3ba49-121">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3ba49-121">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="3ba49-122">標頭</span><span class="sxs-lookup"><span data-stu-id="3ba49-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="3ba49-123"><dt>D3d9types。h</dt></span><span class="sxs-lookup"><span data-stu-id="3ba49-123"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3ba49-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3ba49-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ba49-125">內容保護命令</span><span class="sxs-lookup"><span data-stu-id="3ba49-125">Content Protection Commands</span></span>](content-protection-commands.md)
</dt> <dt>

[<span data-ttu-id="3ba49-126">以 GPU 為基礎的內容保護</span><span class="sxs-lookup"><span data-stu-id="3ba49-126">GPU-Based Content Protection</span></span>](gpu-based-content-protection.md)
</dt> <dt>

[<span data-ttu-id="3ba49-127">**IDirect3DAuthenticatedChannel9：： Configure**</span><span class="sxs-lookup"><span data-stu-id="3ba49-127">**IDirect3DAuthenticatedChannel9::Configure**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)
</dt> </dl>

 

 




