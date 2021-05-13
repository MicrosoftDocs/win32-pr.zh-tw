---
description: 指出 ShellFolderView 物件已完成資料夾內容的列舉。
title: 'ShellFolderViewOC. EnumDone 事件 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumDone
api_type:
- DllExport
api_location:
- Shell32.dll
ms.assetid: 7baa5f58-62c2-406e-a81e-4ca9c446a756
ms.openlocfilehash: 00b0e58ed18ab0da9c3fa362da4b8e3e066cdcc4
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841049"
---
# <a name="shellfolderviewocenumdone-event"></a><span data-ttu-id="6ff76-103">ShellFolderViewOC. EnumDone 事件</span><span class="sxs-lookup"><span data-stu-id="6ff76-103">ShellFolderViewOC.EnumDone event</span></span>

<span data-ttu-id="6ff76-104">指出 [**ShellFolderView**](shellfolderview.md) 物件已完成資料夾內容的列舉。</span><span class="sxs-lookup"><span data-stu-id="6ff76-104">Indicates that the [**ShellFolderView**](shellfolderview.md) object has finished enumerating the folder's contents.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ff76-105">語法</span><span class="sxs-lookup"><span data-stu-id="6ff76-105">Syntax</span></span>


```JScript
function EventHandler()
{
    // Code to handle the event.
}

// Set the event property to the handler.
ShellFolderViewOC.EnumDone = EventHandler;
```



## <a name="parameters"></a><span data-ttu-id="6ff76-106">參數</span><span class="sxs-lookup"><span data-stu-id="6ff76-106">Parameters</span></span>

<span data-ttu-id="6ff76-107">此事件處理常式沒有參數。</span><span class="sxs-lookup"><span data-stu-id="6ff76-107">This event handler has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="6ff76-108">備註</span><span class="sxs-lookup"><span data-stu-id="6ff76-108">Remarks</span></span>

<span data-ttu-id="6ff76-109">[**ShellFolderView**](shellfolderview.md)物件必須先列舉資料夾的內容，才能加以顯示。</span><span class="sxs-lookup"><span data-stu-id="6ff76-109">The [**ShellFolderView**](shellfolderview.md) object must enumerate the contents of a folder before it can display it.</span></span> <span data-ttu-id="6ff76-110">如果資料夾很大或位於遠端系統上，此程式可能需要數分鐘的時間。</span><span class="sxs-lookup"><span data-stu-id="6ff76-110">With folders that are large or located on a remote system, this process can take as much as several minutes.</span></span> <span data-ttu-id="6ff76-111">在這段期間，會顯示動畫的空出圖，向使用者指出正在進行處理。</span><span class="sxs-lookup"><span data-stu-id="6ff76-111">During this time, an animated flashlight graphic is displayed to indicate to the user that processing is under way.</span></span> <span data-ttu-id="6ff76-112">列舉完成之後，就會引發 **EnumDone** 事件，並以資料夾的內容取代下圖。</span><span class="sxs-lookup"><span data-stu-id="6ff76-112">Once the enumeration is complete, the **EnumDone** event is fired and the flashlight graphic is replaced by the contents of the folder.</span></span>

<span data-ttu-id="6ff76-113">提供此事件的事件處理常式代碼，如下所示。</span><span class="sxs-lookup"><span data-stu-id="6ff76-113">Provide event handling code for this event as shown here.</span></span>


```
 
Private Sub object_EnumDone()
    'Event handling code
End Sub
                
```



## <a name="requirements"></a><span data-ttu-id="6ff76-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="6ff76-114">Requirements</span></span>



| <span data-ttu-id="6ff76-115">需求</span><span class="sxs-lookup"><span data-stu-id="6ff76-115">Requirement</span></span> | <span data-ttu-id="6ff76-116">值</span><span class="sxs-lookup"><span data-stu-id="6ff76-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ff76-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6ff76-117">Minimum supported client</span></span><br/> | <span data-ttu-id="6ff76-118">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6ff76-118">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6ff76-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6ff76-119">Minimum supported server</span></span><br/> | <span data-ttu-id="6ff76-120">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6ff76-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="6ff76-121">標頭</span><span class="sxs-lookup"><span data-stu-id="6ff76-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="6ff76-122"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="6ff76-122"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="6ff76-123">Idl</span><span class="sxs-lookup"><span data-stu-id="6ff76-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6ff76-124"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="6ff76-124"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="6ff76-125">DLL</span><span class="sxs-lookup"><span data-stu-id="6ff76-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6ff76-126"><dt>Shell32.dll (5.0 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="6ff76-126"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ff76-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6ff76-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ff76-128">**ShellFolderViewOC**</span><span class="sxs-lookup"><span data-stu-id="6ff76-128">**ShellFolderViewOC**</span></span>](shellfolderviewoc-object.md)
</dt> </dl>

 

 




