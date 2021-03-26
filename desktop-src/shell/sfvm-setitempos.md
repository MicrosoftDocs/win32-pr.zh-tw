---
description: 設定專案在 Shell 視圖中的位置。 由 SHShellFolderView \_ 訊息使用。
title: 'SFVM_SETITEMPOS 訊息 (Shlobj.h .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: b89f2d62-095b-4cad-a47e-2d41e122cb3e
api_name:
- SFVM_SETITEMPOS
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 450aeabee6e5edeba466e4a5fe64725c13eea32b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195126"
---
# <a name="sfvm_setitempos-message"></a><span data-ttu-id="31c81-104">SFVM \_ SETITEMPOS 訊息</span><span class="sxs-lookup"><span data-stu-id="31c81-104">SFVM\_SETITEMPOS message</span></span>

<span data-ttu-id="31c81-105">設定專案在 Shell 視圖中的位置。</span><span class="sxs-lookup"><span data-stu-id="31c81-105">Sets the position of an item in the Shell view.</span></span> <span data-ttu-id="31c81-106">由 [**SHShellFolderView \_ 訊息**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message)使用。</span><span class="sxs-lookup"><span data-stu-id="31c81-106">Used by [**SHShellFolderView\_Message**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).</span></span>


```C++

                SFVM_SETITEMPOS 

    lParam = (LPSFV_SETITEMPOS)&sip;

            
```



## <a name="parameters"></a><span data-ttu-id="31c81-107">參數</span><span class="sxs-lookup"><span data-stu-id="31c81-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31c81-108">*sip* \[在\]</span><span class="sxs-lookup"><span data-stu-id="31c81-108">*sip* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31c81-109">[**SFV \_ SETITEMPOS**](/windows/desktop/api/Shlobj/ns-shlobj-sfv_setitempos)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="31c81-109">A pointer to an [**SFV\_SETITEMPOS**](/windows/desktop/api/Shlobj/ns-shlobj-sfv_setitempos) structure.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="31c81-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="31c81-110">Requirements</span></span>



| <span data-ttu-id="31c81-111">需求</span><span class="sxs-lookup"><span data-stu-id="31c81-111">Requirement</span></span> | <span data-ttu-id="31c81-112">值</span><span class="sxs-lookup"><span data-stu-id="31c81-112">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="31c81-113">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="31c81-113">Minimum supported client</span></span><br/> | <span data-ttu-id="31c81-114">僅限 Windows XP （含 SP1） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="31c81-114">Windows XP with SP1 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="31c81-115">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="31c81-115">Minimum supported server</span></span><br/> | <span data-ttu-id="31c81-116">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="31c81-116">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="31c81-117">標頭</span><span class="sxs-lookup"><span data-stu-id="31c81-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="31c81-118"><dt>Shlobj.h。h</dt></span><span class="sxs-lookup"><span data-stu-id="31c81-118"><dt>Shlobj.h</dt></span></span> </dl> |



 

 




