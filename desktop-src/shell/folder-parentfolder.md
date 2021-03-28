---
description: 包含父資料夾物件。
ms.assetid: b832948c-f599-4ada-8760-9280b86abfed
title: 'ParentFolder 屬性 (Shldisp. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder.ParentFolder
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 200d8f8c931bd81015f52226bed5a4e584951e20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103944194"
---
# <a name="folderparentfolder-property"></a><span data-ttu-id="9602f-103">ParentFolder 屬性</span><span class="sxs-lookup"><span data-stu-id="9602f-103">Folder.ParentFolder property</span></span>

<span data-ttu-id="9602f-104">包含父 [**資料夾**](folder.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="9602f-104">Contains the parent [**Folder**](folder.md) object.</span></span>

<span data-ttu-id="9602f-105">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="9602f-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="9602f-106">語法</span><span class="sxs-lookup"><span data-stu-id="9602f-106">Syntax</span></span>


```JScript
ParentFolder = Folder.ParentFolder
```



## <a name="property-value"></a><span data-ttu-id="9602f-107">屬性值</span><span class="sxs-lookup"><span data-stu-id="9602f-107">Property value</span></span>

<span data-ttu-id="9602f-108">ParentFolder 物件的物件參考。</span><span class="sxs-lookup"><span data-stu-id="9602f-108">An object reference to the ParentFolder object.</span></span>

## <a name="remarks"></a><span data-ttu-id="9602f-109">備註</span><span class="sxs-lookup"><span data-stu-id="9602f-109">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="9602f-110">並非所有的方法都會針對所有資料夾執行。</span><span class="sxs-lookup"><span data-stu-id="9602f-110">Not all methods are implemented for all folders.</span></span> <span data-ttu-id="9602f-111">例如， [**ParseName**](folder-parsename.md) 方法不會針對主控台資料夾執行， (CSIDL \_ 控制項) 。</span><span class="sxs-lookup"><span data-stu-id="9602f-111">For example, the [**ParseName**](folder-parsename.md) method is not implemented for the Control Panel folder (CSIDL\_CONTROLS).</span></span> <span data-ttu-id="9602f-112">如果您嘗試呼叫未產生的方法，則會引發 0x800A01BD (decimal 445) 錯誤。</span><span class="sxs-lookup"><span data-stu-id="9602f-112">If you attempt to call an unimplemented method, a 0x800A01BD (decimal 445) error is raised.</span></span>

 

## <a name="examples"></a><span data-ttu-id="9602f-113">範例</span><span class="sxs-lookup"><span data-stu-id="9602f-113">Examples</span></span>

<span data-ttu-id="9602f-114">下列範例示範如何適當地使用 JScript、VBScript 和 Visual Basic 的 **ParentFolder** 。</span><span class="sxs-lookup"><span data-stu-id="9602f-114">The following example shows the proper usage of **ParentFolder** for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="9602f-115">Jscript：</span><span class="sxs-lookup"><span data-stu-id="9602f-115">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFolderParentFolderJ()
    {
        var objShell    = new ActiveXObject("shell.application");
        var objFolder;
        var ssfPROGRAMS = 2;
        
        objFolder = objShell.NameSpace(ssfPROGRAMS);
        if (objFolder != null)
        {
            var objParentFolder;
                
            objParentFolder = objFolder.ParentFolder;
            if (objParentFolder != null)
            {
                alert(objParentFolder.Title);
            }
        }
    }
</script>
```



<span data-ttu-id="9602f-116">VBScript</span><span class="sxs-lookup"><span data-stu-id="9602f-116">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnFolderParentFolderVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        if (not objShell is nothing) then
            dim objFolder
            dim ssfPROGRAMS
            
            ssfPROGRAMS = 2
            set objFolder = objShell.NameSpace(ssfPROGRAMS)
            if (not objFolder is nothing) then
                dim objParentFolder
                        
                set objParentFolder = objFolder.ParentFolder
                if (not objParentFolder is nothing) then
                    alert(objParentFolder.Title)
                end if
                set objParentFolder = nothing
            end if
            set objFolder = nothing
        end if
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="9602f-117">Visual Basic：</span><span class="sxs-lookup"><span data-stu-id="9602f-117">Visual Basic:</span></span>


```VB
Private Sub fnFolderParentFolderVB()
    Dim objShell    As Shell
    Dim objFolder   As Folder
    Dim ssfPROGRAMS As Long
            
    ssfPROGRAMS = 2
    Set objShell = New Shell
    Set objFolder = objShell.NameSpace(ssfPROGRAMS)
    If (Not objFolder Is Nothing) Then
        Dim objParentFolder As Folder
                
        Set objParentFolder = objFolder.ParentFolder
        If (Not objParentFolder Is Nothing) Then
            Debug.Print objParentFolder.Title
        End If
        Set objParentFolder = Nothing
    End If
    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="9602f-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="9602f-118">Requirements</span></span>



| <span data-ttu-id="9602f-119">需求</span><span class="sxs-lookup"><span data-stu-id="9602f-119">Requirement</span></span> | <span data-ttu-id="9602f-120">值</span><span class="sxs-lookup"><span data-stu-id="9602f-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9602f-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9602f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="9602f-122">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9602f-122">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="9602f-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9602f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="9602f-124">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9602f-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="9602f-125">標頭</span><span class="sxs-lookup"><span data-stu-id="9602f-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="9602f-126"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="9602f-126"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="9602f-127">Idl</span><span class="sxs-lookup"><span data-stu-id="9602f-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9602f-128"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="9602f-128"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="9602f-129">DLL</span><span class="sxs-lookup"><span data-stu-id="9602f-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9602f-130"><dt>Shell32.dll (4.71 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="9602f-130"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




