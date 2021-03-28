---
description: 將物件加入至 Shell 視圖。 由 SHShellFolderView \_ 訊息使用。
title: 'SFVM_ADDOBJECT 訊息 (Shlobj.h .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 90394af6-3809-457c-b2f2-5f35187ed45b
api_name:
- SFVM_ADDOBJECT
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 0e5b3f0a5b1aed634ab8929b0501d2e23ba40352
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104991667"
---
# <a name="sfvm_addobject-message"></a><span data-ttu-id="6c3da-104">SFVM \_ ADDOBJECT 訊息</span><span class="sxs-lookup"><span data-stu-id="6c3da-104">SFVM\_ADDOBJECT message</span></span>

<span data-ttu-id="6c3da-105">將物件加入至 Shell 視圖。</span><span class="sxs-lookup"><span data-stu-id="6c3da-105">Adds an object to the Shell view.</span></span> <span data-ttu-id="6c3da-106">由 [**SHShellFolderView \_ 訊息**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message)使用。</span><span class="sxs-lookup"><span data-stu-id="6c3da-106">Used by [**SHShellFolderView\_Message**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).</span></span>


```C++
SFVM_ADDOBJECT 

    lParam = (LPARAM) pidl;

            
```



## <a name="parameters"></a><span data-ttu-id="6c3da-107">參數</span><span class="sxs-lookup"><span data-stu-id="6c3da-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c3da-108">*pidl* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6c3da-108">*pidl* \[in\]</span></span>
</dt> <dd><span data-ttu-id="6c3da-109">要加入之物件的指標。</span><span class="sxs-lookup"><span data-stu-id="6c3da-109">A pointer to the object of interest to add.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c3da-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="6c3da-110">Return value</span></span>

<span data-ttu-id="6c3da-111">如果程式成功，則傳回已加入之物件的新 listview 專案識別碼;否則，會傳回-1。</span><span class="sxs-lookup"><span data-stu-id="6c3da-111">Returns the new listview item ID of the added object if the process was successful; otherwise, returns -1.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c3da-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="6c3da-112">Requirements</span></span>



| <span data-ttu-id="6c3da-113">需求</span><span class="sxs-lookup"><span data-stu-id="6c3da-113">Requirement</span></span> | <span data-ttu-id="6c3da-114">值</span><span class="sxs-lookup"><span data-stu-id="6c3da-114">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="6c3da-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6c3da-115">Minimum supported client</span></span><br/> | <span data-ttu-id="6c3da-116">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6c3da-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="6c3da-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6c3da-117">Minimum supported server</span></span><br/> | <span data-ttu-id="6c3da-118">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6c3da-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="6c3da-119">標頭</span><span class="sxs-lookup"><span data-stu-id="6c3da-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="6c3da-120"><dt>Shlobj.h。h</dt></span><span class="sxs-lookup"><span data-stu-id="6c3da-120"><dt>Shlobj.h</dt></span></span> </dl> |



 

 




