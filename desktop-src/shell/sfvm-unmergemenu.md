---
description: 通知回呼物件正在移除功能表。 由 IShellFolderViewCB：： MessageSFVCB 使用。
title: 'SFVM_UNMERGEMENU 訊息 (Shlobj.h .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 0255a41d-e8b4-48d2-931a-aa76ad83c18c
api_name:
- SFVM_UNMERGEMENU
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 6c83df7ca42d66f320339901a176dc9d4d38ff37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973780"
---
# <a name="sfvm_unmergemenu-message"></a><span data-ttu-id="0bf00-104">SFVM \_ UNMERGEMENU 訊息</span><span class="sxs-lookup"><span data-stu-id="0bf00-104">SFVM\_UNMERGEMENU message</span></span>

<span data-ttu-id="0bf00-105">通知回呼物件正在移除功能表。</span><span class="sxs-lookup"><span data-stu-id="0bf00-105">Notifies the callback object that a menu is being removed.</span></span> <span data-ttu-id="0bf00-106">由 [**IShellFolderViewCB：： MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)使用。</span><span class="sxs-lookup"><span data-stu-id="0bf00-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_UNMERGEMENU 

    lParam = (LPARAM)(HMENU) hmenuCurrent;

            
```



## <a name="parameters"></a><span data-ttu-id="0bf00-107">參數</span><span class="sxs-lookup"><span data-stu-id="0bf00-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0bf00-108">*hmenuCurrent* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0bf00-108">*hmenuCurrent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0bf00-109">正在移除之功能表的控制碼。</span><span class="sxs-lookup"><span data-stu-id="0bf00-109">The handle of the menu that is being removed.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0bf00-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="0bf00-110">Requirements</span></span>



| <span data-ttu-id="0bf00-111">需求</span><span class="sxs-lookup"><span data-stu-id="0bf00-111">Requirement</span></span> | <span data-ttu-id="0bf00-112">值</span><span class="sxs-lookup"><span data-stu-id="0bf00-112">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="0bf00-113">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0bf00-113">Minimum supported client</span></span><br/> | <span data-ttu-id="0bf00-114">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0bf00-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="0bf00-115">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0bf00-115">Minimum supported server</span></span><br/> | <span data-ttu-id="0bf00-116">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0bf00-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="0bf00-117">標頭</span><span class="sxs-lookup"><span data-stu-id="0bf00-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="0bf00-118"><dt>Shlobj.h。h</dt></span><span class="sxs-lookup"><span data-stu-id="0bf00-118"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
