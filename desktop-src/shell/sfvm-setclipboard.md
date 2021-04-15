---
description: 當其中一個物件放在剪貼簿上作為功能表命令的結果時，就會通知 IShellView。 由 SHShellFolderView \_ 訊息使用。
title: 'SFVM_SETCLIPBOARD 訊息 (Shlobj.h .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 6a4cf0c5-2349-4e1e-b6c5-ee9b5430456e
api_name:
- SFVM_SETCLIPBOARD
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: c9c30848de77ef7de101eaa9d724f2f26f9d384c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104991802"
---
# <a name="sfvm_setclipboard-message"></a><span data-ttu-id="4ab82-104">SFVM \_ SETCLIPBOARD 訊息</span><span class="sxs-lookup"><span data-stu-id="4ab82-104">SFVM\_SETCLIPBOARD message</span></span>

<span data-ttu-id="4ab82-105">當其中一個物件放在剪貼簿上作為功能表命令的結果時，就會通知 [**IShellView**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview) 。</span><span class="sxs-lookup"><span data-stu-id="4ab82-105">Notifies the [**IShellView**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview) when one of its objects is placed on the Clipboard as a result of a menu command.</span></span> <span data-ttu-id="4ab82-106">由 [**SHShellFolderView \_ 訊息**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message)使用。</span><span class="sxs-lookup"><span data-stu-id="4ab82-106">Used by [**SHShellFolderView\_Message**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).</span></span>


```C++
SFVM_SETCLIPBOARD 

    lParam = (DWORD) dwEffect;

            
```



## <a name="parameters"></a><span data-ttu-id="4ab82-107">參數</span><span class="sxs-lookup"><span data-stu-id="4ab82-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ab82-108">*dwEffect* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4ab82-108">*dwEffect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ab82-109">如果專案正在剪下到剪貼簿，請使用 (WPARAM) -2，如果正在將專案複製到剪貼簿，則為 (WPARAM) -3。</span><span class="sxs-lookup"><span data-stu-id="4ab82-109">Use (WPARAM)-2 if the item is being cut to the Clipboard or (WPARAM)-3 if the item is being copied to the Clipboard.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4ab82-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="4ab82-110">Return value</span></span>

<span data-ttu-id="4ab82-111">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="4ab82-111">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4ab82-112">備註</span><span class="sxs-lookup"><span data-stu-id="4ab82-112">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="4ab82-113">需求</span><span class="sxs-lookup"><span data-stu-id="4ab82-113">Requirements</span></span>



| <span data-ttu-id="4ab82-114">需求</span><span class="sxs-lookup"><span data-stu-id="4ab82-114">Requirement</span></span> | <span data-ttu-id="4ab82-115">值</span><span class="sxs-lookup"><span data-stu-id="4ab82-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="4ab82-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4ab82-116">Minimum supported client</span></span><br/> | <span data-ttu-id="4ab82-117">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4ab82-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="4ab82-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4ab82-118">Minimum supported server</span></span><br/> | <span data-ttu-id="4ab82-119">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4ab82-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="4ab82-120">標頭</span><span class="sxs-lookup"><span data-stu-id="4ab82-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="4ab82-121"><dt>Shlobj.h。h</dt></span><span class="sxs-lookup"><span data-stu-id="4ab82-121"><dt>Shlobj.h</dt></span></span> </dl> |



 

 




