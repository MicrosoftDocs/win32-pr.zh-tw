---
description: ShellFolderView. FocusedItem 屬性-取得代表具有輸入焦點之專案的 FolderItem 物件。
ms.assetid: ca88801d-c8fa-4c1c-9294-f52eada40ff6
title: 'ShellFolderView. FocusedItem 屬性 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderView.FocusedItem
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 4f661f555f1492a3323fa3749a8dffd6f00f411d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104006"
---
# <a name="shellfolderviewfocuseditem-property"></a><span data-ttu-id="41a23-103">ShellFolderView. FocusedItem 屬性</span><span class="sxs-lookup"><span data-stu-id="41a23-103">ShellFolderView.FocusedItem property</span></span>

<span data-ttu-id="41a23-104">取得代表具有輸入焦點之專案的 [**FolderItem**](folderitem.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="41a23-104">Gets a [**FolderItem**](folderitem.md) object that represents the item that has the input focus.</span></span>

<span data-ttu-id="41a23-105">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="41a23-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="41a23-106">語法</span><span class="sxs-lookup"><span data-stu-id="41a23-106">Syntax</span></span>


```JScript
objFocusedItem = ShellFolderView.FocusedItem
```



## <a name="property-value"></a><span data-ttu-id="41a23-107">屬性值</span><span class="sxs-lookup"><span data-stu-id="41a23-107">Property value</span></span>

<span data-ttu-id="41a23-108">[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)型別的變數，可接收焦點的專案物件。</span><span class="sxs-lookup"><span data-stu-id="41a23-108">A variable of type [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) that receives the focused item object.</span></span>

## <a name="remarks"></a><span data-ttu-id="41a23-109">備註</span><span class="sxs-lookup"><span data-stu-id="41a23-109">Remarks</span></span>

<span data-ttu-id="41a23-110">**FocusedItem** 只能在本機系統上呼叫。</span><span class="sxs-lookup"><span data-stu-id="41a23-110">**FocusedItem** can only be called on the local system.</span></span> <span data-ttu-id="41a23-111">當透過 HTTP 或 UNC 在網頁上執行時，它將無法運作。</span><span class="sxs-lookup"><span data-stu-id="41a23-111">It will not work when run on a webpage over HTTP or UNC.</span></span>

## <a name="examples"></a><span data-ttu-id="41a23-112">範例</span><span class="sxs-lookup"><span data-stu-id="41a23-112">Examples</span></span>

<span data-ttu-id="41a23-113">下列範例示範如何在內嵌于 HTML 的 JScript 中正確使用這個方法。</span><span class="sxs-lookup"><span data-stu-id="41a23-113">The following example shows the proper use of this method in JScript embedded in HTML.</span></span>


```JScript
<html>
<head>
<title></title>

<script language="JavaScript">
    function fnShellFolderViewFocusedItemJ()
    {
        var objFolderItem;
        
        objFolderItem = WebOC.Document.FocusedItem;
        if (objFolderItem != null)
        {
            alert("Got FolderItem object.");
        }
    }
    
    function fnLoad()
    {
        var webOC;
        
        webOC = document.all("WebOC");
        webOC.Navigate("C:\\");
    }
</script>

</head>
<body onload="fnLoad()">
<object id="WebOC"
        classid="clsid:8856F961-340A-11D0-A96B-00C04FD705A2"
        width=400
        height=400>
</object>
<br><br>
<INPUT id=FocusedItem 
       type=button 
       value=FocusedItem 
       name=FocusedItem 
       onclick="fnShellFolderViewFocusedItemJ()">
</body>
</html>
```



## <a name="requirements"></a><span data-ttu-id="41a23-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="41a23-114">Requirements</span></span>



| <span data-ttu-id="41a23-115">需求</span><span class="sxs-lookup"><span data-stu-id="41a23-115">Requirement</span></span> | <span data-ttu-id="41a23-116">值</span><span class="sxs-lookup"><span data-stu-id="41a23-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41a23-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="41a23-117">Minimum supported client</span></span><br/> | <span data-ttu-id="41a23-118">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="41a23-118">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="41a23-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="41a23-119">Minimum supported server</span></span><br/> | <span data-ttu-id="41a23-120">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="41a23-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="41a23-121">標頭</span><span class="sxs-lookup"><span data-stu-id="41a23-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="41a23-122"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="41a23-122"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="41a23-123">Idl</span><span class="sxs-lookup"><span data-stu-id="41a23-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="41a23-124"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="41a23-124"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="41a23-125">DLL</span><span class="sxs-lookup"><span data-stu-id="41a23-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="41a23-126"><dt>Shell32.dll (4.71 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="41a23-126"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
