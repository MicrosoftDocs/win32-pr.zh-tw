---
description: 通知回呼物件，使用者已叫用其中一個工具列或功能表命令。 由 IShellFolderViewCB：： MessageSFVCB 使用。
ms.assetid: 6b9e4a4d-ec45-489c-bbff-d123d5756b75
title: 'SFVM_INVOKECOMMAND 訊息 (Shlobj.h .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e5fc9709827250e5cf8060400bbecb714ae5998
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852579"
---
# <a name="sfvm_invokecommand-message"></a><span data-ttu-id="3ca45-104">SFVM \_ INVOKECOMMAND 訊息</span><span class="sxs-lookup"><span data-stu-id="3ca45-104">SFVM\_INVOKECOMMAND message</span></span>

<span data-ttu-id="3ca45-105">通知回呼物件，使用者已叫用其中一個工具列或功能表命令。</span><span class="sxs-lookup"><span data-stu-id="3ca45-105">Notifies the callback object that one of its toolbar or menu commands has been invoked by the user.</span></span> <span data-ttu-id="3ca45-106">由 [**IShellFolderViewCB：： MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)使用。</span><span class="sxs-lookup"><span data-stu-id="3ca45-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_INVOKECOMMAND 

    wParam = (WPARAM)(UINT) idCmd;

            
```



## <a name="parameters"></a><span data-ttu-id="3ca45-107">參數</span><span class="sxs-lookup"><span data-stu-id="3ca45-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ca45-108">*idCmd* \[\]</span><span class="sxs-lookup"><span data-stu-id="3ca45-108">*idCmd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ca45-109">選定工具列或功能表項目的命令識別碼。</span><span class="sxs-lookup"><span data-stu-id="3ca45-109">The command ID of the selected toolbar or menu item.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3ca45-110">備註</span><span class="sxs-lookup"><span data-stu-id="3ca45-110">Remarks</span></span>

<span data-ttu-id="3ca45-111">此訊息基本上與傳統視窗程式中的 [**WM \_ 命令**](../menurc/wm-command.md) 訊息具有相同的功能。</span><span class="sxs-lookup"><span data-stu-id="3ca45-111">This message serves essentially the same function as a [**WM\_COMMAND**](../menurc/wm-command.md) message in a conventional window procedure.</span></span> <span data-ttu-id="3ca45-112">它可讓回呼物件處理已加入 Windows 檔案總管工具或功能表列中的任何專案。</span><span class="sxs-lookup"><span data-stu-id="3ca45-112">It allows the callback object to handle any items that it has added to the Windows Explorer tool or menu bar.</span></span>

## <a name="requirements"></a><span data-ttu-id="3ca45-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="3ca45-113">Requirements</span></span>



| <span data-ttu-id="3ca45-114">需求</span><span class="sxs-lookup"><span data-stu-id="3ca45-114">Requirement</span></span> | <span data-ttu-id="3ca45-115">值</span><span class="sxs-lookup"><span data-stu-id="3ca45-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="3ca45-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3ca45-116">Minimum supported client</span></span><br/> | <span data-ttu-id="3ca45-117">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3ca45-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="3ca45-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3ca45-118">Minimum supported server</span></span><br/> | <span data-ttu-id="3ca45-119">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3ca45-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="3ca45-120">標頭</span><span class="sxs-lookup"><span data-stu-id="3ca45-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="3ca45-121"><dt>Shlobj.h。h</dt></span><span class="sxs-lookup"><span data-stu-id="3ca45-121"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
