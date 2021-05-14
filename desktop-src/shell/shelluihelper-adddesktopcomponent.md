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
ms.openlocfilehash: 2edaa79bd62dcee40e4f197700d2128cb0b2070d
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842459"
---
# <a name="shelluihelperadddesktopcomponent-method"></a><span data-ttu-id="a0e07-103">ShellUIHelper. AddDesktopComponent 方法</span><span class="sxs-lookup"><span data-stu-id="a0e07-103">ShellUIHelper.AddDesktopComponent method</span></span>

<span data-ttu-id="a0e07-104">將專案加入至 Microsoft Active Desktop。</span><span class="sxs-lookup"><span data-stu-id="a0e07-104">Adds an item to the Microsoft Active Desktop.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0e07-105">語法</span><span class="sxs-lookup"><span data-stu-id="a0e07-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="a0e07-106">參數</span><span class="sxs-lookup"><span data-stu-id="a0e07-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0e07-107">*sURL* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a0e07-107">*sURL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0e07-108">類型： **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="a0e07-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="a0e07-109">指定新的我的最愛專案之 URL 的 **字串** 值。</span><span class="sxs-lookup"><span data-stu-id="a0e07-109">A **String** value that specifies the URL of the new favorite item.</span></span>

</dd> <dt>

<span data-ttu-id="a0e07-110">*sType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a0e07-110">*sType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0e07-111">類型： **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="a0e07-111">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="a0e07-112">**字串** 值，指定要加入的專案類型。</span><span class="sxs-lookup"><span data-stu-id="a0e07-112">A **String** value that specifies the type of item being added.</span></span> <span data-ttu-id="a0e07-113">這可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="a0e07-113">This can be one of the following values.</span></span>

<dt>



 <span data-ttu-id="a0e07-114"> (映射) </span><span class="sxs-lookup"><span data-stu-id="a0e07-114">(image)</span></span>


</dt> <dd>

<span data-ttu-id="a0e07-115">元件為影像。</span><span class="sxs-lookup"><span data-stu-id="a0e07-115">The component is an image.</span></span>

</dd> <dt>



 <span data-ttu-id="a0e07-116"> (網站) </span><span class="sxs-lookup"><span data-stu-id="a0e07-116">(website)</span></span>


</dt> <dd>

<span data-ttu-id="a0e07-117">元件是網站。</span><span class="sxs-lookup"><span data-stu-id="a0e07-117">The component is a website.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="a0e07-118">*左方* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="a0e07-118">*Left* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a0e07-119">類型： **Variant**</span><span class="sxs-lookup"><span data-stu-id="a0e07-119">Type: **Variant**</span></span>

<span data-ttu-id="a0e07-120">元件左邊緣的位置，以螢幕座標為單位。</span><span class="sxs-lookup"><span data-stu-id="a0e07-120">The position of the left edge of the component, in screen coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="a0e07-121">*頂端* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="a0e07-121">*Top* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a0e07-122">類型： **Variant**</span><span class="sxs-lookup"><span data-stu-id="a0e07-122">Type: **Variant**</span></span>

<span data-ttu-id="a0e07-123">元件上邊緣的位置，以螢幕座標為單位。</span><span class="sxs-lookup"><span data-stu-id="a0e07-123">The position of the top edge of the component, in screen coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="a0e07-124">*寬度* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="a0e07-124">*Width* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a0e07-125">類型： **Variant**</span><span class="sxs-lookup"><span data-stu-id="a0e07-125">Type: **Variant**</span></span>

<span data-ttu-id="a0e07-126">元件的寬度（以螢幕單位為單位）。</span><span class="sxs-lookup"><span data-stu-id="a0e07-126">The width of the component, in screen units.</span></span>

</dd> <dt>

<span data-ttu-id="a0e07-127">*高度* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="a0e07-127">*Height* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a0e07-128">類型： **Variant**</span><span class="sxs-lookup"><span data-stu-id="a0e07-128">Type: **Variant**</span></span>

<span data-ttu-id="a0e07-129">元件的高度，以螢幕單位為單位。</span><span class="sxs-lookup"><span data-stu-id="a0e07-129">The height of the component, in screen units.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="a0e07-130">範例</span><span class="sxs-lookup"><span data-stu-id="a0e07-130">Examples</span></span>

<span data-ttu-id="a0e07-131">下列範例會針對內嵌于 HTML 和 Visual Basic 中的 JScript，顯示此方法的適當用法。</span><span class="sxs-lookup"><span data-stu-id="a0e07-131">The following example shows the proper usage of this method for JScript embedded in HTML and Visual Basic.</span></span>

<span data-ttu-id="a0e07-132">Jscript：</span><span class="sxs-lookup"><span data-stu-id="a0e07-132">JScript:</span></span>


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



<span data-ttu-id="a0e07-133">Visual Basic：</span><span class="sxs-lookup"><span data-stu-id="a0e07-133">Visual Basic:</span></span>


```VB
Private Sub fnShellUIHelperAddDesktopComponentVB()
    Dim objShellUIHelper As ShellUIHelper
    
    Set objShellUIHelper = New ShellUIHelper
        objShellUIHelper.AddDesktopComponent "https://www.microsoft.com/", "website"
    Set objShellUIHelper = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="a0e07-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="a0e07-134">Requirements</span></span>



| <span data-ttu-id="a0e07-135">需求</span><span class="sxs-lookup"><span data-stu-id="a0e07-135">Requirement</span></span> | <span data-ttu-id="a0e07-136">值</span><span class="sxs-lookup"><span data-stu-id="a0e07-136">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0e07-137">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a0e07-137">Minimum supported client</span></span><br/> | <span data-ttu-id="a0e07-138">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a0e07-138">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="a0e07-139">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a0e07-139">Minimum supported server</span></span><br/> | <span data-ttu-id="a0e07-140">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a0e07-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="a0e07-141">標頭</span><span class="sxs-lookup"><span data-stu-id="a0e07-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="a0e07-142"><dt>Exdisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="a0e07-142"><dt>Exdisp.h</dt></span></span> </dl>                            |
| <span data-ttu-id="a0e07-143">DLL</span><span class="sxs-lookup"><span data-stu-id="a0e07-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a0e07-144"><dt>Shell32.dll (4.71 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="a0e07-144"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
