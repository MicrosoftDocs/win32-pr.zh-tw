---
description: 呼叫以回應使用者所關閉的 web view barricade。
ms.assetid: 170893b6-c947-45b1-b717-a93a0b083bda
title: 'Folder2. DismissedWebViewBarricade 方法 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder2.DismissedWebViewBarricade
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: cdedc7292b0dd52ca903b944993e32df1ec2c3b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115517"
---
# <a name="folder2dismissedwebviewbarricade-method"></a><span data-ttu-id="44a14-103">Folder2. DismissedWebViewBarricade 方法</span><span class="sxs-lookup"><span data-stu-id="44a14-103">Folder2.DismissedWebViewBarricade method</span></span>

<span data-ttu-id="44a14-104">呼叫以回應使用者所關閉的 web view barricade。</span><span class="sxs-lookup"><span data-stu-id="44a14-104">Called in response to the web view barricade being dismissed by the user.</span></span>

## <a name="syntax"></a><span data-ttu-id="44a14-105">語法</span><span class="sxs-lookup"><span data-stu-id="44a14-105">Syntax</span></span>


```JScript
Folder2.DismissedWebViewBarricade()
```



## <a name="parameters"></a><span data-ttu-id="44a14-106">參數</span><span class="sxs-lookup"><span data-stu-id="44a14-106">Parameters</span></span>

<span data-ttu-id="44a14-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="44a14-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="44a14-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="44a14-108">Return value</span></span>

<span data-ttu-id="44a14-109">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="44a14-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="44a14-110">備註</span><span class="sxs-lookup"><span data-stu-id="44a14-110">Remarks</span></span>

<span data-ttu-id="44a14-111">應用程式會在使用者關閉 web view barricade 之後呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="44a14-111">An application calls this method after the user dismisses the web view barricade.</span></span>

## <a name="examples"></a><span data-ttu-id="44a14-112">範例</span><span class="sxs-lookup"><span data-stu-id="44a14-112">Examples</span></span>

<span data-ttu-id="44a14-113">下列範例會使用 **DismissedWebViewBarricade** 指定 C： Windows 資料夾的 web view barricade \\ 已關閉。</span><span class="sxs-lookup"><span data-stu-id="44a14-113">The following example uses **DismissedWebViewBarricade** to specify that the web view barricade for the C:\\Windows folder has been dismissed.</span></span> <span data-ttu-id="44a14-114">JScript、VBScript 和 Visual Basic 會顯示適當的使用方式。</span><span class="sxs-lookup"><span data-stu-id="44a14-114">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="44a14-115">Jscript：</span><span class="sxs-lookup"><span data-stu-id="44a14-115">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFolder2ObjectDismissedWebViewBarricadeJ()
    {
        var objShell  = new ActiveXObject("shell.application");
        var objFolder2 = new Object;
        
        objFolder2 = objShell.NameSpace("C:\\WINDOWS");
        if (objFolder2 != null)
        {
            objFolder2.DismissedWebViewBarricade();
        }
    }
</script>
```



<span data-ttu-id="44a14-116">VBScript</span><span class="sxs-lookup"><span data-stu-id="44a14-116">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnFolder2ObjectDismissedWebViewBarricadeVB()
        dim objShell
        dim objFolder2

        set objShell = CreateObject("shell.application")
        set objFolder2 = objShell.NameSpace("C:\WINDOWS")

        if (not objFolder2 is nothing) then
            objFolder2.DismissedWebViewBarricade()
        end if

        set objFolder2 = nothing
        set objShell = nothing
    end function
</script>
```



<span data-ttu-id="44a14-117">Visual Basic：</span><span class="sxs-lookup"><span data-stu-id="44a14-117">Visual Basic:</span></span>


```VB
Private Sub btnDismissedWebViewBarricade_Click()
    Dim objShell   As Shell
    Dim objFolder2 As Folder2

    Set objShell = New Shell
    Set objFolder2 = objShell.NameSpace("C:\WINDOWS")

    If (Not objFolder2 Is Nothing) Then
        objFolder2.DismissedWebViewBarricade
    End If

    Set objFolder2 = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="44a14-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="44a14-118">Requirements</span></span>



| <span data-ttu-id="44a14-119">需求</span><span class="sxs-lookup"><span data-stu-id="44a14-119">Requirement</span></span> | <span data-ttu-id="44a14-120">值</span><span class="sxs-lookup"><span data-stu-id="44a14-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="44a14-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="44a14-121">Minimum supported client</span></span><br/> | <span data-ttu-id="44a14-122">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="44a14-122">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="44a14-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="44a14-123">Minimum supported server</span></span><br/> | <span data-ttu-id="44a14-124">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="44a14-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="44a14-125">標頭</span><span class="sxs-lookup"><span data-stu-id="44a14-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="44a14-126"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="44a14-126"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="44a14-127">Idl</span><span class="sxs-lookup"><span data-stu-id="44a14-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="44a14-128"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="44a14-128"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="44a14-129">DLL</span><span class="sxs-lookup"><span data-stu-id="44a14-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="44a14-130"><dt>Shell32.dll (5.0 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="44a14-130"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44a14-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="44a14-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44a14-132">**Folder2**</span><span class="sxs-lookup"><span data-stu-id="44a14-132">**Folder2**</span></span>](folder2-object.md)
</dt> <dt>

[<span data-ttu-id="44a14-133">**資料夾**</span><span class="sxs-lookup"><span data-stu-id="44a14-133">**Folder**</span></span>](folder.md)
</dt> </dl>

 

 




