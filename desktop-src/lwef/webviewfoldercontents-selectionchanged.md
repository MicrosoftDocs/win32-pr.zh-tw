---
title: 'WebViewFolderContents. SelectionChanged 事件 (Shldisp .h) '
description: 發生于視圖中任何專案或專案的選取狀態變更時。
ms.assetid: 46dfceec-aa81-4950-81e5-526a6e621271
keywords:
- SelectionChanged 事件舊版 Windows 環境功能
topic_type:
- apiref
api_name:
- SelectionChanged
api_location:
- Shell32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8421e9d06ff9fd24256da8a23cdd100b5749968
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509223"
---
# <a name="webviewfoldercontentsselectionchanged-event"></a><span data-ttu-id="23472-104">WebViewFolderContents. SelectionChanged 事件</span><span class="sxs-lookup"><span data-stu-id="23472-104">WebViewFolderContents.SelectionChanged event</span></span>

<span data-ttu-id="23472-105">發生于視圖中任何專案或專案的選取狀態變更時。</span><span class="sxs-lookup"><span data-stu-id="23472-105">Occurs when the selection state of any item or items in the view has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="23472-106">語法</span><span class="sxs-lookup"><span data-stu-id="23472-106">Syntax</span></span>


```JScript
function EventHandler()
{
    // Code to handle the event.
}

// Set the event property to the handler.
WebViewFolderContents.SelectionChanged = EventHandler;
```



## <a name="parameters"></a><span data-ttu-id="23472-107">參數</span><span class="sxs-lookup"><span data-stu-id="23472-107">Parameters</span></span>

<span data-ttu-id="23472-108">此事件處理常式沒有參數。</span><span class="sxs-lookup"><span data-stu-id="23472-108">This event handler has no parameters.</span></span>

## <a name="examples"></a><span data-ttu-id="23472-109">範例</span><span class="sxs-lookup"><span data-stu-id="23472-109">Examples</span></span>

<span data-ttu-id="23472-110">下列範例會針對內嵌于 HTML 的 JScript，顯示此事件的適當用法。</span><span class="sxs-lookup"><span data-stu-id="23472-110">The following example shows the proper usage of this event for JScript embedded in HTML.</span></span>


```HTML
<html>
<head>

...

<script language="JavaScript">
    function fnWebViewFolderContentsSelectionChangedJ()
    {
        alert("SelectionChanged event was called");
    }
</script>

<script language="JavaScript" for="FileList" event="SelectionChanged">
    fnWebViewFolderContentsSelectionChangedJ();
</script>

</head>
<body>

...

<object id=FileList classid="clsid:1820FED0-473E-11D0-A96C-00C04FD705A2" tabIndex=1>
</body>
</html>
```



## <a name="requirements"></a><span data-ttu-id="23472-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="23472-111">Requirements</span></span>



| <span data-ttu-id="23472-112">需求</span><span class="sxs-lookup"><span data-stu-id="23472-112">Requirement</span></span> | <span data-ttu-id="23472-113">值</span><span class="sxs-lookup"><span data-stu-id="23472-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="23472-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="23472-114">Minimum supported client</span></span><br/> | <span data-ttu-id="23472-115">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="23472-115">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="23472-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="23472-116">Minimum supported server</span></span><br/> | <span data-ttu-id="23472-117">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="23472-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="23472-118">標頭</span><span class="sxs-lookup"><span data-stu-id="23472-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="23472-119"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="23472-119"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="23472-120">Idl</span><span class="sxs-lookup"><span data-stu-id="23472-120">IDL</span></span><br/>                      | <dl> <span data-ttu-id="23472-121"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="23472-121"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="23472-122">DLL</span><span class="sxs-lookup"><span data-stu-id="23472-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="23472-123"><dt>Shell32.dll (4.71 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="23472-123"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 





