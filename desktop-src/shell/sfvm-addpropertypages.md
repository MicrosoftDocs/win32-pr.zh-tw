---
description: 允許回呼物件提供要加入所選取物件之屬性工作表中的頁面。 由 IShellFolderViewCB：： MessageSFVCB 使用。
title: 'SFVM_ADDPROPERTYPAGES 訊息 (Shlobj.h .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 54f67d0e-6089-4e75-a547-5313794e1512
api_name:
- SFVM_ADDPROPERTYPAGES
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: e5f3e1f39b457bce105a8ac2b4be8b5939435615
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104991666"
---
# <a name="sfvm_addpropertypages-message"></a><span data-ttu-id="06ab6-104">SFVM \_ ADDPROPERTYPAGES 訊息</span><span class="sxs-lookup"><span data-stu-id="06ab6-104">SFVM\_ADDPROPERTYPAGES message</span></span>

<span data-ttu-id="06ab6-105">允許回呼物件提供要加入所選取物件之 **屬性** 表中的頁面。</span><span class="sxs-lookup"><span data-stu-id="06ab6-105">Allows the callback object to provide a page to add to the **Properties** property sheet of the selected object.</span></span> <span data-ttu-id="06ab6-106">由 [**IShellFolderViewCB：： MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)使用。</span><span class="sxs-lookup"><span data-stu-id="06ab6-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_ADDPROPERTYPAGES 

    lParam = (LPARAM)(SFVM_PROPPAGE_DATA*) pData;

            
```



## <a name="parameters"></a><span data-ttu-id="06ab6-107">參數</span><span class="sxs-lookup"><span data-stu-id="06ab6-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06ab6-108">*.pdata* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="06ab6-108">*pData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="06ab6-109">[**SFVM \_ PROPPAGE \_ 資料**](/windows/desktop/api/shlobj_core/ns-shlobj_core-sfvm_proppage_data)結構的位址。</span><span class="sxs-lookup"><span data-stu-id="06ab6-109">The address of a [**SFVM\_PROPPAGE\_DATA**](/windows/desktop/api/shlobj_core/ns-shlobj_core-sfvm_proppage_data) structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="06ab6-110">備註</span><span class="sxs-lookup"><span data-stu-id="06ab6-110">Remarks</span></span>

<span data-ttu-id="06ab6-111">此訊息基本上與 [**IShellPropSheetExt：： AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages)有相同的功能。</span><span class="sxs-lookup"><span data-stu-id="06ab6-111">This message serves essentially the same function as [**IShellPropSheetExt::AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages).</span></span> <span data-ttu-id="06ab6-112">如需進一步討論，請參閱 [建立屬性工作表處理常式](propsheet-handlers.md) 。</span><span class="sxs-lookup"><span data-stu-id="06ab6-112">See [Creating Property Sheet Handlers](propsheet-handlers.md) for further discussion.</span></span>

## <a name="requirements"></a><span data-ttu-id="06ab6-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="06ab6-113">Requirements</span></span>



| <span data-ttu-id="06ab6-114">需求</span><span class="sxs-lookup"><span data-stu-id="06ab6-114">Requirement</span></span> | <span data-ttu-id="06ab6-115">值</span><span class="sxs-lookup"><span data-stu-id="06ab6-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="06ab6-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="06ab6-116">Minimum supported client</span></span><br/> | <span data-ttu-id="06ab6-117">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="06ab6-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="06ab6-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="06ab6-118">Minimum supported server</span></span><br/> | <span data-ttu-id="06ab6-119">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="06ab6-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="06ab6-120">標頭</span><span class="sxs-lookup"><span data-stu-id="06ab6-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="06ab6-121"><dt>Shlobj.h。h</dt></span><span class="sxs-lookup"><span data-stu-id="06ab6-121"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
