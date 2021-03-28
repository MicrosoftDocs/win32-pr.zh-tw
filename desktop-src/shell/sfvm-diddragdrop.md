---
description: SFVM \_ DIDDRAGDROP 可能已變更或無法使用。
ms.assetid: 5d37cf61-d8a7-4afa-9159-fea13d2b1d59
title: 'SFVM_DIDDRAGDROP 訊息 (Shlobj.h .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 025bcf6320b014ff31b0819f394dd8b76fa90e59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104991682"
---
# <a name="sfvm_diddragdrop-message"></a><span data-ttu-id="5267c-103">SFVM \_ DIDDRAGDROP 訊息</span><span class="sxs-lookup"><span data-stu-id="5267c-103">SFVM\_DIDDRAGDROP message</span></span>

<span data-ttu-id="5267c-104">\[**SFVM \_DIDDRAGDROP** 可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="5267c-104">\[**SFVM\_DIDDRAGDROP** is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="5267c-105">它在後續版本中可能會變更或無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="5267c-105">It may be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="5267c-106">通知回呼函式已開始拖放作業。</span><span class="sxs-lookup"><span data-stu-id="5267c-106">Notifies the callback function that a drag-and-drop operation has begun.</span></span> <span data-ttu-id="5267c-107">由 [**IShellFolderViewCB：： MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)使用。</span><span class="sxs-lookup"><span data-stu-id="5267c-107">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_DIDDRAGDROP 
    wParam = (WPARAM)(DWORD) dwEffect;
    lParam = (LPARAM)(IDataObject*) pIdo;
            
```



## <a name="parameters"></a><span data-ttu-id="5267c-108">參數</span><span class="sxs-lookup"><span data-stu-id="5267c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5267c-109">*dwEffect* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5267c-109">*dwEffect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5267c-110">來自 [**DROPEFFECT**](../com/dropeffect-constants.md) 列舉的 drop 效果規範。</span><span class="sxs-lookup"><span data-stu-id="5267c-110">A drop effect specifier from the [**DROPEFFECT**](../com/dropeffect-constants.md) enumeration.</span></span> <span data-ttu-id="5267c-111">這是藉由呼叫 [**SHDoDragDrop**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shdodragdrop)來取得。</span><span class="sxs-lookup"><span data-stu-id="5267c-111">This is obtained by calling [**SHDoDragDrop**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shdodragdrop).</span></span>

</dd> <dt>

<span data-ttu-id="5267c-112">*pIdo* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5267c-112">*pIdo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5267c-113">[**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject)實例的指標。</span><span class="sxs-lookup"><span data-stu-id="5267c-113">A pointer to the [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) instance.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5267c-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="5267c-114">Requirements</span></span>



| <span data-ttu-id="5267c-115">需求</span><span class="sxs-lookup"><span data-stu-id="5267c-115">Requirement</span></span> | <span data-ttu-id="5267c-116">值</span><span class="sxs-lookup"><span data-stu-id="5267c-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="5267c-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5267c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="5267c-118">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5267c-118">Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="5267c-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5267c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="5267c-120">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5267c-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="5267c-121">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="5267c-121">End of client support</span></span><br/>    | <span data-ttu-id="5267c-122">Windows XP 含 SP2</span><span class="sxs-lookup"><span data-stu-id="5267c-122">Windows XP with SP2</span></span><br/>                                                      |
| <span data-ttu-id="5267c-123">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="5267c-123">End of server support</span></span><br/>    | <span data-ttu-id="5267c-124">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="5267c-124">Windows Server 2003</span></span><br/>                                                      |
| <span data-ttu-id="5267c-125">標頭</span><span class="sxs-lookup"><span data-stu-id="5267c-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="5267c-126"><dt>Shlobj.h。h</dt></span><span class="sxs-lookup"><span data-stu-id="5267c-126"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
