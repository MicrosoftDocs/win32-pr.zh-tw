---
description: 建立並傳回指定資料夾的資料夾物件。
ms.assetid: c0d61bc6-6851-4b47-a62d-4c24d2958b98
title: 'Shell. NameSpace 方法 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.NameSpace
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 856a86efb4aca6ae7c1d4c8a3a81b5bc722a3963
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192809"
---
# <a name="shellnamespace-method"></a><span data-ttu-id="24119-103">Shell. NameSpace 方法</span><span class="sxs-lookup"><span data-stu-id="24119-103">Shell.NameSpace method</span></span>

<span data-ttu-id="24119-104">建立並傳回指定資料夾的 [**資料夾**](folder.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="24119-104">Creates and returns a [**Folder**](folder.md) object for the specified folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="24119-105">語法</span><span class="sxs-lookup"><span data-stu-id="24119-105">Syntax</span></span>


```JScript
retVal = Shell.NameSpace(
  vDir
)
```


```VB

Shell.NameSpace( _
  ByVal vDir As Variant _
) As Folder
```





## <a name="parameters"></a><span data-ttu-id="24119-106">參數</span><span class="sxs-lookup"><span data-stu-id="24119-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24119-107">*vDir* \[在\]</span><span class="sxs-lookup"><span data-stu-id="24119-107">*vDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24119-108">類型： **Variant**</span><span class="sxs-lookup"><span data-stu-id="24119-108">Type: **Variant**</span></span>

<span data-ttu-id="24119-109">要建立 [**資料夾**](folder.md) 物件的資料夾。</span><span class="sxs-lookup"><span data-stu-id="24119-109">The folder for which to create the [**Folder**](folder.md) object.</span></span> <span data-ttu-id="24119-110">這可以是指定資料夾路徑或其中一個 [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) 值的字串。</span><span class="sxs-lookup"><span data-stu-id="24119-110">This can be a string that specifies the path of the folder or one of the [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) values.</span></span> <span data-ttu-id="24119-111">請注意，在 **ShellSpecialFolderConstants** 中找到的常數名稱可以在 Visual Basic 中使用，但不能在 VBScript 或 JScript 中使用。</span><span class="sxs-lookup"><span data-stu-id="24119-111">Note that the constant names found in **ShellSpecialFolderConstants** are available in Visual Basic, but not in VBScript or JScript.</span></span> <span data-ttu-id="24119-112">在這些情況下，必須在其位置使用數值。</span><span class="sxs-lookup"><span data-stu-id="24119-112">In those cases, the numeric values must be used in their place.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="24119-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="24119-113">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="24119-114">JScript</span><span class="sxs-lookup"><span data-stu-id="24119-114">JScript</span></span>

<span data-ttu-id="24119-115">類型： **[**資料夾**](folder.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="24119-115">Type: **[**Folder**](folder.md)\*\***</span></span>

<span data-ttu-id="24119-116">指定資料夾之 [**資料夾**](folder.md) 物件的物件參考。</span><span class="sxs-lookup"><span data-stu-id="24119-116">Object reference to the [**Folder**](folder.md) object for the specified folder.</span></span> <span data-ttu-id="24119-117">如果未成功建立資料夾，此值會傳回 **null**。</span><span class="sxs-lookup"><span data-stu-id="24119-117">If the folder is not successfully created, this value returns **null**.</span></span>

### <a name="vb"></a><span data-ttu-id="24119-118">VB</span><span class="sxs-lookup"><span data-stu-id="24119-118">VB</span></span>

<span data-ttu-id="24119-119">類型： **[**資料夾**](folder.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="24119-119">Type: **[**Folder**](folder.md)\*\***</span></span>

<span data-ttu-id="24119-120">指定資料夾之 [**資料夾**](folder.md) 物件的物件參考。</span><span class="sxs-lookup"><span data-stu-id="24119-120">Object reference to the [**Folder**](folder.md) object for the specified folder.</span></span> <span data-ttu-id="24119-121">如果未成功建立資料夾，此值會傳回 **null**。</span><span class="sxs-lookup"><span data-stu-id="24119-121">If the folder is not successfully created, this value returns **null**.</span></span>

## <a name="examples"></a><span data-ttu-id="24119-122">範例</span><span class="sxs-lookup"><span data-stu-id="24119-122">Examples</span></span>

<span data-ttu-id="24119-123">下列範例顯示使用中的 **命名空間** 。</span><span class="sxs-lookup"><span data-stu-id="24119-123">The following example shows **NameSpace** in use.</span></span> <span data-ttu-id="24119-124">JScript、VBScript 和 Visual Basic 會顯示適當的使用方式。</span><span class="sxs-lookup"><span data-stu-id="24119-124">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="24119-125">Jscript：</span><span class="sxs-lookup"><span data-stu-id="24119-125">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellNameSpaceJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder;
        var ssfWINDOWS = 36
        
        objFolder = objShell.NameSpace(ssfWINDOWS);
        if (objFolder != null)
        {
            alert(objFolder.Title);
        }
    }
</script>
```



<span data-ttu-id="24119-126">VBScript</span><span class="sxs-lookup"><span data-stu-id="24119-126">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellNameSpaceVB()
        dim objShell
        dim objFolder
        
        set objShell = CreateObject("shell.application")
        set objFolder = objShell.NameSpace("C:\\")

        if (not objFolder is nothing) then
            alert(objFolder.Title)
        end if

        set objFolder = nothing
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="24119-127">Visual Basic：</span><span class="sxs-lookup"><span data-stu-id="24119-127">Visual Basic:</span></span>


```VB
Private Sub fnShellNameSpaceVB()
    Dim objShell  As Shell
    Dim objFolder As Folder

    Set objShell = New Shell
    Set objFolder = objShell.NameSpace(ssfPERSONAL)

    If (Not objFolder Is Nothing) Then
        Debug.Print objFolder.Title
    End If

    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="24119-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="24119-128">Requirements</span></span>



| <span data-ttu-id="24119-129">需求</span><span class="sxs-lookup"><span data-stu-id="24119-129">Requirement</span></span> | <span data-ttu-id="24119-130">值</span><span class="sxs-lookup"><span data-stu-id="24119-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="24119-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="24119-131">Minimum supported client</span></span><br/> | <span data-ttu-id="24119-132">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="24119-132">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="24119-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="24119-133">Minimum supported server</span></span><br/> | <span data-ttu-id="24119-134">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="24119-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="24119-135">標頭</span><span class="sxs-lookup"><span data-stu-id="24119-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="24119-136"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="24119-136"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="24119-137">Idl</span><span class="sxs-lookup"><span data-stu-id="24119-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="24119-138"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="24119-138"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="24119-139">DLL</span><span class="sxs-lookup"><span data-stu-id="24119-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="24119-140"><dt>Shell32.dll (4.71 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="24119-140"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




