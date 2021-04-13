---
title: 'WebViewFolderContents. FocusedItem 屬性 (Shldisp .h) '
description: 取得代表具有輸入焦點之專案的 FolderItem 物件。
ms.assetid: 84cf92ac-dadb-4741-8383-a8ae1d35d4e0
keywords:
- FocusedItem 屬性舊版 Windows 環境功能
- FocusedItem 屬性舊版 Windows 環境功能，WebViewFolderContents 物件
- WebViewFolderContents 物件舊版 Windows 環境功能，FocusedItem 屬性
topic_type:
- apiref
api_name:
- WebViewFolderContents.FocusedItem
api_location:
- Shell32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 050e7c2a4c280a949ec3684e2b05610830315a37
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104383942"
---
# <a name="webviewfoldercontentsfocuseditem-property"></a><span data-ttu-id="0fa7b-106">WebViewFolderContents. FocusedItem 屬性</span><span class="sxs-lookup"><span data-stu-id="0fa7b-106">WebViewFolderContents.FocusedItem property</span></span>

<span data-ttu-id="0fa7b-107">取得代表具有輸入焦點之專案的 [**FolderItem**](../shell/folderitem.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="0fa7b-107">Gets a [**FolderItem**](../shell/folderitem.md) object that represents the item that has the input focus.</span></span>

<span data-ttu-id="0fa7b-108">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="0fa7b-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="0fa7b-109">語法</span><span class="sxs-lookup"><span data-stu-id="0fa7b-109">Syntax</span></span>


```JScript
objFocusedItem = WebViewFolderContents.FocusedItem
```



## <a name="property-value"></a><span data-ttu-id="0fa7b-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="0fa7b-110">Property value</span></span>

<span data-ttu-id="0fa7b-111">[IDispatch](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch)型別的變數，可接收焦點的專案物件。</span><span class="sxs-lookup"><span data-stu-id="0fa7b-111">A variable of type [IDispatch](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) that receives the focused item object.</span></span>

## <a name="examples"></a><span data-ttu-id="0fa7b-112">範例</span><span class="sxs-lookup"><span data-stu-id="0fa7b-112">Examples</span></span>

<span data-ttu-id="0fa7b-113">下列範例示範如何在內嵌于 HTML 的 JScript 中，適當使用此屬性。</span><span class="sxs-lookup"><span data-stu-id="0fa7b-113">The following example shows the proper usage of this property in JScript embedded in HTML.</span></span>


```HTML
<html>
<head>

...

<script language="JavaScript">
    function fnWebViewFolderContentsFocusedItemJ()
    {
        var objFolderItem;

        objFolderItem = FileList.FocusedItem;
        if (objFolderItem != null)
        {
            alert(objFolderItem.Name);
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



## <a name="requirements"></a><span data-ttu-id="0fa7b-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="0fa7b-114">Requirements</span></span>



| <span data-ttu-id="0fa7b-115">需求</span><span class="sxs-lookup"><span data-stu-id="0fa7b-115">Requirement</span></span> | <span data-ttu-id="0fa7b-116">值</span><span class="sxs-lookup"><span data-stu-id="0fa7b-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0fa7b-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0fa7b-117">Minimum supported client</span></span><br/> | <span data-ttu-id="0fa7b-118">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0fa7b-118">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="0fa7b-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0fa7b-119">Minimum supported server</span></span><br/> | <span data-ttu-id="0fa7b-120">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0fa7b-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="0fa7b-121">標頭</span><span class="sxs-lookup"><span data-stu-id="0fa7b-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="0fa7b-122"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="0fa7b-122"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="0fa7b-123">Idl</span><span class="sxs-lookup"><span data-stu-id="0fa7b-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0fa7b-124"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="0fa7b-124"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="0fa7b-125">DLL</span><span class="sxs-lookup"><span data-stu-id="0fa7b-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0fa7b-126"><dt>Shell32.dll (4.71 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="0fa7b-126"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

