---
description: 設定在受保護的內容變成可供 CPU 或匯流排存取之前，所執行的加密層級。
ms.assetid: 6de6c4a3-705a-4420-b9f4-8d4d442b23bf
title: 'D3DAUTHENTICATEDCONFIGURE_ENCRYPTIONWHENACCESSIBLE (D3d9types) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCONFIGURE_ENCRYPTIONWHENACCESSIBLE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 8b624c26c81549372e0e09b4a08ce73f6cd3dd27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510809"
---
# <a name="d3dauthenticatedconfigure_encryptionwhenaccessible"></a><span data-ttu-id="c0326-103">D3DAUTHENTICATEDCONFIGURE \_ ENCRYPTIONWHENACCESSIBLE</span><span class="sxs-lookup"><span data-stu-id="c0326-103">D3DAUTHENTICATEDCONFIGURE\_ENCRYPTIONWHENACCESSIBLE</span></span>

<span data-ttu-id="c0326-104">設定在受保護的內容變成可供 CPU 或匯流排存取之前，所執行的加密層級。</span><span class="sxs-lookup"><span data-stu-id="c0326-104">Sets the level of encryption that is performed before protected content becomes accessible to the CPU or bus.</span></span>



| <span data-ttu-id="c0326-105">需求</span><span class="sxs-lookup"><span data-stu-id="c0326-105">Requirement</span></span> | <span data-ttu-id="c0326-106">值</span><span class="sxs-lookup"><span data-stu-id="c0326-106">Value</span></span> |
|--------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0326-107">命令 GUID</span><span class="sxs-lookup"><span data-stu-id="c0326-107">Command GUID</span></span> | <span data-ttu-id="c0326-108">**D3DAUTHENTICATEDCONFIGURE \_ ENCRYPTIONWHENACCESSIBLE**</span><span class="sxs-lookup"><span data-stu-id="c0326-108">**D3DAUTHENTICATEDCONFIGURE\_ENCRYPTIONWHENACCESSIBLE**</span></span>                                                                     |
| <span data-ttu-id="c0326-109">輸入資料</span><span class="sxs-lookup"><span data-stu-id="c0326-109">Input data</span></span>   | [<span data-ttu-id="c0326-110">**D3DAUTHENTICATEDCHANNEL \_ CONFIGUREUNCOMPRESSEDENCRYPTION**</span><span class="sxs-lookup"><span data-stu-id="c0326-110">**D3DAUTHENTICATEDCHANNEL\_CONFIGUREUNCOMPRESSEDENCRYPTION**</span></span>](d3dauthenticatedchannel-configureuncompressedencryption.md) |



 

## <a name="remarks"></a><span data-ttu-id="c0326-111">備註</span><span class="sxs-lookup"><span data-stu-id="c0326-111">Remarks</span></span>

<span data-ttu-id="c0326-112">下列通道類型支援此查詢：</span><span class="sxs-lookup"><span data-stu-id="c0326-112">The following channel types support this query:</span></span>

-   <span data-ttu-id="c0326-113">**D3DAUTHENTICATEDCHANNEL \_ 驅動程式 \_ 硬體**</span><span class="sxs-lookup"><span data-stu-id="c0326-113">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_HARDWARE**</span></span>
-   <span data-ttu-id="c0326-114">**D3DAUTHENTICATEDCHANNEL \_ 驅動程式 \_ 軟體**</span><span class="sxs-lookup"><span data-stu-id="c0326-114">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_SOFTWARE**</span></span>

## <a name="requirements"></a><span data-ttu-id="c0326-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="c0326-115">Requirements</span></span>



| <span data-ttu-id="c0326-116">需求</span><span class="sxs-lookup"><span data-stu-id="c0326-116">Requirement</span></span> | <span data-ttu-id="c0326-117">值</span><span class="sxs-lookup"><span data-stu-id="c0326-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c0326-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c0326-118">Minimum supported client</span></span><br/> | <span data-ttu-id="c0326-119">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c0326-119">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="c0326-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c0326-120">Minimum supported server</span></span><br/> | <span data-ttu-id="c0326-121">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c0326-121">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="c0326-122">標頭</span><span class="sxs-lookup"><span data-stu-id="c0326-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="c0326-123"><dt>D3d9types。h</dt></span><span class="sxs-lookup"><span data-stu-id="c0326-123"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0326-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c0326-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0326-125">內容保護命令</span><span class="sxs-lookup"><span data-stu-id="c0326-125">Content Protection Commands</span></span>](content-protection-commands.md)
</dt> <dt>

[<span data-ttu-id="c0326-126">以 GPU 為基礎的內容保護</span><span class="sxs-lookup"><span data-stu-id="c0326-126">GPU-Based Content Protection</span></span>](gpu-based-content-protection.md)
</dt> <dt>

[<span data-ttu-id="c0326-127">**IDirect3DAuthenticatedChannel9：： Configure**</span><span class="sxs-lookup"><span data-stu-id="c0326-127">**IDirect3DAuthenticatedChannel9::Configure**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)
</dt> </dl>

 

 




