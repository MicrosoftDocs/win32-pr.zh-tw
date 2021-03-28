---
description: 包含資料夾的 FolderItem 物件。
ms.assetid: 0964505d-4138-4444-91d4-46c707c45688
title: 'Folder2： Self 屬性 (Shldisp) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder2.Self
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: f49666096f35f9871f8a3b3c141d4bc169dea0c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191046"
---
# <a name="folder2self-property"></a><span data-ttu-id="59e56-103">Folder2。 Self 屬性</span><span class="sxs-lookup"><span data-stu-id="59e56-103">Folder2.Self property</span></span>

<span data-ttu-id="59e56-104">包含資料夾的 [**FolderItem**](folderitem.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="59e56-104">Contains the folder's [**FolderItem**](folderitem.md) object.</span></span>

<span data-ttu-id="59e56-105">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="59e56-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="59e56-106">語法</span><span class="sxs-lookup"><span data-stu-id="59e56-106">Syntax</span></span>


```JScript
Self = Folder2.Self
```



## <a name="property-value"></a><span data-ttu-id="59e56-107">屬性值</span><span class="sxs-lookup"><span data-stu-id="59e56-107">Property value</span></span>

<span data-ttu-id="59e56-108">評估為資料夾 [**FolderItem**](folderitem.md) 物件的物件。</span><span class="sxs-lookup"><span data-stu-id="59e56-108">The object that evaluates to the folder's [**FolderItem**](folderitem.md) object.</span></span>

## <a name="examples"></a><span data-ttu-id="59e56-109">範例</span><span class="sxs-lookup"><span data-stu-id="59e56-109">Examples</span></span>

<span data-ttu-id="59e56-110">下列範例會使用 **Self** 來取得 C [](folderitem.md) ： Windows 資料夾的 FolderItem \\ 。</span><span class="sxs-lookup"><span data-stu-id="59e56-110">The following example uses **Self** to retrieve the [**FolderItem**](folderitem.md) for the C:\\Windows folder.</span></span> <span data-ttu-id="59e56-111">JScript、VBScript 和 Visual Basic 會顯示適當的使用方式。</span><span class="sxs-lookup"><span data-stu-id="59e56-111">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="59e56-112">Jscript：</span><span class="sxs-lookup"><span data-stu-id="59e56-112">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFolder2ObjectSelfJ()
    {
        var objShell  = new ActiveXObject("shell.application");
        var objFolder2 = new Object;
        
        objFolder2 = objShell.NameSpace("C:\\WINDOWS");
        if (objFolder2 != null)
        {
            var objFolderItem = new Object;
            
            objFolderItem = objFolder2.Self;
            if (objFolderItem != null)
            {
                //Add code here.
            }
        }
    }
</script>
```



<span data-ttu-id="59e56-113">VBScript</span><span class="sxs-lookup"><span data-stu-id="59e56-113">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnFolder2ObjectSelfVB()
        dim objShell
        dim objFolder2

        set objShell = CreateObject("shell.application")
        set objFolder2 = objShell.NameSpace("C:\WINDOWS")

        if (not objFolder2 is nothing) then
            dim objFolderItem
            
            set objFolderItem = objFolder2.Self

            if (not objFolderItem is nothing) then
                'Add code here.
            end if
        end if

        set objFolder2 = nothing
        set objShell = nothing
    end function
</script>
```



<span data-ttu-id="59e56-114">Visual Basic：</span><span class="sxs-lookup"><span data-stu-id="59e56-114">Visual Basic:</span></span>


```VB
Private Sub btnFolder2Self_Click()
    Dim objShell   As Shell
    Dim objFolder2 As Folder2

    Set objShell = New Shell
    Set objFolder2 = objShell.NameSpace("C:\WINDOWS")

    If (Not objFolder2 Is Nothing) Then
        Dim objFolderItem As FolderItem
        
        Set objFolderItem = objFolder2.Self()

        If (Not objFolderItem Is Nothing) Then
            'Add code here.
        End If

        Set objFolderItem = Nothing
    End If

    Set objFolder2 = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="59e56-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="59e56-115">Requirements</span></span>



| <span data-ttu-id="59e56-116">需求</span><span class="sxs-lookup"><span data-stu-id="59e56-116">Requirement</span></span> | <span data-ttu-id="59e56-117">值</span><span class="sxs-lookup"><span data-stu-id="59e56-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59e56-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="59e56-118">Minimum supported client</span></span><br/> | <span data-ttu-id="59e56-119">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="59e56-119">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="59e56-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="59e56-120">Minimum supported server</span></span><br/> | <span data-ttu-id="59e56-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="59e56-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="59e56-122">標頭</span><span class="sxs-lookup"><span data-stu-id="59e56-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="59e56-123"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="59e56-123"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="59e56-124">Idl</span><span class="sxs-lookup"><span data-stu-id="59e56-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="59e56-125"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="59e56-125"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="59e56-126">DLL</span><span class="sxs-lookup"><span data-stu-id="59e56-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="59e56-127"><dt>Shell32.dll (5.0 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="59e56-127"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59e56-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="59e56-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59e56-129">**Folder2**</span><span class="sxs-lookup"><span data-stu-id="59e56-129">**Folder2**</span></span>](folder2-object.md)
</dt> <dt>

[<span data-ttu-id="59e56-130">**資料夾**</span><span class="sxs-lookup"><span data-stu-id="59e56-130">**Folder**</span></span>](folder.md)
</dt> </dl>

 

 




