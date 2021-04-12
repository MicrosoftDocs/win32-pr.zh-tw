---
title: 'WebViewFolderContents. ViewOptions 屬性 (Shldisp .h) '
description: 取得一組 ShellFolderViewOptions 旗標，指出視圖的目前選項。
ms.assetid: 96edb144-e532-4ab5-99ae-d945e211d744
keywords:
- ViewOptions 屬性舊版 Windows 環境功能
- ViewOptions 屬性舊版 Windows 環境功能，WebViewFolderContents 物件
- WebViewFolderContents 物件舊版 Windows 環境功能，ViewOptions 屬性
topic_type:
- apiref
api_name:
- WebViewFolderContents.ViewOptions
api_location:
- Shell32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 737ec5cb22fdc5c0002006898b837b557b5f6089
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024682"
---
# <a name="webviewfoldercontentsviewoptions-property"></a><span data-ttu-id="2f20f-106">WebViewFolderContents. ViewOptions 屬性</span><span class="sxs-lookup"><span data-stu-id="2f20f-106">WebViewFolderContents.ViewOptions property</span></span>

<span data-ttu-id="2f20f-107">取得一組 [**ShellFolderViewOptions**](/windows/desktop/api/shldisp/ne-shldisp-shellfolderviewoptions) 旗標，指出視圖的目前選項。</span><span class="sxs-lookup"><span data-stu-id="2f20f-107">Gets a set of [**ShellFolderViewOptions**](/windows/desktop/api/shldisp/ne-shldisp-shellfolderviewoptions) flags that indicate the current options of the view.</span></span>

<span data-ttu-id="2f20f-108">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="2f20f-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f20f-109">語法</span><span class="sxs-lookup"><span data-stu-id="2f20f-109">Syntax</span></span>


```JScript
objViewOptions = WebViewFolderContents.ViewOptions
```



## <a name="property-value"></a><span data-ttu-id="2f20f-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="2f20f-110">Property value</span></span>

<span data-ttu-id="2f20f-111">[IDispatch](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch)型別的變數，可接收 view options 物件。</span><span class="sxs-lookup"><span data-stu-id="2f20f-111">A variable of type [IDispatch](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) that receives the view options object.</span></span>

## <a name="examples"></a><span data-ttu-id="2f20f-112">範例</span><span class="sxs-lookup"><span data-stu-id="2f20f-112">Examples</span></span>

<span data-ttu-id="2f20f-113">下列範例示範如何在內嵌于 HTML 的 JScript 中，適當使用此屬性。</span><span class="sxs-lookup"><span data-stu-id="2f20f-113">The following example shows the proper usage of this property in JScript embedded in HTML.</span></span>


```HTML
<html>
<head>

...

<script language="JavaScript">
    function fnWebViewFolderContentsViewOptionsJ()
    {
        var nViewOptions;

        nViewOptions = FileList.ViewOptions;
        if (nViewOptions != "")
        {
            alert(nViewOptions);
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



## <a name="requirements"></a><span data-ttu-id="2f20f-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="2f20f-114">Requirements</span></span>



| <span data-ttu-id="2f20f-115">需求</span><span class="sxs-lookup"><span data-stu-id="2f20f-115">Requirement</span></span> | <span data-ttu-id="2f20f-116">值</span><span class="sxs-lookup"><span data-stu-id="2f20f-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f20f-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2f20f-117">Minimum supported client</span></span><br/> | <span data-ttu-id="2f20f-118">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2f20f-118">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="2f20f-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2f20f-119">Minimum supported server</span></span><br/> | <span data-ttu-id="2f20f-120">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2f20f-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="2f20f-121">標頭</span><span class="sxs-lookup"><span data-stu-id="2f20f-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="2f20f-122"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="2f20f-122"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="2f20f-123">Idl</span><span class="sxs-lookup"><span data-stu-id="2f20f-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2f20f-124"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="2f20f-124"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="2f20f-125">DLL</span><span class="sxs-lookup"><span data-stu-id="2f20f-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2f20f-126"><dt>Shell32.dll (4.71 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="2f20f-126"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

