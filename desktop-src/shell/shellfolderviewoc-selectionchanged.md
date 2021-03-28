---
description: 指出視圖中一個或多個專案的選取狀態已變更。
title: 'ShellFolderViewOC. SelectionChanged 事件 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SelectionChanged
api_type:
- DllExport
api_location:
- Shell32.dll
ms.assetid: 85c37f4e-229f-4383-8218-10f8c2b0b8a0
ms.openlocfilehash: 3f88ad698b990847a9b7f2fa1b74cc5b53ec7beb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320144"
---
# <a name="shellfolderviewocselectionchanged-event"></a><span data-ttu-id="d3e66-103">ShellFolderViewOC. SelectionChanged 事件</span><span class="sxs-lookup"><span data-stu-id="d3e66-103">ShellFolderViewOC.SelectionChanged event</span></span>

<span data-ttu-id="d3e66-104">指出視圖中一個或多個專案的選取狀態已變更。</span><span class="sxs-lookup"><span data-stu-id="d3e66-104">Indicates that the selection state of one or more items in the view has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3e66-105">語法</span><span class="sxs-lookup"><span data-stu-id="d3e66-105">Syntax</span></span>


```JScript
function EventHandler()
{
    // Code to handle the event.
}

// Set the event property to the handler.
ShellFolderViewOC.SelectionChanged = EventHandler;
```



## <a name="parameters"></a><span data-ttu-id="d3e66-106">參數</span><span class="sxs-lookup"><span data-stu-id="d3e66-106">Parameters</span></span>

<span data-ttu-id="d3e66-107">此事件處理常式沒有參數。</span><span class="sxs-lookup"><span data-stu-id="d3e66-107">This event handler has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="d3e66-108">備註</span><span class="sxs-lookup"><span data-stu-id="d3e66-108">Remarks</span></span>

<span data-ttu-id="d3e66-109">提供此事件的事件處理常式代碼，如下所示。</span><span class="sxs-lookup"><span data-stu-id="d3e66-109">Provide event handling code for this event as shown here.</span></span>


```
 
Private Sub object_SelectionChanged()
    'Event handling code
End Sub
                
```



## <a name="requirements"></a><span data-ttu-id="d3e66-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="d3e66-110">Requirements</span></span>



| <span data-ttu-id="d3e66-111">需求</span><span class="sxs-lookup"><span data-stu-id="d3e66-111">Requirement</span></span> | <span data-ttu-id="d3e66-112">值</span><span class="sxs-lookup"><span data-stu-id="d3e66-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3e66-113">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d3e66-113">Minimum supported client</span></span><br/> | <span data-ttu-id="d3e66-114">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d3e66-114">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d3e66-115">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d3e66-115">Minimum supported server</span></span><br/> | <span data-ttu-id="d3e66-116">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d3e66-116">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="d3e66-117">標頭</span><span class="sxs-lookup"><span data-stu-id="d3e66-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="d3e66-118"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="d3e66-118"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="d3e66-119">Idl</span><span class="sxs-lookup"><span data-stu-id="d3e66-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d3e66-120"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="d3e66-120"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="d3e66-121">DLL</span><span class="sxs-lookup"><span data-stu-id="d3e66-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d3e66-122"><dt>Shell32.dll (5.0 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="d3e66-122"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d3e66-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d3e66-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3e66-124">**ShellFolderViewOC**</span><span class="sxs-lookup"><span data-stu-id="d3e66-124">**ShellFolderViewOC**</span></span>](shellfolderviewoc-object.md)
</dt> </dl>

 

 




