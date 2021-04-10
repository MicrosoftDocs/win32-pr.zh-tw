---
title: 'WebViewFolderContents. PopupItemMenu 方法 (Shldisp .h) '
description: 為指定的專案建立快捷方式功能表，並傳回選取的命令字串。
ms.assetid: 3c07500c-2fe9-4976-a1a8-b128e75f9325
keywords:
- PopupItemMenu 方法舊版 Windows 環境功能
- PopupItemMenu 方法舊版 Windows 環境功能，WebViewFolderContents 物件
- WebViewFolderContents 物件舊版 Windows 環境功能，PopupItemMenu 方法
topic_type:
- apiref
api_name:
- WebViewFolderContents.PopupItemMenu
api_location:
- Shell32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41753814f103998185acc798a37447f22356d2aa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685564"
---
# <a name="webviewfoldercontentspopupitemmenu-method"></a><span data-ttu-id="778c2-106">WebViewFolderContents. PopupItemMenu 方法</span><span class="sxs-lookup"><span data-stu-id="778c2-106">WebViewFolderContents.PopupItemMenu method</span></span>

<span data-ttu-id="778c2-107">為指定的專案建立快捷方式功能表，並傳回選取的命令字串。</span><span class="sxs-lookup"><span data-stu-id="778c2-107">Creates a shortcut menu for the specified item and returns the selected command string.</span></span>

## <a name="syntax"></a><span data-ttu-id="778c2-108">語法</span><span class="sxs-lookup"><span data-stu-id="778c2-108">Syntax</span></span>


```JScript
retVal = WebViewFolderContents.PopupItemMenu(
  vItem,
  [ vx ],
  [ vy ]
)
```



## <a name="parameters"></a><span data-ttu-id="778c2-109">參數</span><span class="sxs-lookup"><span data-stu-id="778c2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="778c2-110">*vItem* \[在\]</span><span class="sxs-lookup"><span data-stu-id="778c2-110">*vItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="778c2-111">類型： **Variant**</span><span class="sxs-lookup"><span data-stu-id="778c2-111">Type: **Variant**</span></span>

<span data-ttu-id="778c2-112">將建立快捷方式功能表的 [**FolderItem**](../shell/folderitem.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="778c2-112">The [**FolderItem**](../shell/folderitem.md) object for which the shortcut menu will be created.</span></span>

</dd> <dt>

<span data-ttu-id="778c2-113">*vx* \[ in、optional\]</span><span class="sxs-lookup"><span data-stu-id="778c2-113">*vx* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="778c2-114">類型： **Variant**</span><span class="sxs-lookup"><span data-stu-id="778c2-114">Type: **Variant**</span></span>

<span data-ttu-id="778c2-115">功能表的水準位置（以螢幕座標為單位）。</span><span class="sxs-lookup"><span data-stu-id="778c2-115">The horizontal position of the menu, in screen coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="778c2-116">*vy* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="778c2-116">*vy* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="778c2-117">類型： **Variant**</span><span class="sxs-lookup"><span data-stu-id="778c2-117">Type: **Variant**</span></span>

<span data-ttu-id="778c2-118">功能表的垂直位置（以螢幕座標為單位）。</span><span class="sxs-lookup"><span data-stu-id="778c2-118">The vertical position of the menu, in screen coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="778c2-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="778c2-119">Return value</span></span>

<span data-ttu-id="778c2-120">類型： \**[BSTR](/previous-versions/windows/desktop/automat/bstr) \** _</span><span class="sxs-lookup"><span data-stu-id="778c2-120">Type: \**[BSTR](/previous-versions/windows/desktop/automat/bstr)\** _</span></span>

<span data-ttu-id="778c2-121">當此方法傳回時，會包含命令字串。</span><span class="sxs-lookup"><span data-stu-id="778c2-121">When this method returns, contains the command string.</span></span>

## <a name="examples"></a><span data-ttu-id="778c2-122">範例</span><span class="sxs-lookup"><span data-stu-id="778c2-122">Examples</span></span>

<span data-ttu-id="778c2-123">下列範例示範如何適當地使用 _ *PopupItemMenu*\* 來內嵌于 HTML 中的 JScript。</span><span class="sxs-lookup"><span data-stu-id="778c2-123">The following example shows the proper use of _ *PopupItemMenu*\* for JScript embedded in HTML.</span></span>


```HTML
<html>
<head>

...

<script language="JavaScript">
    function fnWebViewFolderContentsPopupItemMenuJ()
    {
        var objFolderItem;

        objFolderItem = FileList.FocusedItem;
        if (objFolderItem != null)
        {
            var szCommand;

            szCommand = FileList.PopupItemMenu(objFolderItem);
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



## <a name="requirements"></a><span data-ttu-id="778c2-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="778c2-124">Requirements</span></span>



| <span data-ttu-id="778c2-125">需求</span><span class="sxs-lookup"><span data-stu-id="778c2-125">Requirement</span></span> | <span data-ttu-id="778c2-126">值</span><span class="sxs-lookup"><span data-stu-id="778c2-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="778c2-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="778c2-127">Minimum supported client</span></span><br/> | <span data-ttu-id="778c2-128">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="778c2-128">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="778c2-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="778c2-129">Minimum supported server</span></span><br/> | <span data-ttu-id="778c2-130">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="778c2-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="778c2-131">標頭</span><span class="sxs-lookup"><span data-stu-id="778c2-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="778c2-132"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="778c2-132"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="778c2-133">Idl</span><span class="sxs-lookup"><span data-stu-id="778c2-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="778c2-134"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="778c2-134"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="778c2-135">DLL</span><span class="sxs-lookup"><span data-stu-id="778c2-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="778c2-136"><dt>Shell32.dll (4.71 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="778c2-136"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

