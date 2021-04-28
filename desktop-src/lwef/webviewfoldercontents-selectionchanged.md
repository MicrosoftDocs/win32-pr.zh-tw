---
title: 'WebViewFolderContents. SelectionChanged 事件 (Shldisp .h) '
description: WebViewFolderContents. SelectionChanged 事件-在 view 中的任何專案或專案的選取狀態變更時，就會發生此事件。
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
ms.openlocfilehash: ea6176cb2a1703d48cd2ddec8069c65d7efc978f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108102656"
---
# <a name="webviewfoldercontentsselectionchanged-event"></a><span data-ttu-id="b16b8-104">WebViewFolderContents. SelectionChanged 事件</span><span class="sxs-lookup"><span data-stu-id="b16b8-104">WebViewFolderContents.SelectionChanged event</span></span>

<span data-ttu-id="b16b8-105">發生于視圖中任何專案或專案的選取狀態變更時。</span><span class="sxs-lookup"><span data-stu-id="b16b8-105">Occurs when the selection state of any item or items in the view has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="b16b8-106">語法</span><span class="sxs-lookup"><span data-stu-id="b16b8-106">Syntax</span></span>


```JScript
function EventHandler()
{
    // Code to handle the event.
}

// Set the event property to the handler.
WebViewFolderContents.SelectionChanged = EventHandler;
```



## <a name="parameters"></a><span data-ttu-id="b16b8-107">參數</span><span class="sxs-lookup"><span data-stu-id="b16b8-107">Parameters</span></span>

<span data-ttu-id="b16b8-108">此事件處理常式沒有參數。</span><span class="sxs-lookup"><span data-stu-id="b16b8-108">This event handler has no parameters.</span></span>

## <a name="examples"></a><span data-ttu-id="b16b8-109">範例</span><span class="sxs-lookup"><span data-stu-id="b16b8-109">Examples</span></span>

<span data-ttu-id="b16b8-110">下列範例會針對內嵌于 HTML 的 JScript，顯示此事件的適當用法。</span><span class="sxs-lookup"><span data-stu-id="b16b8-110">The following example shows the proper usage of this event for JScript embedded in HTML.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="b16b8-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="b16b8-111">Requirements</span></span>



| <span data-ttu-id="b16b8-112">需求</span><span class="sxs-lookup"><span data-stu-id="b16b8-112">Requirement</span></span> | <span data-ttu-id="b16b8-113">值</span><span class="sxs-lookup"><span data-stu-id="b16b8-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b16b8-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b16b8-114">Minimum supported client</span></span><br/> | <span data-ttu-id="b16b8-115">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b16b8-115">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="b16b8-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b16b8-116">Minimum supported server</span></span><br/> | <span data-ttu-id="b16b8-117">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b16b8-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="b16b8-118">標頭</span><span class="sxs-lookup"><span data-stu-id="b16b8-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="b16b8-119"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="b16b8-119"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="b16b8-120">Idl</span><span class="sxs-lookup"><span data-stu-id="b16b8-120">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b16b8-121"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="b16b8-121"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="b16b8-122">DLL</span><span class="sxs-lookup"><span data-stu-id="b16b8-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b16b8-123"><dt>Shell32.dll (4.71 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="b16b8-123"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 





