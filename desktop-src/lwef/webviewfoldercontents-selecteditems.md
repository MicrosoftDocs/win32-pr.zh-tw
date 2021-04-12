---
title: WebViewFolderContents.SelectedItems 方法 (Shldisp.h)
description: 取得 FolderItems 物件，這個物件表示視圖中所有選取的專案。
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
ms.openlocfilehash: cee4b7f34cdcabec637671af79775fc1fa546790
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025405"
---
# <a name="webviewfoldercontentsselecteditems-method"></a><span data-ttu-id="fac97-106">WebViewFolderContents. SelectedItems 方法</span><span class="sxs-lookup"><span data-stu-id="fac97-106">WebViewFolderContents.SelectedItems method</span></span>

<span data-ttu-id="fac97-107">取得 [**FolderItems**](../shell/folderitems.md) 物件，這個物件表示視圖中所有選取的專案。</span><span class="sxs-lookup"><span data-stu-id="fac97-107">Gets a [**FolderItems**](../shell/folderitems.md) object that represents all of the selected items in the view.</span></span>

## <a name="syntax"></a><span data-ttu-id="fac97-108">語法</span><span class="sxs-lookup"><span data-stu-id="fac97-108">Syntax</span></span>


```JScript
retVal = WebViewFolderContents.SelectedItems()
```



## <a name="parameters"></a><span data-ttu-id="fac97-109">參數</span><span class="sxs-lookup"><span data-stu-id="fac97-109">Parameters</span></span>

<span data-ttu-id="fac97-110">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="fac97-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="fac97-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="fac97-111">Return value</span></span>

<span data-ttu-id="fac97-112">類型： **[ **FolderItems**](../shell/folderitems.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="fac97-112">Type: **[**FolderItems**](../shell/folderitems.md)\*\***</span></span>

<span data-ttu-id="fac97-113">[**FolderItems**](../shell/folderitems.md)物件的物件參考。</span><span class="sxs-lookup"><span data-stu-id="fac97-113">An object reference to the [**FolderItems**](../shell/folderitems.md) object.</span></span>

## <a name="examples"></a><span data-ttu-id="fac97-114">範例</span><span class="sxs-lookup"><span data-stu-id="fac97-114">Examples</span></span>

<span data-ttu-id="fac97-115">下列範例會針對內嵌于 HTML 中的 JScript，顯示此方法的適當用法。</span><span class="sxs-lookup"><span data-stu-id="fac97-115">The following example shows the proper usage of this method for JScript embedded in HTML.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="fac97-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="fac97-116">Requirements</span></span>



| <span data-ttu-id="fac97-117">需求</span><span class="sxs-lookup"><span data-stu-id="fac97-117">Requirement</span></span> | <span data-ttu-id="fac97-118">值</span><span class="sxs-lookup"><span data-stu-id="fac97-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fac97-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fac97-119">Minimum supported client</span></span><br/> | <span data-ttu-id="fac97-120">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fac97-120">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="fac97-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fac97-121">Minimum supported server</span></span><br/> | <span data-ttu-id="fac97-122">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fac97-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="fac97-123">標頭</span><span class="sxs-lookup"><span data-stu-id="fac97-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="fac97-124"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="fac97-124"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="fac97-125">Idl</span><span class="sxs-lookup"><span data-stu-id="fac97-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="fac97-126"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="fac97-126"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="fac97-127">DLL</span><span class="sxs-lookup"><span data-stu-id="fac97-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fac97-128"><dt>Shell32.dll (4.71 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="fac97-128"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

