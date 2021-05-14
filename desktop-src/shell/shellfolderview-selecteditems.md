---
description: ShellFolderView. SelectedItems 方法-取得代表 view 中所有選取專案的 FolderItems 物件。
title: 'ShellFolderView. SelectedItems 方法 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderView.SelectedItems
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 1ee3bf2e-f9c9-47d9-a0f2-efedd69770c5
ms.openlocfilehash: 485eda530adc4955abb27899d67ac0900eb0a910
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/12/2021
ms.locfileid: "109840739"
---
# <a name="shellfolderviewselecteditems-method"></a><span data-ttu-id="e54d8-103">ShellFolderView. SelectedItems 方法</span><span class="sxs-lookup"><span data-stu-id="e54d8-103">ShellFolderView.SelectedItems method</span></span>

<span data-ttu-id="e54d8-104">取得 [**FolderItems**](folderitems.md) 物件，這個物件表示視圖中所有選取的專案。</span><span class="sxs-lookup"><span data-stu-id="e54d8-104">Gets a [**FolderItems**](folderitems.md) object that represents all of the selected items in the view.</span></span>

## <a name="syntax"></a><span data-ttu-id="e54d8-105">語法</span><span class="sxs-lookup"><span data-stu-id="e54d8-105">Syntax</span></span>


```JScript
retVal = ShellFolderView.SelectedItems()
```



## <a name="parameters"></a><span data-ttu-id="e54d8-106">參數</span><span class="sxs-lookup"><span data-stu-id="e54d8-106">Parameters</span></span>

<span data-ttu-id="e54d8-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="e54d8-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e54d8-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="e54d8-108">Return value</span></span>

<span data-ttu-id="e54d8-109">類型： **[ **FolderItems**](folderitems.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="e54d8-109">Type: **[**FolderItems**](folderitems.md)\*\***</span></span>

<span data-ttu-id="e54d8-110">[**FolderItems**](folderitems.md)物件的物件參考。</span><span class="sxs-lookup"><span data-stu-id="e54d8-110">An object reference to the [**FolderItems**](folderitems.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="e54d8-111">備註</span><span class="sxs-lookup"><span data-stu-id="e54d8-111">Remarks</span></span>

<span data-ttu-id="e54d8-112">**SelectedItems** 只能在本機系統上呼叫。</span><span class="sxs-lookup"><span data-stu-id="e54d8-112">**SelectedItems** can only be called on the local system.</span></span> <span data-ttu-id="e54d8-113">當透過 HTTP 或 UNC 在網頁上執行時，它將無法運作。</span><span class="sxs-lookup"><span data-stu-id="e54d8-113">It will not work when run on a webpage over HTTP or UNC.</span></span>

## <a name="examples"></a><span data-ttu-id="e54d8-114">範例</span><span class="sxs-lookup"><span data-stu-id="e54d8-114">Examples</span></span>

<span data-ttu-id="e54d8-115">下列範例示範如何在內嵌于 HTML 的 JScript 中正確使用這個方法。</span><span class="sxs-lookup"><span data-stu-id="e54d8-115">The following example shows the proper use of this method in JScript embedded in HTML.</span></span>


```JScript
<html>
<head>
<title></title>

<script language="JavaScript">
    function fnShellFolderViewSelectedItemsJ()
    {
        var objFolderItems;
        
        objFolderItems = WebOC.Document.SelectedItems();
        if (objFolderItems != null)
        {
            alert("Got FolderItems object.");
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
<INPUT id=SelectedItems 
       type=button 
       value=SelectedItems 
       name=SelectedItems 
       onclick="fnShellFolderViewSelectedItemsJ()">
</body>
</html>
```



## <a name="requirements"></a><span data-ttu-id="e54d8-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="e54d8-116">Requirements</span></span>



| <span data-ttu-id="e54d8-117">需求</span><span class="sxs-lookup"><span data-stu-id="e54d8-117">Requirement</span></span> | <span data-ttu-id="e54d8-118">值</span><span class="sxs-lookup"><span data-stu-id="e54d8-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e54d8-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e54d8-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e54d8-120">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e54d8-120">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="e54d8-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e54d8-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e54d8-122">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e54d8-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="e54d8-123">標頭</span><span class="sxs-lookup"><span data-stu-id="e54d8-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="e54d8-124"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="e54d8-124"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="e54d8-125">Idl</span><span class="sxs-lookup"><span data-stu-id="e54d8-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e54d8-126"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="e54d8-126"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="e54d8-127">DLL</span><span class="sxs-lookup"><span data-stu-id="e54d8-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e54d8-128"><dt>Shell32.dll (4.71 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="e54d8-128"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




