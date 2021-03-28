---
description: 取得一組旗標，指出視圖的目前選項。
ms.assetid: 83a17033-bd7f-44de-a0c8-460d12c4825d
title: 'ShellFolderView. ViewOptions 屬性 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderView.ViewOptions
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: e336034e7d5037b8037c6fd0ef549fe5f87da312
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104991719"
---
# <a name="shellfolderviewviewoptions-property"></a><span data-ttu-id="9f677-103">ShellFolderView. ViewOptions 屬性</span><span class="sxs-lookup"><span data-stu-id="9f677-103">ShellFolderView.ViewOptions property</span></span>

<span data-ttu-id="9f677-104">取得一組旗標，指出視圖的目前選項。</span><span class="sxs-lookup"><span data-stu-id="9f677-104">Gets a set of flags that indicate the current options of the view.</span></span>

<span data-ttu-id="9f677-105">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="9f677-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f677-106">語法</span><span class="sxs-lookup"><span data-stu-id="9f677-106">Syntax</span></span>


```JScript
objViewOptions = ShellFolderView.ViewOptions
```



## <a name="property-value"></a><span data-ttu-id="9f677-107">屬性值</span><span class="sxs-lookup"><span data-stu-id="9f677-107">Property value</span></span>

<span data-ttu-id="9f677-108">[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)型別的變數，可接收 view options 物件。</span><span class="sxs-lookup"><span data-stu-id="9f677-108">A variable of type [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) that receives the view options object.</span></span> <span data-ttu-id="9f677-109">包含下列一或多個值：</span><span class="sxs-lookup"><span data-stu-id="9f677-109">Contains one or more of the following values:</span></span>

<dt>

<span id="SFVVO_SHOWALLOBJECTS"></span><span id="sfvvo_showallobjects"></span>

<span data-ttu-id="9f677-110"><span id="SFVVO_SHOWALLOBJECTS"></span><span id="sfvvo_showallobjects"></span>**SFVVO \_SHOWALLOBJECTS** (0x00000001) </span><span class="sxs-lookup"><span data-stu-id="9f677-110"><span id="SFVVO_SHOWALLOBJECTS"></span><span id="sfvvo_showallobjects"></span>**SFVVO\_SHOWALLOBJECTS** (0x00000001)</span></span>


</dt> <dd>

<span data-ttu-id="9f677-111">[ **顯示所有** 檔案] 選項為啟用狀態。</span><span class="sxs-lookup"><span data-stu-id="9f677-111">The **Show All Files** option is enabled.</span></span>

</dd> <dt>

<span id="SFVVO_SHOWEXTENSIONS"></span><span id="sfvvo_showextensions"></span>

<span data-ttu-id="9f677-112"><span id="SFVVO_SHOWEXTENSIONS"></span><span id="sfvvo_showextensions"></span>**SFVVO \_SHOWEXTENSIONS** (0x00000002) </span><span class="sxs-lookup"><span data-stu-id="9f677-112"><span id="SFVVO_SHOWEXTENSIONS"></span><span id="sfvvo_showextensions"></span>**SFVVO\_SHOWEXTENSIONS** (0x00000002)</span></span>


</dt> <dd>

<span data-ttu-id="9f677-113">[ **隱藏已知檔案類型的副檔名** ] 選項已停用。</span><span class="sxs-lookup"><span data-stu-id="9f677-113">The **Hide extensions for known file types** option is disabled.</span></span>

</dd> <dt>

<span id="SFVVO_SHOWCOMPCOLOR"></span><span id="sfvvo_showcompcolor"></span>

<span data-ttu-id="9f677-114"><span id="SFVVO_SHOWCOMPCOLOR"></span><span id="sfvvo_showcompcolor"></span>**SFVVO \_SHOWCOMPCOLOR** (0x00000008) </span><span class="sxs-lookup"><span data-stu-id="9f677-114"><span id="SFVVO_SHOWCOMPCOLOR"></span><span id="sfvvo_showcompcolor"></span>**SFVVO\_SHOWCOMPCOLOR** (0x00000008)</span></span>


</dt> <dd>

<span data-ttu-id="9f677-115">[ **顯示具有替代色彩的壓縮檔案和資料夾** ] 選項為啟用狀態。</span><span class="sxs-lookup"><span data-stu-id="9f677-115">The **Display Compressed Files and Folders with Alternate Color** option is enabled.</span></span>

</dd> <dt>

<span id="SFVVO_SHOWSYSFILES"></span><span id="sfvvo_showsysfiles"></span>

<span data-ttu-id="9f677-116"><span id="SFVVO_SHOWSYSFILES"></span><span id="sfvvo_showsysfiles"></span>**SFVVO \_SHOWSYSFILES** (0x00000020) </span><span class="sxs-lookup"><span data-stu-id="9f677-116"><span id="SFVVO_SHOWSYSFILES"></span><span id="sfvvo_showsysfiles"></span>**SFVVO\_SHOWSYSFILES** (0x00000020)</span></span>


</dt> <dd>

<span data-ttu-id="9f677-117">[不 **顯示隱藏** 的檔案] 選項已啟用。</span><span class="sxs-lookup"><span data-stu-id="9f677-117">The **Do Not Show Hidden Files** option is enabled.</span></span>

</dd> <dt>

<span id="SFVVO_WIN95CLASSIC"></span><span id="sfvvo_win95classic"></span>

<span data-ttu-id="9f677-118"><span id="SFVVO_WIN95CLASSIC"></span><span id="sfvvo_win95classic"></span>**SFVVO \_WIN95CLASSIC** (0x00000040) </span><span class="sxs-lookup"><span data-stu-id="9f677-118"><span id="SFVVO_WIN95CLASSIC"></span><span id="sfvvo_win95classic"></span>**SFVVO\_WIN95CLASSIC** (0x00000040)</span></span>


</dt> <dd>

<span data-ttu-id="9f677-119">[ **傳統樣式** ] 選項已啟用。</span><span class="sxs-lookup"><span data-stu-id="9f677-119">The **Classic Style** option is enabled.</span></span>

</dd> <dt>

<span id="SFVVO_DOUBLECLICKINWEBVIEW"></span><span id="sfvvo_doubleclickinwebview"></span>

<span data-ttu-id="9f677-120"><span id="SFVVO_DOUBLECLICKINWEBVIEW"></span><span id="sfvvo_doubleclickinwebview"></span>**SFVVO \_DOUBLECLICKINWEBVIEW** (0x00000080) </span><span class="sxs-lookup"><span data-stu-id="9f677-120"><span id="SFVVO_DOUBLECLICKINWEBVIEW"></span><span id="sfvvo_doubleclickinwebview"></span>**SFVVO\_DOUBLECLICKINWEBVIEW** (0x00000080)</span></span>


</dt> <dd>

<span data-ttu-id="9f677-121">**按兩下以開啟專案** 選項已啟用。</span><span class="sxs-lookup"><span data-stu-id="9f677-121">The **Double-Click to Open an Item** option is enabled.</span></span>

</dd> <dt>

<span id="SFVVO_DESKTOPHTML"></span><span id="sfvvo_desktophtml"></span>

<span data-ttu-id="9f677-122"><span id="SFVVO_DESKTOPHTML"></span><span id="sfvvo_desktophtml"></span>**SFVVO \_DESKTOPHTML** (0x00000200) </span><span class="sxs-lookup"><span data-stu-id="9f677-122"><span id="SFVVO_DESKTOPHTML"></span><span id="sfvvo_desktophtml"></span>**SFVVO\_DESKTOPHTML** (0x00000200)</span></span>


</dt> <dd>

<span data-ttu-id="9f677-123">[ **Active Desktop – View As Web Page** ] 選項為 enabled。</span><span class="sxs-lookup"><span data-stu-id="9f677-123">The **Active Desktop – View as Web Page** option is enabled.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9f677-124">備註</span><span class="sxs-lookup"><span data-stu-id="9f677-124">Remarks</span></span>

<span data-ttu-id="9f677-125">[**FocusedItem**](shellfolderview-focuseditem.md) 只能在本機系統上呼叫。</span><span class="sxs-lookup"><span data-stu-id="9f677-125">[**FocusedItem**](shellfolderview-focuseditem.md) can only be called on the local system.</span></span> <span data-ttu-id="9f677-126">當透過 HTTP 或 UNC 在網頁上執行時，它將無法運作。</span><span class="sxs-lookup"><span data-stu-id="9f677-126">It will not work when run on a webpage over HTTP or UNC.</span></span>

## <a name="examples"></a><span data-ttu-id="9f677-127">範例</span><span class="sxs-lookup"><span data-stu-id="9f677-127">Examples</span></span>

<span data-ttu-id="9f677-128">下列範例示範如何在內嵌于 HTML 的 JScript 中正確使用這個方法。</span><span class="sxs-lookup"><span data-stu-id="9f677-128">The following example shows the proper use of this method in JScript embedded in HTML.</span></span>


```JScript
<html>
<head>
<title></title>

<script language="JavaScript">
    function fnShellFolderViewViewOptionsJ()
    {
        var objOptions;
        
        objOptions = WebOC.Document.ViewOptions;
        if (objOptions != null)
        {
            alert(objOptions);
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
<INPUT id=ViewOptions 
       type=button 
       value=ViewOptions 
       name=ViewOptions 
       onclick="fnShellFolderViewViewOptionsJ()">
</body>
</html>
```



## <a name="requirements"></a><span data-ttu-id="9f677-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="9f677-129">Requirements</span></span>



| <span data-ttu-id="9f677-130">需求</span><span class="sxs-lookup"><span data-stu-id="9f677-130">Requirement</span></span> | <span data-ttu-id="9f677-131">值</span><span class="sxs-lookup"><span data-stu-id="9f677-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f677-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9f677-132">Minimum supported client</span></span><br/> | <span data-ttu-id="9f677-133">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9f677-133">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="9f677-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9f677-134">Minimum supported server</span></span><br/> | <span data-ttu-id="9f677-135">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9f677-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="9f677-136">標頭</span><span class="sxs-lookup"><span data-stu-id="9f677-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="9f677-137"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="9f677-137"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="9f677-138">Idl</span><span class="sxs-lookup"><span data-stu-id="9f677-138">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9f677-139"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="9f677-139"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="9f677-140">DLL</span><span class="sxs-lookup"><span data-stu-id="9f677-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9f677-141"><dt>Shell32.dll (4.71 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="9f677-141"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
