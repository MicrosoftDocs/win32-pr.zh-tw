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
ms.openlocfilehash: 53d6fc3eb6f13d136af603a3129ba75a46c3c6a6
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841039"
---
# <a name="shellfolderviewocselectionchanged-event"></a><span data-ttu-id="88f1a-103">ShellFolderViewOC. SelectionChanged 事件</span><span class="sxs-lookup"><span data-stu-id="88f1a-103">ShellFolderViewOC.SelectionChanged event</span></span>

<span data-ttu-id="88f1a-104">指出視圖中一個或多個專案的選取狀態已變更。</span><span class="sxs-lookup"><span data-stu-id="88f1a-104">Indicates that the selection state of one or more items in the view has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="88f1a-105">語法</span><span class="sxs-lookup"><span data-stu-id="88f1a-105">Syntax</span></span>


```JScript
function EventHandler()
{
    // Code to handle the event.
}

// Set the event property to the handler.
ShellFolderViewOC.SelectionChanged = EventHandler;
```



## <a name="parameters"></a><span data-ttu-id="88f1a-106">參數</span><span class="sxs-lookup"><span data-stu-id="88f1a-106">Parameters</span></span>

<span data-ttu-id="88f1a-107">此事件處理常式沒有參數。</span><span class="sxs-lookup"><span data-stu-id="88f1a-107">This event handler has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="88f1a-108">備註</span><span class="sxs-lookup"><span data-stu-id="88f1a-108">Remarks</span></span>

<span data-ttu-id="88f1a-109">提供此事件的事件處理常式代碼，如下所示。</span><span class="sxs-lookup"><span data-stu-id="88f1a-109">Provide event handling code for this event as shown here.</span></span>


```
 
Private Sub object_SelectionChanged()
    'Event handling code
End Sub
                
```



## <a name="requirements"></a><span data-ttu-id="88f1a-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="88f1a-110">Requirements</span></span>



| <span data-ttu-id="88f1a-111">需求</span><span class="sxs-lookup"><span data-stu-id="88f1a-111">Requirement</span></span> | <span data-ttu-id="88f1a-112">值</span><span class="sxs-lookup"><span data-stu-id="88f1a-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88f1a-113">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="88f1a-113">Minimum supported client</span></span><br/> | <span data-ttu-id="88f1a-114">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="88f1a-114">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="88f1a-115">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="88f1a-115">Minimum supported server</span></span><br/> | <span data-ttu-id="88f1a-116">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="88f1a-116">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="88f1a-117">標頭</span><span class="sxs-lookup"><span data-stu-id="88f1a-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="88f1a-118"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="88f1a-118"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="88f1a-119">Idl</span><span class="sxs-lookup"><span data-stu-id="88f1a-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="88f1a-120"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="88f1a-120"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="88f1a-121">DLL</span><span class="sxs-lookup"><span data-stu-id="88f1a-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="88f1a-122"><dt>Shell32.dll (5.0 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="88f1a-122"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88f1a-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="88f1a-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88f1a-124">**ShellFolderViewOC**</span><span class="sxs-lookup"><span data-stu-id="88f1a-124">**ShellFolderViewOC**</span></span>](shellfolderviewoc-object.md)
</dt> </dl>

 

 




