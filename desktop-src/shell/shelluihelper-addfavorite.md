---
description: 顯示用來建立我的最愛專案的預設使用者介面。 使用者介面會初始化為指定的參數。
title: 'ShellUIHelper. AddFavorite 方法 (Exdisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellUIHelper.AddFavorite
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: b30e776e-642c-4599-b83f-ef15bc0b23d2
ms.openlocfilehash: 2ce6fa0a71bb2ab995e510f06b4403c78bebcc60
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842449"
---
# <a name="shelluihelperaddfavorite-method"></a><span data-ttu-id="3a998-104">ShellUIHelper. AddFavorite 方法</span><span class="sxs-lookup"><span data-stu-id="3a998-104">ShellUIHelper.AddFavorite method</span></span>

<span data-ttu-id="3a998-105">顯示用來建立我的最愛專案的預設使用者介面。</span><span class="sxs-lookup"><span data-stu-id="3a998-105">Displays the default user interface for creating a favorite item.</span></span> <span data-ttu-id="3a998-106">使用者介面會初始化為指定的參數。</span><span class="sxs-lookup"><span data-stu-id="3a998-106">The user interface is initialized to the specified parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a998-107">語法</span><span class="sxs-lookup"><span data-stu-id="3a998-107">Syntax</span></span>


```JScript
iRetVal = ShellUIHelper.AddFavorite(
  sURL,
  [ vTitle ]
)
```



## <a name="parameters"></a><span data-ttu-id="3a998-108">參數</span><span class="sxs-lookup"><span data-stu-id="3a998-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a998-109">*sURL* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3a998-109">*sURL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a998-110">類型： **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="3a998-110">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="3a998-111">**字串** 值，指定要加入至 [我的最愛 **]** 資料夾的專案 URL。</span><span class="sxs-lookup"><span data-stu-id="3a998-111">A **String** value that specifies the URL of the item to be added to the **Favorites** folder.</span></span>

</dd> <dt>

<span data-ttu-id="3a998-112">*vTitle* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="3a998-112">*vTitle* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3a998-113">類型： **Variant \***</span><span class="sxs-lookup"><span data-stu-id="3a998-113">Type: **Variant\***</span></span>

<span data-ttu-id="3a998-114">指定專案名稱的 **變數** 值。</span><span class="sxs-lookup"><span data-stu-id="3a998-114">A **Variant** value that specifies the name of the item.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="3a998-115">範例</span><span class="sxs-lookup"><span data-stu-id="3a998-115">Examples</span></span>

<span data-ttu-id="3a998-116">下列範例會針對內嵌于 HTML 和 Visual Basic 中的 JScript，顯示此方法的適當用法。</span><span class="sxs-lookup"><span data-stu-id="3a998-116">The following example shows the proper usage of this method for JScript embedded in HTML and Visual Basic.</span></span>

<span data-ttu-id="3a998-117">Jscript：</span><span class="sxs-lookup"><span data-stu-id="3a998-117">JScript:</span></span>


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
    function fnShellUIHelperAddFavoriteJ()
    {
        ShellUIHelper.AddFavorite("https://www.msn.com", "MSN Home Page");
    }
</script>

</head>
<body onload=fnShellUIHelperAddFavoriteJ()>
</body>
</html>
```



<span data-ttu-id="3a998-118">Visual Basic：</span><span class="sxs-lookup"><span data-stu-id="3a998-118">Visual Basic:</span></span>


```VB
Private Sub fnShellUIHelperAddFavoriteVB()
    Dim objShellUIHelper As ShellUIHelper
    
    Set objShellUIHelper = New ShellUIHelper
        objShellUIHelper.AddFavorite "https://www.msn.com", "MSN Home Page"
    Set objShellUIHelper = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="3a998-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="3a998-119">Requirements</span></span>



| <span data-ttu-id="3a998-120">需求</span><span class="sxs-lookup"><span data-stu-id="3a998-120">Requirement</span></span> | <span data-ttu-id="3a998-121">值</span><span class="sxs-lookup"><span data-stu-id="3a998-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a998-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3a998-122">Minimum supported client</span></span><br/> | <span data-ttu-id="3a998-123">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3a998-123">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="3a998-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3a998-124">Minimum supported server</span></span><br/> | <span data-ttu-id="3a998-125">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3a998-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="3a998-126">標頭</span><span class="sxs-lookup"><span data-stu-id="3a998-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="3a998-127"><dt>Exdisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="3a998-127"><dt>Exdisp.h</dt></span></span> </dl>                            |
| <span data-ttu-id="3a998-128">DLL</span><span class="sxs-lookup"><span data-stu-id="3a998-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3a998-129"><dt>Shell32.dll (4.71 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="3a998-129"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
