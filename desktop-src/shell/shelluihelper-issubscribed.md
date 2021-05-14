---
description: 指出是否已訂閱指定的 URL。
title: 'ShellUIHelper. IsSubscribed 方法 (Exdisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellUIHelper.IsSubscribed
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: fcf23352-6603-4b17-9c3b-b353cca1c003
ms.openlocfilehash: ca68d2e46ce74593b66aac6f995b88ddcb79796b
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842489"
---
# <a name="shelluihelperissubscribed-method"></a><span data-ttu-id="3e1f9-103">ShellUIHelper. IsSubscribed 方法</span><span class="sxs-lookup"><span data-stu-id="3e1f9-103">ShellUIHelper.IsSubscribed method</span></span>

<span data-ttu-id="3e1f9-104">指出是否已訂閱指定的 URL。</span><span class="sxs-lookup"><span data-stu-id="3e1f9-104">Indicates whether a specified URL is subscribed to.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e1f9-105">語法</span><span class="sxs-lookup"><span data-stu-id="3e1f9-105">Syntax</span></span>


```JScript
bRetVal = ShellUIHelper.IsSubscribed(
  sURL
)
```



## <a name="parameters"></a><span data-ttu-id="3e1f9-106">參數</span><span class="sxs-lookup"><span data-stu-id="3e1f9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e1f9-107">*sURL* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3e1f9-107">*sURL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e1f9-108">類型： **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="3e1f9-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="3e1f9-109">指定 URL 的 **字串** 值。</span><span class="sxs-lookup"><span data-stu-id="3e1f9-109">A **String** value that specifies the URL.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e1f9-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="3e1f9-110">Return value</span></span>

<span data-ttu-id="3e1f9-111">類型：**布林 \* 值**</span><span class="sxs-lookup"><span data-stu-id="3e1f9-111">Type: **Boolean\***</span></span>

<span data-ttu-id="3e1f9-112">如果 URL 已訂閱，則為 **true** ;否則 **為 false**。</span><span class="sxs-lookup"><span data-stu-id="3e1f9-112">**true** if the URL is subscribed to; otherwise, **false**.</span></span>

## <a name="examples"></a><span data-ttu-id="3e1f9-113">範例</span><span class="sxs-lookup"><span data-stu-id="3e1f9-113">Examples</span></span>

<span data-ttu-id="3e1f9-114">下列範例會針對內嵌于 HTML 和 Visual Basic 中的 JScript，顯示此方法的適當用法。</span><span class="sxs-lookup"><span data-stu-id="3e1f9-114">The following example shows the proper usage of this method for JScript embedded in HTML and Visual Basic.</span></span>

<span data-ttu-id="3e1f9-115">Jscript：</span><span class="sxs-lookup"><span data-stu-id="3e1f9-115">JScript:</span></span>


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
    function fnShellUIHelperIsSubscribedJ()
    {
        var bReturn;
        
        bReturn = ShellUIHelper.IsSubscribed("https://www.microsoft.com/");
        alert(bReturn);
    }
</script>

</head>
<body onload=fnShellUIHelperIsSubscribedJ()>
</body>
</html>
```



<span data-ttu-id="3e1f9-116">Visual Basic：</span><span class="sxs-lookup"><span data-stu-id="3e1f9-116">Visual Basic:</span></span>


```VB
Private Sub fnShellUIHelperIsSubscribedVB()
    Dim objShellUIHelper As ShellUIHelper
    Dim bReturn          As Boolean
    
    Set objShellUIHelper = New ShellUIHelper
        bReturn = objShellUIHelper.IsSubscribed("https://www.microsoft.com/")
        Debug.Print bReturn
    Set objShellUIHelper = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="3e1f9-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="3e1f9-117">Requirements</span></span>



| <span data-ttu-id="3e1f9-118">需求</span><span class="sxs-lookup"><span data-stu-id="3e1f9-118">Requirement</span></span> | <span data-ttu-id="3e1f9-119">值</span><span class="sxs-lookup"><span data-stu-id="3e1f9-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e1f9-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3e1f9-120">Minimum supported client</span></span><br/> | <span data-ttu-id="3e1f9-121">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3e1f9-121">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="3e1f9-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3e1f9-122">Minimum supported server</span></span><br/> | <span data-ttu-id="3e1f9-123">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3e1f9-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="3e1f9-124">標頭</span><span class="sxs-lookup"><span data-stu-id="3e1f9-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="3e1f9-125"><dt>Exdisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="3e1f9-125"><dt>Exdisp.h</dt></span></span> </dl>                            |
| <span data-ttu-id="3e1f9-126">DLL</span><span class="sxs-lookup"><span data-stu-id="3e1f9-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3e1f9-127"><dt>Shell32.dll (4.71 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="3e1f9-127"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
