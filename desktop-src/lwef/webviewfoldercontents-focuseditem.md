---
title: 'WebViewFolderContents. FocusedItem 屬性 (Shldisp .h) '
description: WebViewFolderContents. FocusedItem 屬性-取得代表具有輸入焦點之專案的 FolderItem 物件。
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
ms.openlocfilehash: 724743b81f605dc9ba5794a4a796b8a0c4a2a03f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108102726"
---
# <a name="webviewfoldercontentsfocuseditem-property"></a><span data-ttu-id="57be2-106">WebViewFolderContents. FocusedItem 屬性</span><span class="sxs-lookup"><span data-stu-id="57be2-106">WebViewFolderContents.FocusedItem property</span></span>

<span data-ttu-id="57be2-107">取得代表具有輸入焦點之專案的 [**FolderItem**](../shell/folderitem.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="57be2-107">Gets a [**FolderItem**](../shell/folderitem.md) object that represents the item that has the input focus.</span></span>

<span data-ttu-id="57be2-108">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="57be2-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="57be2-109">語法</span><span class="sxs-lookup"><span data-stu-id="57be2-109">Syntax</span></span>


```JScript
objFocusedItem = WebViewFolderContents.FocusedItem
```



## <a name="property-value"></a><span data-ttu-id="57be2-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="57be2-110">Property value</span></span>

<span data-ttu-id="57be2-111">[IDispatch](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch)型別的變數，可接收焦點的專案物件。</span><span class="sxs-lookup"><span data-stu-id="57be2-111">A variable of type [IDispatch](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) that receives the focused item object.</span></span>

## <a name="examples"></a><span data-ttu-id="57be2-112">範例</span><span class="sxs-lookup"><span data-stu-id="57be2-112">Examples</span></span>

<span data-ttu-id="57be2-113">下列範例示範如何在內嵌于 HTML 的 JScript 中，適當使用此屬性。</span><span class="sxs-lookup"><span data-stu-id="57be2-113">The following example shows the proper usage of this property in JScript embedded in HTML.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="57be2-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="57be2-114">Requirements</span></span>



| <span data-ttu-id="57be2-115">需求</span><span class="sxs-lookup"><span data-stu-id="57be2-115">Requirement</span></span> | <span data-ttu-id="57be2-116">值</span><span class="sxs-lookup"><span data-stu-id="57be2-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="57be2-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="57be2-117">Minimum supported client</span></span><br/> | <span data-ttu-id="57be2-118">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="57be2-118">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="57be2-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="57be2-119">Minimum supported server</span></span><br/> | <span data-ttu-id="57be2-120">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="57be2-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="57be2-121">標頭</span><span class="sxs-lookup"><span data-stu-id="57be2-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="57be2-122"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="57be2-122"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="57be2-123">Idl</span><span class="sxs-lookup"><span data-stu-id="57be2-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="57be2-124"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="57be2-124"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="57be2-125">DLL</span><span class="sxs-lookup"><span data-stu-id="57be2-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="57be2-126"><dt>Shell32.dll (4.71 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="57be2-126"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

