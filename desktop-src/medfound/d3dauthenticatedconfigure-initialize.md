---
description: 初始化已驗證的通道。
ms.assetid: a74edbaa-af57-4f8e-9974-f6053f59377f
title: 'D3DAUTHENTICATEDCONFIGURE_INITIALIZE (D3d9types) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCONFIGURE_INITIALIZE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 2cd3238b7a7eea27356ce76ec9c83bf8aea4d7f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971153"
---
# <a name="d3dauthenticatedconfigure_initialize"></a><span data-ttu-id="1f923-103">D3DAUTHENTICATEDCONFIGURE \_ INITIALIZE</span><span class="sxs-lookup"><span data-stu-id="1f923-103">D3DAUTHENTICATEDCONFIGURE\_INITIALIZE</span></span>

<span data-ttu-id="1f923-104">初始化已驗證的通道。</span><span class="sxs-lookup"><span data-stu-id="1f923-104">Initializes the authenticated channel.</span></span>



| <span data-ttu-id="1f923-105">需求</span><span class="sxs-lookup"><span data-stu-id="1f923-105">Requirement</span></span> | <span data-ttu-id="1f923-106">值</span><span class="sxs-lookup"><span data-stu-id="1f923-106">Value</span></span> |
|--------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f923-107">命令 GUID</span><span class="sxs-lookup"><span data-stu-id="1f923-107">Command GUID</span></span> | <span data-ttu-id="1f923-108">**D3DAUTHENTICATEDCONFIGURE \_ INITIALIZE**</span><span class="sxs-lookup"><span data-stu-id="1f923-108">**D3DAUTHENTICATEDCONFIGURE\_INITIALIZE**</span></span>                                                           |
| <span data-ttu-id="1f923-109">輸入資料</span><span class="sxs-lookup"><span data-stu-id="1f923-109">Input data</span></span>   | [<span data-ttu-id="1f923-110">**D3DAUTHENTICATEDCHANNEL \_ CONFIGUREINITIALIZE**</span><span class="sxs-lookup"><span data-stu-id="1f923-110">**D3DAUTHENTICATEDCHANNEL\_CONFIGUREINITIALIZE**</span></span>](d3dauthenticatedchannel-configureinitialize.md) |



 

## <a name="remarks"></a><span data-ttu-id="1f923-111">備註</span><span class="sxs-lookup"><span data-stu-id="1f923-111">Remarks</span></span>

<span data-ttu-id="1f923-112">在會話開始時傳送此命令一次。</span><span class="sxs-lookup"><span data-stu-id="1f923-112">Send this command once, at the start of the session.</span></span> <span data-ttu-id="1f923-113">每個已驗證的通道只能傳送一次此命令。</span><span class="sxs-lookup"><span data-stu-id="1f923-113">This command can be sent only one time for each authenticated channel.</span></span> <span data-ttu-id="1f923-114">此命令會忽略輸入的序號。</span><span class="sxs-lookup"><span data-stu-id="1f923-114">The input sequence number is ignored for this command.</span></span>

<span data-ttu-id="1f923-115">下列通道類型支援此命令：</span><span class="sxs-lookup"><span data-stu-id="1f923-115">The following channel types support this command:</span></span>

-   <span data-ttu-id="1f923-116">**D3DAUTHENTICATEDCHANNEL \_ 驅動程式 \_ 硬體**</span><span class="sxs-lookup"><span data-stu-id="1f923-116">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_HARDWARE**</span></span>
-   <span data-ttu-id="1f923-117">**D3DAUTHENTICATEDCHANNEL \_ 驅動程式 \_ 軟體**</span><span class="sxs-lookup"><span data-stu-id="1f923-117">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_SOFTWARE**</span></span>

## <a name="requirements"></a><span data-ttu-id="1f923-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="1f923-118">Requirements</span></span>



| <span data-ttu-id="1f923-119">需求</span><span class="sxs-lookup"><span data-stu-id="1f923-119">Requirement</span></span> | <span data-ttu-id="1f923-120">值</span><span class="sxs-lookup"><span data-stu-id="1f923-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1f923-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1f923-121">Minimum supported client</span></span><br/> | <span data-ttu-id="1f923-122">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1f923-122">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="1f923-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1f923-123">Minimum supported server</span></span><br/> | <span data-ttu-id="1f923-124">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1f923-124">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="1f923-125">標頭</span><span class="sxs-lookup"><span data-stu-id="1f923-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="1f923-126"><dt>D3d9types。h</dt></span><span class="sxs-lookup"><span data-stu-id="1f923-126"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f923-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1f923-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f923-128">內容保護命令</span><span class="sxs-lookup"><span data-stu-id="1f923-128">Content Protection Commands</span></span>](content-protection-commands.md)
</dt> <dt>

[<span data-ttu-id="1f923-129">以 GPU 為基礎的內容保護</span><span class="sxs-lookup"><span data-stu-id="1f923-129">GPU-Based Content Protection</span></span>](gpu-based-content-protection.md)
</dt> <dt>

[<span data-ttu-id="1f923-130">**IDirect3DAuthenticatedChannel9：： Configure**</span><span class="sxs-lookup"><span data-stu-id="1f923-130">**IDirect3DAuthenticatedChannel9::Configure**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)
</dt> </dl>

 

 




