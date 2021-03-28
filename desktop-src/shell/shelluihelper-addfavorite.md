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
ms.openlocfilehash: a5c3cae52f0ad18c1f2ddf6cf91759d1c6daf6c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973733"
---
# <a name="shelluihelperaddfavorite-method"></a><span data-ttu-id="e0dbc-104">ShellUIHelper. AddFavorite 方法</span><span class="sxs-lookup"><span data-stu-id="e0dbc-104">ShellUIHelper.AddFavorite method</span></span>

<span data-ttu-id="e0dbc-105">顯示用來建立我的最愛專案的預設使用者介面。</span><span class="sxs-lookup"><span data-stu-id="e0dbc-105">Displays the default user interface for creating a favorite item.</span></span> <span data-ttu-id="e0dbc-106">使用者介面會初始化為指定的參數。</span><span class="sxs-lookup"><span data-stu-id="e0dbc-106">The user interface is initialized to the specified parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0dbc-107">語法</span><span class="sxs-lookup"><span data-stu-id="e0dbc-107">Syntax</span></span>


```JScript
iRetVal = ShellUIHelper.AddFavorite(
  sURL,
  [ vTitle ]
)
```



## <a name="parameters"></a><span data-ttu-id="e0dbc-108">參數</span><span class="sxs-lookup"><span data-stu-id="e0dbc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0dbc-109">*sURL* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e0dbc-109">*sURL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e0dbc-110">類型： **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="e0dbc-110">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="e0dbc-111">**字串** 值，指定要加入至 [我的最愛 **]** 資料夾的專案 URL。</span><span class="sxs-lookup"><span data-stu-id="e0dbc-111">A **String** value that specifies the URL of the item to be added to the **Favorites** folder.</span></span>

</dd> <dt>

<span data-ttu-id="e0dbc-112">*vTitle* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="e0dbc-112">*vTitle* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e0dbc-113">類型： \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="e0dbc-113">Type: \**Variant\** _</span></span>

<span data-ttu-id="e0dbc-114">_ *Variant*\* 值，指定專案的名稱。</span><span class="sxs-lookup"><span data-stu-id="e0dbc-114">A _ *Variant*\* value that specifies the name of the item.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="e0dbc-115">範例</span><span class="sxs-lookup"><span data-stu-id="e0dbc-115">Examples</span></span>

<span data-ttu-id="e0dbc-116">下列範例會針對內嵌于 HTML 和 Visual Basic 中的 JScript，顯示此方法的適當用法。</span><span class="sxs-lookup"><span data-stu-id="e0dbc-116">The following example shows the proper usage of this method for JScript embedded in HTML and Visual Basic.</span></span>

<span data-ttu-id="e0dbc-117">Jscript：</span><span class="sxs-lookup"><span data-stu-id="e0dbc-117">JScript:</span></span>


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



<span data-ttu-id="e0dbc-118">Visual Basic：</span><span class="sxs-lookup"><span data-stu-id="e0dbc-118">Visual Basic:</span></span>


```VB
Private Sub fnShellUIHelperAddFavoriteVB()
    Dim objShellUIHelper As ShellUIHelper
    
    Set objShellUIHelper = New ShellUIHelper
        objShellUIHelper.AddFavorite "https://www.msn.com", "MSN Home Page"
    Set objShellUIHelper = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="e0dbc-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="e0dbc-119">Requirements</span></span>



| <span data-ttu-id="e0dbc-120">需求</span><span class="sxs-lookup"><span data-stu-id="e0dbc-120">Requirement</span></span> | <span data-ttu-id="e0dbc-121">值</span><span class="sxs-lookup"><span data-stu-id="e0dbc-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0dbc-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e0dbc-122">Minimum supported client</span></span><br/> | <span data-ttu-id="e0dbc-123">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e0dbc-123">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="e0dbc-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e0dbc-124">Minimum supported server</span></span><br/> | <span data-ttu-id="e0dbc-125">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e0dbc-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="e0dbc-126">標頭</span><span class="sxs-lookup"><span data-stu-id="e0dbc-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="e0dbc-127"><dt>Exdisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="e0dbc-127"><dt>Exdisp.h</dt></span></span> </dl>                            |
| <span data-ttu-id="e0dbc-128">DLL</span><span class="sxs-lookup"><span data-stu-id="e0dbc-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e0dbc-129"><dt>Shell32.dll (4.71 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="e0dbc-129"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
