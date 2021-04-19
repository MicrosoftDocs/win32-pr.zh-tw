---
title: 'WebViewFolderContents： Script 屬性 (Shldisp .h) '
description: 取得視圖的腳本物件。
ms.assetid: f65246c5-3cd6-43bd-b267-ad27bdd0b41e
keywords:
- 腳本屬性舊版 Windows 環境功能
- 腳本屬性舊版 Windows 環境功能，WebViewFolderContents 物件
- WebViewFolderContents 物件舊版 Windows 環境功能，腳本屬性
topic_type:
- apiref
api_name:
- WebViewFolderContents.Script
api_location:
- Shell32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92133278d73851fa43353c116a2385da9b0fd3da
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106996584"
---
# <a name="webviewfoldercontentsscript-property"></a><span data-ttu-id="11daa-106">WebViewFolderContents。 Script 屬性</span><span class="sxs-lookup"><span data-stu-id="11daa-106">WebViewFolderContents.Script property</span></span>

<span data-ttu-id="11daa-107">取得視圖的腳本物件。</span><span class="sxs-lookup"><span data-stu-id="11daa-107">Gets the scripting object for the view.</span></span>

<span data-ttu-id="11daa-108">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="11daa-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="11daa-109">語法</span><span class="sxs-lookup"><span data-stu-id="11daa-109">Syntax</span></span>


```JScript
objScript = WebViewFolderContents.Script
```



## <a name="property-value"></a><span data-ttu-id="11daa-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="11daa-110">Property value</span></span>

<span data-ttu-id="11daa-111">[IDispatch](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch)型別的變數，它會接收腳本物件。</span><span class="sxs-lookup"><span data-stu-id="11daa-111">A variable of type [IDispatch](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) that receives the scripting object.</span></span>

## <a name="examples"></a><span data-ttu-id="11daa-112">範例</span><span class="sxs-lookup"><span data-stu-id="11daa-112">Examples</span></span>

<span data-ttu-id="11daa-113">下列範例示範如何在內嵌于 HTML 的 JScript 中，適當使用此屬性。</span><span class="sxs-lookup"><span data-stu-id="11daa-113">The following example shows the proper usage of this property in JScript embedded in HTML.</span></span>


```HTML
<html>
<head>

...

<script language="JavaScript">
    function fnWebViewFolderContentsScriptJ()
    {
        var objScript;

        objScript = FileList.Script;
        if (objScript != null)
        {
            alert(objScript.Name);
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



## <a name="requirements"></a><span data-ttu-id="11daa-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="11daa-114">Requirements</span></span>



| <span data-ttu-id="11daa-115">需求</span><span class="sxs-lookup"><span data-stu-id="11daa-115">Requirement</span></span> | <span data-ttu-id="11daa-116">值</span><span class="sxs-lookup"><span data-stu-id="11daa-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11daa-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="11daa-117">Minimum supported client</span></span><br/> | <span data-ttu-id="11daa-118">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="11daa-118">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="11daa-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="11daa-119">Minimum supported server</span></span><br/> | <span data-ttu-id="11daa-120">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="11daa-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="11daa-121">標頭</span><span class="sxs-lookup"><span data-stu-id="11daa-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="11daa-122"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="11daa-122"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="11daa-123">Idl</span><span class="sxs-lookup"><span data-stu-id="11daa-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="11daa-124"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="11daa-124"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="11daa-125">DLL</span><span class="sxs-lookup"><span data-stu-id="11daa-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="11daa-126"><dt>Shell32.dll (4.71 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="11daa-126"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

