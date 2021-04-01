---
description: 取得代表視圖的資料夾物件。
ms.assetid: 8f3e7827-f2a0-4ce9-b3e9-e6316ec58863
title: 'ShellFolderView 資料夾屬性 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderView.Folder
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 40590064048ba5410dc9341791aec443f16d68e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194439"
---
# <a name="shellfolderviewfolder-property"></a><span data-ttu-id="5bec9-103">ShellFolderView 資料夾屬性</span><span class="sxs-lookup"><span data-stu-id="5bec9-103">ShellFolderView.Folder property</span></span>

<span data-ttu-id="5bec9-104">取得代表視圖的 [**資料夾**](folder.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="5bec9-104">Gets a [**Folder**](folder.md) object that represents the view.</span></span>

<span data-ttu-id="5bec9-105">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="5bec9-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="5bec9-106">語法</span><span class="sxs-lookup"><span data-stu-id="5bec9-106">Syntax</span></span>


```JScript
Folder = ShellFolderView.Folder
```



## <a name="property-value"></a><span data-ttu-id="5bec9-107">屬性值</span><span class="sxs-lookup"><span data-stu-id="5bec9-107">Property value</span></span>

<span data-ttu-id="5bec9-108">接收 [**資料夾**](folder.md) 物件的物件。</span><span class="sxs-lookup"><span data-stu-id="5bec9-108">Object that receives the [**Folder**](folder.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="5bec9-109">備註</span><span class="sxs-lookup"><span data-stu-id="5bec9-109">Remarks</span></span>

<span data-ttu-id="5bec9-110">只能在本機系統上呼叫 **資料夾**。</span><span class="sxs-lookup"><span data-stu-id="5bec9-110">**Folder** can only be called on the local system.</span></span> <span data-ttu-id="5bec9-111">當透過 HTTP 或 UNC 在網頁上執行時，它將無法運作。</span><span class="sxs-lookup"><span data-stu-id="5bec9-111">It will not work when run on a webpage over HTTP or UNC.</span></span>

## <a name="examples"></a><span data-ttu-id="5bec9-112">範例</span><span class="sxs-lookup"><span data-stu-id="5bec9-112">Examples</span></span>

<span data-ttu-id="5bec9-113">下列範例會針對內嵌于 HTML 的 JScript，顯示此屬性的適當用法。</span><span class="sxs-lookup"><span data-stu-id="5bec9-113">The following example shows the proper usage of this property for JScript embedded in HTML.</span></span>


```JScript
<html>
<head>
<title></title>

<script language="JavaScript">
    function fnShellFolderViewFolderJ()
    {
        var objFolder;
        
        objFolder = WebOC.Document.Folder;
        if (objFolder != null)
        {
            alert("Got Folder object");
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
        height=400 VIEWASTEXT>
</object>
<br><br>
<INPUT id=Folder 
       type=button 
       value=Folder 
       name=Folder 
       onclick="fnShellFolderViewFolderJ()">
</body>
</html>
```



## <a name="requirements"></a><span data-ttu-id="5bec9-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="5bec9-114">Requirements</span></span>



| <span data-ttu-id="5bec9-115">需求</span><span class="sxs-lookup"><span data-stu-id="5bec9-115">Requirement</span></span> | <span data-ttu-id="5bec9-116">值</span><span class="sxs-lookup"><span data-stu-id="5bec9-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5bec9-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5bec9-117">Minimum supported client</span></span><br/> | <span data-ttu-id="5bec9-118">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5bec9-118">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="5bec9-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5bec9-119">Minimum supported server</span></span><br/> | <span data-ttu-id="5bec9-120">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5bec9-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="5bec9-121">標頭</span><span class="sxs-lookup"><span data-stu-id="5bec9-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="5bec9-122"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="5bec9-122"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="5bec9-123">Idl</span><span class="sxs-lookup"><span data-stu-id="5bec9-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5bec9-124"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="5bec9-124"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="5bec9-125">DLL</span><span class="sxs-lookup"><span data-stu-id="5bec9-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5bec9-126"><dt>Shell32.dll (4.71 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="5bec9-126"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




