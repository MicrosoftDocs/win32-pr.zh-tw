---
description: 允許回呼物件指定資料夾檢視中的專案數。 由 IShellFolderViewCB：： MessageSFVCB 使用。
title: 'SFVM_DEFITEMCOUNT 訊息 (Shlobj.h .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 62306eaa-e52e-432b-9233-d990519d5739
api_name:
- SFVM_DEFITEMCOUNT
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 4e3f746e422428ab9f925cf4ff3f460ccd578367
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944491"
---
# <a name="sfvm_defitemcount-message"></a><span data-ttu-id="88757-104">SFVM \_ DEFITEMCOUNT 訊息</span><span class="sxs-lookup"><span data-stu-id="88757-104">SFVM\_DEFITEMCOUNT message</span></span>

<span data-ttu-id="88757-105">允許回呼物件指定資料夾檢視中的專案數。</span><span class="sxs-lookup"><span data-stu-id="88757-105">Allows the callback object to specify the number of items in the folder view.</span></span> <span data-ttu-id="88757-106">由 [**IShellFolderViewCB：： MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)使用。</span><span class="sxs-lookup"><span data-stu-id="88757-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_DEFITEMCOUNT 

    lParam = (LPARAM)(UINT*) cItems;

            
```



## <a name="parameters"></a><span data-ttu-id="88757-107">參數</span><span class="sxs-lookup"><span data-stu-id="88757-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88757-108">*cItems* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="88757-108">*cItems* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="88757-109">資料夾檢視中的專案數。</span><span class="sxs-lookup"><span data-stu-id="88757-109">The number of items in the folder view.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="88757-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="88757-110">Requirements</span></span>



| <span data-ttu-id="88757-111">需求</span><span class="sxs-lookup"><span data-stu-id="88757-111">Requirement</span></span> | <span data-ttu-id="88757-112">值</span><span class="sxs-lookup"><span data-stu-id="88757-112">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="88757-113">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="88757-113">Minimum supported client</span></span><br/> | <span data-ttu-id="88757-114">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="88757-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="88757-115">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="88757-115">Minimum supported server</span></span><br/> | <span data-ttu-id="88757-116">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="88757-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="88757-117">標頭</span><span class="sxs-lookup"><span data-stu-id="88757-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="88757-118"><dt>Shlobj.h。h</dt></span><span class="sxs-lookup"><span data-stu-id="88757-118"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
