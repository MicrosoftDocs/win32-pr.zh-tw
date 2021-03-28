---
description: 允許回呼物件將按鈕加入至工具列。 由 IShellFolderViewCB：： MessageSFVCB 使用。
title: 'SFVM_GETBUTTONINFO 訊息 (Shlobj.h .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 983652ed-7309-46aa-a6c9-7516411ba5ac
api_name:
- SFVM_GETBUTTONINFO
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: d0db40f7c1f54cd13d54765ba34a8eab31246809
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973485"
---
# <a name="sfvm_getbuttoninfo-message"></a><span data-ttu-id="78dad-104">SFVM \_ GETBUTTONINFO 訊息</span><span class="sxs-lookup"><span data-stu-id="78dad-104">SFVM\_GETBUTTONINFO message</span></span>

<span data-ttu-id="78dad-105">允許回呼物件將按鈕加入至工具列。</span><span class="sxs-lookup"><span data-stu-id="78dad-105">Allows the callback object to add buttons to the toolbar.</span></span> <span data-ttu-id="78dad-106">由 [**IShellFolderViewCB：： MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)使用。</span><span class="sxs-lookup"><span data-stu-id="78dad-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_GETBUTTONINFO 

    lParam = (LPARAM)(LPTBINFO) ptbinfo;

            
```



## <a name="parameters"></a><span data-ttu-id="78dad-107">參數</span><span class="sxs-lookup"><span data-stu-id="78dad-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78dad-108">*ptbinfo* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="78dad-108">*ptbinfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="78dad-109">[**TBINFO**](/windows/desktop/api/Shlobj/ns-shlobj-tbinfo)結構的位址，指定按鈕數目以及如何將其加入工具列。</span><span class="sxs-lookup"><span data-stu-id="78dad-109">The address of a [**TBINFO**](/windows/desktop/api/Shlobj/ns-shlobj-tbinfo) structure that specifies the number of buttons and how they are to be added to the toolbar.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="78dad-110">備註</span><span class="sxs-lookup"><span data-stu-id="78dad-110">Remarks</span></span>

<span data-ttu-id="78dad-111">您可以在標準系統資料夾 view 物件按鈕上附加或顯示按鈕，或顯示這些按鈕來取代標準按鈕。</span><span class="sxs-lookup"><span data-stu-id="78dad-111">Buttons can be appended or prepended to the standard system folder view object buttons, or be displayed in place of the standard buttons.</span></span> <span data-ttu-id="78dad-112">此訊息後面會接著 [**SFVM \_ GETBUTTONS**](sfvm-getbuttons.md) 訊息，以抓取有關按鈕細節的資訊。</span><span class="sxs-lookup"><span data-stu-id="78dad-112">This message is followed by a [**SFVM\_GETBUTTONS**](sfvm-getbuttons.md) message that retrieves the information concerning the button specifics.</span></span>

## <a name="requirements"></a><span data-ttu-id="78dad-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="78dad-113">Requirements</span></span>



| <span data-ttu-id="78dad-114">需求</span><span class="sxs-lookup"><span data-stu-id="78dad-114">Requirement</span></span> | <span data-ttu-id="78dad-115">值</span><span class="sxs-lookup"><span data-stu-id="78dad-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="78dad-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="78dad-116">Minimum supported client</span></span><br/> | <span data-ttu-id="78dad-117">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="78dad-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="78dad-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="78dad-118">Minimum supported server</span></span><br/> | <span data-ttu-id="78dad-119">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="78dad-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="78dad-120">標頭</span><span class="sxs-lookup"><span data-stu-id="78dad-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="78dad-121"><dt>Shlobj.h。h</dt></span><span class="sxs-lookup"><span data-stu-id="78dad-121"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
