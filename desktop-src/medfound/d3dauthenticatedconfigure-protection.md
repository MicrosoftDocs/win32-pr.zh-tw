---
description: 啟用或停用裝置的保護。
ms.assetid: 120d940f-39a0-4ad5-bd3e-c108b3f98ace
title: 'D3DAUTHENTICATEDCONFIGURE_PROTECTION (D3d9types) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCONFIGURE_PROTECTION
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 0e9ff9d3be9003bb274c82827e386848d3b755e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510808"
---
# <a name="d3dauthenticatedconfigure_protection"></a><span data-ttu-id="6e3c2-103">D3DAUTHENTICATEDCONFIGURE \_ 保護</span><span class="sxs-lookup"><span data-stu-id="6e3c2-103">D3DAUTHENTICATEDCONFIGURE\_PROTECTION</span></span>

<span data-ttu-id="6e3c2-104">啟用或停用裝置的保護。</span><span class="sxs-lookup"><span data-stu-id="6e3c2-104">Enables or disables protection for the device.</span></span>



| <span data-ttu-id="6e3c2-105">需求</span><span class="sxs-lookup"><span data-stu-id="6e3c2-105">Requirement</span></span> | <span data-ttu-id="6e3c2-106">值</span><span class="sxs-lookup"><span data-stu-id="6e3c2-106">Value</span></span> |
|--------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e3c2-107">命令 GUID</span><span class="sxs-lookup"><span data-stu-id="6e3c2-107">Command GUID</span></span> | <span data-ttu-id="6e3c2-108">**D3DAUTHENTICATEDCONFIGURE \_ 保護**</span><span class="sxs-lookup"><span data-stu-id="6e3c2-108">**D3DAUTHENTICATEDCONFIGURE\_PROTECTION**</span></span>                                                           |
| <span data-ttu-id="6e3c2-109">輸入資料</span><span class="sxs-lookup"><span data-stu-id="6e3c2-109">Input data</span></span>   | [<span data-ttu-id="6e3c2-110">**D3DAUTHENTICATEDCHANNEL \_ CONFIGUREPROTECTION**</span><span class="sxs-lookup"><span data-stu-id="6e3c2-110">**D3DAUTHENTICATEDCHANNEL\_CONFIGUREPROTECTION**</span></span>](d3dauthenticatedchannel-configureprotection.md) |



 

## <a name="remarks"></a><span data-ttu-id="6e3c2-111">備註</span><span class="sxs-lookup"><span data-stu-id="6e3c2-111">Remarks</span></span>

<span data-ttu-id="6e3c2-112">此命令對所有通道類型都有效。</span><span class="sxs-lookup"><span data-stu-id="6e3c2-112">This command is valid for all channel types.</span></span>

## <a name="requirements"></a><span data-ttu-id="6e3c2-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="6e3c2-113">Requirements</span></span>



| <span data-ttu-id="6e3c2-114">需求</span><span class="sxs-lookup"><span data-stu-id="6e3c2-114">Requirement</span></span> | <span data-ttu-id="6e3c2-115">值</span><span class="sxs-lookup"><span data-stu-id="6e3c2-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6e3c2-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6e3c2-116">Minimum supported client</span></span><br/> | <span data-ttu-id="6e3c2-117">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6e3c2-117">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="6e3c2-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6e3c2-118">Minimum supported server</span></span><br/> | <span data-ttu-id="6e3c2-119">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6e3c2-119">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="6e3c2-120">標頭</span><span class="sxs-lookup"><span data-stu-id="6e3c2-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="6e3c2-121"><dt>D3d9types。h</dt></span><span class="sxs-lookup"><span data-stu-id="6e3c2-121"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6e3c2-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6e3c2-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e3c2-123">內容保護命令</span><span class="sxs-lookup"><span data-stu-id="6e3c2-123">Content Protection Commands</span></span>](content-protection-commands.md)
</dt> <dt>

[<span data-ttu-id="6e3c2-124">以 GPU 為基礎的內容保護</span><span class="sxs-lookup"><span data-stu-id="6e3c2-124">GPU-Based Content Protection</span></span>](gpu-based-content-protection.md)
</dt> <dt>

[<span data-ttu-id="6e3c2-125">**IDirect3DAuthenticatedChannel9：： Configure**</span><span class="sxs-lookup"><span data-stu-id="6e3c2-125">**IDirect3DAuthenticatedChannel9::Configure**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)
</dt> </dl>

 

 




