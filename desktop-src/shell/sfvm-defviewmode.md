---
description: 允許回呼物件指定 view 模式。 由 IShellFolderViewCB：： MessageSFVCB 使用。
title: 'SFVM_DEFVIEWMODE 訊息 (Shlobj.h .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 5118fc81-490f-4d76-9361-0d6af0c4b4c0
api_name:
- SFVM_DEFVIEWMODE
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 8d57bb61b2b938947d0290345215e3735d9d8763
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104991778"
---
# <a name="sfvm_defviewmode-message"></a><span data-ttu-id="56a3b-104">SFVM \_ DEFVIEWMODE 訊息</span><span class="sxs-lookup"><span data-stu-id="56a3b-104">SFVM\_DEFVIEWMODE message</span></span>

<span data-ttu-id="56a3b-105">允許回呼物件指定 view 模式。</span><span class="sxs-lookup"><span data-stu-id="56a3b-105">Allows the callback object to specify the view mode.</span></span> <span data-ttu-id="56a3b-106">由 [**IShellFolderViewCB：： MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)使用。</span><span class="sxs-lookup"><span data-stu-id="56a3b-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_DEFVIEWMODE 

    lParam = (LPARAM)(FOLDERVIEWMODE*) pViewMode;

            
```



## <a name="parameters"></a><span data-ttu-id="56a3b-107">參數</span><span class="sxs-lookup"><span data-stu-id="56a3b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56a3b-108">*pViewMode* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="56a3b-108">*pViewMode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="56a3b-109">[**FOLDERVIEWMODE**](/windows/desktop/api/shobjidl_core/ne-shobjidl_core-folderviewmode)列舉型別中的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="56a3b-109">One of the values from the [**FOLDERVIEWMODE**](/windows/desktop/api/shobjidl_core/ne-shobjidl_core-folderviewmode) enumerated type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="56a3b-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="56a3b-110">Requirements</span></span>



| <span data-ttu-id="56a3b-111">需求</span><span class="sxs-lookup"><span data-stu-id="56a3b-111">Requirement</span></span> | <span data-ttu-id="56a3b-112">值</span><span class="sxs-lookup"><span data-stu-id="56a3b-112">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="56a3b-113">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="56a3b-113">Minimum supported client</span></span><br/> | <span data-ttu-id="56a3b-114">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="56a3b-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="56a3b-115">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="56a3b-115">Minimum supported server</span></span><br/> | <span data-ttu-id="56a3b-116">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="56a3b-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="56a3b-117">標頭</span><span class="sxs-lookup"><span data-stu-id="56a3b-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="56a3b-118"><dt>Shlobj.h。h</dt></span><span class="sxs-lookup"><span data-stu-id="56a3b-118"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
