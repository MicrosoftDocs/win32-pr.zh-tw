---
title: WebViewFolderContents.SelectedItems 方法 (Shldisp.h)
description: WebViewFolderContents. SelectedItems 方法-取得代表 view 中所有選取專案的 FolderItems 物件。
ms.assetid: 683acac4-f157-4a75-a3f8-c693887c1ea5
keywords:
- SelectedItems 方法舊版 Windows 環境功能
- SelectedItems 方法舊版 Windows 環境功能，WebViewFolderContents 物件
- WebViewFolderContents 物件舊版 Windows 環境功能，SelectedItems 方法
topic_type:
- apiref
api_name:
- WebViewFolderContents.SelectedItems
api_location:
- Shell32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25a242991f6f9472610dffa20593f9cab5d8c310
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108102646"
---
# <a name="webviewfoldercontentsselecteditems-method"></a><span data-ttu-id="4d631-106">WebViewFolderContents. SelectedItems 方法</span><span class="sxs-lookup"><span data-stu-id="4d631-106">WebViewFolderContents.SelectedItems method</span></span>

<span data-ttu-id="4d631-107">取得 [**FolderItems**](../shell/folderitems.md) 物件，這個物件表示視圖中所有選取的專案。</span><span class="sxs-lookup"><span data-stu-id="4d631-107">Gets a [**FolderItems**](../shell/folderitems.md) object that represents all of the selected items in the view.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d631-108">語法</span><span class="sxs-lookup"><span data-stu-id="4d631-108">Syntax</span></span>


```JScript
retVal = WebViewFolderContents.SelectedItems()
```



## <a name="parameters"></a><span data-ttu-id="4d631-109">參數</span><span class="sxs-lookup"><span data-stu-id="4d631-109">Parameters</span></span>

<span data-ttu-id="4d631-110">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="4d631-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4d631-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="4d631-111">Return value</span></span>

<span data-ttu-id="4d631-112">類型： **[ **FolderItems**](../shell/folderitems.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="4d631-112">Type: **[**FolderItems**](../shell/folderitems.md)\*\***</span></span>

<span data-ttu-id="4d631-113">[**FolderItems**](../shell/folderitems.md)物件的物件參考。</span><span class="sxs-lookup"><span data-stu-id="4d631-113">An object reference to the [**FolderItems**](../shell/folderitems.md) object.</span></span>

## <a name="examples"></a><span data-ttu-id="4d631-114">範例</span><span class="sxs-lookup"><span data-stu-id="4d631-114">Examples</span></span>

<span data-ttu-id="4d631-115">下列範例會針對內嵌于 HTML 中的 JScript，顯示此方法的適當用法。</span><span class="sxs-lookup"><span data-stu-id="4d631-115">The following example shows the proper usage of this method for JScript embedded in HTML.</span></span>


```HTML
<html>
<head>

...

<script language="JavaScript">
    function fnWebViewFolderContentsSelectedItemsJ()
    {
        var objFolderItems;

        objFolderItems = FileList.SelectedItems();
        if (objFolderItems != null)
        {
            alert(objFolderItems.Count);
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



## <a name="requirements"></a><span data-ttu-id="4d631-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="4d631-116">Requirements</span></span>



| <span data-ttu-id="4d631-117">需求</span><span class="sxs-lookup"><span data-stu-id="4d631-117">Requirement</span></span> | <span data-ttu-id="4d631-118">值</span><span class="sxs-lookup"><span data-stu-id="4d631-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d631-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4d631-119">Minimum supported client</span></span><br/> | <span data-ttu-id="4d631-120">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4d631-120">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="4d631-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4d631-121">Minimum supported server</span></span><br/> | <span data-ttu-id="4d631-122">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4d631-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="4d631-123">標頭</span><span class="sxs-lookup"><span data-stu-id="4d631-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="4d631-124"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="4d631-124"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="4d631-125">Idl</span><span class="sxs-lookup"><span data-stu-id="4d631-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4d631-126"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="4d631-126"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="4d631-127">DLL</span><span class="sxs-lookup"><span data-stu-id="4d631-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4d631-128"><dt>Shell32.dll (4.71 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="4d631-128"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

