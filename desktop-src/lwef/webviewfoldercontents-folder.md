---
title: WebViewFolderContents.Folder 屬性 (Shldisp.h)
description: WebViewFolderContents 屬性-取得代表視圖的資料夾物件。
ms.assetid: 1d81c27a-1e48-4c0a-b74d-c63af43a909d
keywords:
- 資料夾屬性舊版 Windows 環境功能
- 資料夾屬性舊版 Windows 環境功能，WebViewFolderContents 物件
- WebViewFolderContents 物件舊版 Windows 環境功能，資料夾屬性
topic_type:
- apiref
api_name:
- WebViewFolderContents.Folder
api_location:
- Shell32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e88fd7a54971fa088bdddbc78d3d8df4af610875
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108102696"
---
# <a name="webviewfoldercontentsfolder-property"></a><span data-ttu-id="6e880-106">WebViewFolderContents 資料夾屬性</span><span class="sxs-lookup"><span data-stu-id="6e880-106">WebViewFolderContents.Folder property</span></span>

<span data-ttu-id="6e880-107">取得代表視圖的 [**資料夾**](../shell/folder.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="6e880-107">Gets a [**Folder**](../shell/folder.md) object that represents the view.</span></span>

<span data-ttu-id="6e880-108">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="6e880-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e880-109">語法</span><span class="sxs-lookup"><span data-stu-id="6e880-109">Syntax</span></span>


```JScript
Folder = WebViewFolderContents.Folder
```



## <a name="property-value"></a><span data-ttu-id="6e880-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="6e880-110">Property value</span></span>

<span data-ttu-id="6e880-111">接收 [**資料夾**](../shell/folder.md) 物件的物件。</span><span class="sxs-lookup"><span data-stu-id="6e880-111">An object that receives the [**Folder**](../shell/folder.md) object.</span></span>

## <a name="examples"></a><span data-ttu-id="6e880-112">範例</span><span class="sxs-lookup"><span data-stu-id="6e880-112">Examples</span></span>

<span data-ttu-id="6e880-113">下列範例示範如何在內嵌于 HTML 的 JScript 中，適當使用此屬性。</span><span class="sxs-lookup"><span data-stu-id="6e880-113">The following example shows the proper usage of this property in JScript embedded in HTML.</span></span>


```HTML
<html>
<head>

...

<script language="JavaScript">
    function fnWebViewFolderContentsFolderJ()
    {
        var objFolder;

        objFolder = FileList.Folder;
        if (objFolder != null)
        {
            alert(objFolder.Title);
        }
    }
</script>

</head>
<body>

...

<object id=FileList classid="clsid:1820FED0-473E-11D0-A96C-00C04FD705A2" tabIndex=1>
</body>
</html>
```



## <a name="requirements"></a><span data-ttu-id="6e880-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="6e880-114">Requirements</span></span>



| <span data-ttu-id="6e880-115">需求</span><span class="sxs-lookup"><span data-stu-id="6e880-115">Requirement</span></span> | <span data-ttu-id="6e880-116">值</span><span class="sxs-lookup"><span data-stu-id="6e880-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e880-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6e880-117">Minimum supported client</span></span><br/> | <span data-ttu-id="6e880-118">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6e880-118">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="6e880-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6e880-119">Minimum supported server</span></span><br/> | <span data-ttu-id="6e880-120">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6e880-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="6e880-121">標頭</span><span class="sxs-lookup"><span data-stu-id="6e880-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="6e880-122"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="6e880-122"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="6e880-123">Idl</span><span class="sxs-lookup"><span data-stu-id="6e880-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6e880-124"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="6e880-124"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="6e880-125">DLL</span><span class="sxs-lookup"><span data-stu-id="6e880-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6e880-126"><dt>Shell32.dll (4.71 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="6e880-126"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

