---
description: 將專案加入至 Microsoft Active Desktop。
title: 'ShellUIHelper. AddDesktopComponent 方法 (Exdisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellUIHelper.AddDesktopComponent
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 41634a89-15b9-41c8-ba3f-4bf19b786f6f
ms.openlocfilehash: d5234a0b43ea25c8ac931dc14ec90f7a6696ddfb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973668"
---
# <a name="shelluihelperadddesktopcomponent-method"></a><span data-ttu-id="264a8-103">ShellUIHelper. AddDesktopComponent 方法</span><span class="sxs-lookup"><span data-stu-id="264a8-103">ShellUIHelper.AddDesktopComponent method</span></span>

<span data-ttu-id="264a8-104">將專案加入至 Microsoft Active Desktop。</span><span class="sxs-lookup"><span data-stu-id="264a8-104">Adds an item to the Microsoft Active Desktop.</span></span>

## <a name="syntax"></a><span data-ttu-id="264a8-105">語法</span><span class="sxs-lookup"><span data-stu-id="264a8-105">Syntax</span></span>


```JScript
iRetVal = ShellUIHelper.AddDesktopComponent(
  sURL,
  sType,
  [ Left ],
  [ Top ],
  [ Width ],
  [ Height ]
)
```



## <a name="parameters"></a><span data-ttu-id="264a8-106">參數</span><span class="sxs-lookup"><span data-stu-id="264a8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="264a8-107">*sURL* \[在\]</span><span class="sxs-lookup"><span data-stu-id="264a8-107">*sURL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="264a8-108">類型： **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="264a8-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="264a8-109">指定新的我的最愛專案之 URL 的 **字串** 值。</span><span class="sxs-lookup"><span data-stu-id="264a8-109">A **String** value that specifies the URL of the new favorite item.</span></span>

</dd> <dt>

<span data-ttu-id="264a8-110">*sType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="264a8-110">*sType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="264a8-111">類型： **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="264a8-111">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="264a8-112">**字串** 值，指定要加入的專案類型。</span><span class="sxs-lookup"><span data-stu-id="264a8-112">A **String** value that specifies the type of item being added.</span></span> <span data-ttu-id="264a8-113">這可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="264a8-113">This can be one of the following values.</span></span>

<dt>



 <span data-ttu-id="264a8-114"> (映射) </span><span class="sxs-lookup"><span data-stu-id="264a8-114">(image)</span></span>


</dt> <dd>

<span data-ttu-id="264a8-115">元件為影像。</span><span class="sxs-lookup"><span data-stu-id="264a8-115">The component is an image.</span></span>

</dd> <dt>



 <span data-ttu-id="264a8-116"> (網站) </span><span class="sxs-lookup"><span data-stu-id="264a8-116">(website)</span></span>


</dt> <dd>

<span data-ttu-id="264a8-117">元件是網站。</span><span class="sxs-lookup"><span data-stu-id="264a8-117">The component is a website.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="264a8-118">*左方* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="264a8-118">*Left* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="264a8-119">類型： **Variant**</span><span class="sxs-lookup"><span data-stu-id="264a8-119">Type: **Variant**</span></span>

<span data-ttu-id="264a8-120">元件左邊緣的位置，以螢幕座標為單位。</span><span class="sxs-lookup"><span data-stu-id="264a8-120">The position of the left edge of the component, in screen coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="264a8-121">*頂端* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="264a8-121">*Top* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="264a8-122">類型： **Variant**</span><span class="sxs-lookup"><span data-stu-id="264a8-122">Type: **Variant**</span></span>

<span data-ttu-id="264a8-123">元件上邊緣的位置，以螢幕座標為單位。</span><span class="sxs-lookup"><span data-stu-id="264a8-123">The position of the top edge of the component, in screen coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="264a8-124">*寬度* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="264a8-124">*Width* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="264a8-125">類型： **Variant**</span><span class="sxs-lookup"><span data-stu-id="264a8-125">Type: **Variant**</span></span>

<span data-ttu-id="264a8-126">元件的寬度（以螢幕單位為單位）。</span><span class="sxs-lookup"><span data-stu-id="264a8-126">The width of the component, in screen units.</span></span>

</dd> <dt>

<span data-ttu-id="264a8-127">*高度* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="264a8-127">*Height* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="264a8-128">類型： **Variant**</span><span class="sxs-lookup"><span data-stu-id="264a8-128">Type: **Variant**</span></span>

<span data-ttu-id="264a8-129">元件的高度，以螢幕單位為單位。</span><span class="sxs-lookup"><span data-stu-id="264a8-129">The height of the component, in screen units.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="264a8-130">範例</span><span class="sxs-lookup"><span data-stu-id="264a8-130">Examples</span></span>

<span data-ttu-id="264a8-131">下列範例會針對內嵌于 HTML 和 Visual Basic 中的 JScript，顯示此方法的適當用法。</span><span class="sxs-lookup"><span data-stu-id="264a8-131">The following example shows the proper usage of this method for JScript embedded in HTML and Visual Basic.</span></span>

<span data-ttu-id="264a8-132">Jscript：</span><span class="sxs-lookup"><span data-stu-id="264a8-132">JScript:</span></span>


```JScript
<html>
<head>
<title></title>

<object id="ShellUIHelper"
        classid="CLSID:64AB4BB7-111E-11d1-8F79-00C04FC2FBE1"
        width=0
        height=0
        VIEWASTEXT>
</object>

<script language="JavaScript">
    function fnShellUIHelperAddDesktopComponentJ()
    {
        ShellUIHelper.AddDesktopComponent("https://www.microsoft.com/", "website");
    }
</script>

</head>
<body onload=fnShellUIHelperAddDesktopComponentJ()>
</body>
</html>
```



<span data-ttu-id="264a8-133">Visual Basic：</span><span class="sxs-lookup"><span data-stu-id="264a8-133">Visual Basic:</span></span>


```VB
Private Sub fnShellUIHelperAddDesktopComponentVB()
    Dim objShellUIHelper As ShellUIHelper
    
    Set objShellUIHelper = New ShellUIHelper
        objShellUIHelper.AddDesktopComponent "https://www.microsoft.com/", "website"
    Set objShellUIHelper = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="264a8-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="264a8-134">Requirements</span></span>



| <span data-ttu-id="264a8-135">需求</span><span class="sxs-lookup"><span data-stu-id="264a8-135">Requirement</span></span> | <span data-ttu-id="264a8-136">值</span><span class="sxs-lookup"><span data-stu-id="264a8-136">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="264a8-137">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="264a8-137">Minimum supported client</span></span><br/> | <span data-ttu-id="264a8-138">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="264a8-138">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="264a8-139">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="264a8-139">Minimum supported server</span></span><br/> | <span data-ttu-id="264a8-140">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="264a8-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="264a8-141">標頭</span><span class="sxs-lookup"><span data-stu-id="264a8-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="264a8-142"><dt>Exdisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="264a8-142"><dt>Exdisp.h</dt></span></span> </dl>                            |
| <span data-ttu-id="264a8-143">DLL</span><span class="sxs-lookup"><span data-stu-id="264a8-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="264a8-144"><dt>Shell32.dll (4.71 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="264a8-144"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
