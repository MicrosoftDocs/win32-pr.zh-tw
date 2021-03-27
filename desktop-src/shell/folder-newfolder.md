---
description: 建立新的資料夾。
ms.assetid: 7a552e5a-e9a3-4fcf-bc6b-17e8bc39af87
title: 'NewFolder 方法 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder.NewFolder
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 86784aa071be22cd16a06d9d4516970d2924079a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103944195"
---
# <a name="foldernewfolder-method"></a><span data-ttu-id="3b610-103">NewFolder 方法</span><span class="sxs-lookup"><span data-stu-id="3b610-103">Folder.NewFolder method</span></span>

<span data-ttu-id="3b610-104">建立新的資料夾。</span><span class="sxs-lookup"><span data-stu-id="3b610-104">Creates a new folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b610-105">語法</span><span class="sxs-lookup"><span data-stu-id="3b610-105">Syntax</span></span>


```JScript
Folder.NewFolder(
  bName,
  [ vOptions ]
)
```



## <a name="parameters"></a><span data-ttu-id="3b610-106">參數</span><span class="sxs-lookup"><span data-stu-id="3b610-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b610-107">*bName*</span><span class="sxs-lookup"><span data-stu-id="3b610-107">*bName*</span></span> 
</dt> <dd>

<span data-ttu-id="3b610-108">類型： **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="3b610-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="3b610-109">字串，指定新資料夾的名稱。</span><span class="sxs-lookup"><span data-stu-id="3b610-109">A string that specifies the name of the new folder.</span></span>

</dd> <dt>

<span data-ttu-id="3b610-110">*vOptions* \[選\]</span><span class="sxs-lookup"><span data-stu-id="3b610-110">*vOptions* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3b610-111">類型： **Variant**</span><span class="sxs-lookup"><span data-stu-id="3b610-111">Type: **Variant**</span></span>

<span data-ttu-id="3b610-112">目前不使用此值。</span><span class="sxs-lookup"><span data-stu-id="3b610-112">This value is not currently used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b610-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="3b610-113">Return value</span></span>

<span data-ttu-id="3b610-114">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="3b610-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3b610-115">備註</span><span class="sxs-lookup"><span data-stu-id="3b610-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="3b610-116">並非所有的方法都會針對所有資料夾執行。</span><span class="sxs-lookup"><span data-stu-id="3b610-116">Not all methods are implemented for all folders.</span></span> <span data-ttu-id="3b610-117">例如， [**ParseName**](folder-parsename.md) 方法不會針對主控台資料夾執行， (CSIDL \_ 控制項) 。</span><span class="sxs-lookup"><span data-stu-id="3b610-117">For example, the [**ParseName**](folder-parsename.md) method is not implemented for the Control Panel folder (CSIDL\_CONTROLS).</span></span> <span data-ttu-id="3b610-118">如果您嘗試呼叫未產生的方法，則會引發 0x800A01BD (decimal 445) 錯誤。</span><span class="sxs-lookup"><span data-stu-id="3b610-118">If you attempt to call an unimplemented method, a 0x800A01BD (decimal 445) error is raised.</span></span>

 

## <a name="examples"></a><span data-ttu-id="3b610-119">範例</span><span class="sxs-lookup"><span data-stu-id="3b610-119">Examples</span></span>

<span data-ttu-id="3b610-120">下列範例會使用 **NewFolder** 來建立新的資料夾 C： \\ >testfolder。</span><span class="sxs-lookup"><span data-stu-id="3b610-120">The following example uses **NewFolder** to create the new folder C:\\TestFolder.</span></span> <span data-ttu-id="3b610-121">JScript、VBScript 和 Visual Basic 會顯示適當的使用方式。</span><span class="sxs-lookup"><span data-stu-id="3b610-121">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="3b610-122">Jscript：</span><span class="sxs-lookup"><span data-stu-id="3b610-122">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFolderObjectNewFolderJ()
    {
        var objShell  = new ActiveXObject("shell.application");
        var objFolder = new Object;
        
        objFolder = objShell.NameSpace("C:\\");
        if (objFolder != null)
        {
            objFolder.NewFolder("TestFolder");
        }
    }
</script>
```



<span data-ttu-id="3b610-123">VBScript</span><span class="sxs-lookup"><span data-stu-id="3b610-123">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnFolderObjectNewFolderVB()
        dim objShell
        dim objFolder
        
        set objShell = CreateObject("shell.application")
        set objFolder = objShell.NameSpace("C:\")

        if (not objFolder is nothing) then
            objFolder.NewFolder("TestFolder")
        end if

        set objFolder = nothing
        set objShell = nothing
    end function
</script>
```



<span data-ttu-id="3b610-124">Visual Basic：</span><span class="sxs-lookup"><span data-stu-id="3b610-124">Visual Basic:</span></span>


```VB
Private Sub btnNewFolder_Click()
    Dim objShell  As Shell
    Dim objFolder As Folder

    Set objShell = New Shell
    Set objFolder = objShell.NameSpace("C:\")

    If (Not objFolder Is Nothing) Then
        objFolder.NewFolder ("TestFolder")
    End If

    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="3b610-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="3b610-125">Requirements</span></span>



| <span data-ttu-id="3b610-126">需求</span><span class="sxs-lookup"><span data-stu-id="3b610-126">Requirement</span></span> | <span data-ttu-id="3b610-127">值</span><span class="sxs-lookup"><span data-stu-id="3b610-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b610-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3b610-128">Minimum supported client</span></span><br/> | <span data-ttu-id="3b610-129">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3b610-129">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="3b610-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3b610-130">Minimum supported server</span></span><br/> | <span data-ttu-id="3b610-131">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3b610-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="3b610-132">標頭</span><span class="sxs-lookup"><span data-stu-id="3b610-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="3b610-133"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="3b610-133"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="3b610-134">Idl</span><span class="sxs-lookup"><span data-stu-id="3b610-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3b610-135"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="3b610-135"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="3b610-136">DLL</span><span class="sxs-lookup"><span data-stu-id="3b610-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3b610-137"><dt>Shell32.dll (4.71 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="3b610-137"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
