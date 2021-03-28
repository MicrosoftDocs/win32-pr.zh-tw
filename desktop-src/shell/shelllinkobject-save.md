---
description: 儲存連結的所有變更。
ms.assetid: 4c776c82-8eca-4c9b-9487-4a835affd2d8
title: 'ShellLinkObject： Save 方法 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellLinkObject.Save
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 0283b839069464a1a059bd11ef52b522f7ec7072
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104991795"
---
# <a name="shelllinkobjectsave-method"></a><span data-ttu-id="9139b-103">ShellLinkObject。 Save 方法</span><span class="sxs-lookup"><span data-stu-id="9139b-103">ShellLinkObject.Save method</span></span>

<span data-ttu-id="9139b-104">儲存連結的所有變更。</span><span class="sxs-lookup"><span data-stu-id="9139b-104">Saves all changes to the link.</span></span>

## <a name="syntax"></a><span data-ttu-id="9139b-105">語法</span><span class="sxs-lookup"><span data-stu-id="9139b-105">Syntax</span></span>


```JScript
iRetVal = ShellLinkObject.Save(
  [ sFile ]
)
```



## <a name="parameters"></a><span data-ttu-id="9139b-106">參數</span><span class="sxs-lookup"><span data-stu-id="9139b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9139b-107">*sFile* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="9139b-107">*sFile* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9139b-108">類型： **Variant**</span><span class="sxs-lookup"><span data-stu-id="9139b-108">Type: **Variant**</span></span>

<span data-ttu-id="9139b-109">字串值，包含要儲存新連結資訊之檔案的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="9139b-109">A string value that contains the fully qualified path of the file where the new link information is to be saved.</span></span> <span data-ttu-id="9139b-110">如果未指定任何檔案，則會使用目前的檔案。</span><span class="sxs-lookup"><span data-stu-id="9139b-110">If no file is specified, the current file is used.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="9139b-111">範例</span><span class="sxs-lookup"><span data-stu-id="9139b-111">Examples</span></span>

<span data-ttu-id="9139b-112">下列範例會示範如何適當地使用此方法來進行 JScript、VBScript 和 Visual Basic。</span><span class="sxs-lookup"><span data-stu-id="9139b-112">The following example shows the proper usage of this method for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="9139b-113">Jscript：</span><span class="sxs-lookup"><span data-stu-id="9139b-113">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellLinkObjectSaveJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder;
        var ssfPROGRAMS = 2;
        
        objFolder = objShell.NameSpace(ssfPROGRAMS);
        if (objFolder != null)
        {
            var objFolderItem;
            
            objFolderItem = objFolder.ParseName("Internet Explorer.lnk");
            if (objFolderItem != null)
            {
                var objShellLink;
                
                objShellLink = objFolderItem.GetLink;
                if (objShellLink != null)
                {
                    // Making a change to the ShellLinkObject.
                    objShellLink.Description = "New Description";
                    
                    // Saving the changes.
                    objShellLink.Save();
                }
            }
        }
    }
</script>
```



<span data-ttu-id="9139b-114">VBScript</span><span class="sxs-lookup"><span data-stu-id="9139b-114">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellLinkObjectSaveVB()
        dim objShell
        dim objFolder
        dim ssfPROGRAMS
        
        ssfPROGRAMS = 2
        set objShell = CreateObject("shell.application")
        set objFolder = objShell.NameSpace(ssfPROGRAMS)
            if (not objFolder is nothing) then
                dim objFolderItem
                
                set objFolderItem = objFolder.ParseName("Internet Explorer.lnk")
                    if (not objFolderItem is nothing) then
                        dim objShellLink
                        
                        set objShellLink = objFolderItem.GetLink
                            if (not objShellLink is nothing) then
                                'Making a change to the ShellLinkObject.
                                objShellLink.Description = "New Description"
                                
                                'Saving the changes.
                                objShellLink.Save()
                            end if
                        set objShellLink = nothing
                    end if
                set objFolderItem = nothing
            end if
        set objFolder = nothing
        set objShell = nothing
    end function

 </script>
```



<span data-ttu-id="9139b-115">Visual Basic：</span><span class="sxs-lookup"><span data-stu-id="9139b-115">Visual Basic:</span></span>


```VB
Private Sub fnShellLinkObjectSaveVB()
    Dim objShell  As Shell
    Dim objFolder As Folder
    
    Set objShell = New Shell
    Set objFolder = objShell.NameSpace(ssfPROGRAMS)
        If (Not objFolder Is Nothing) Then
            Dim objFolderItem As FolderItem
            
            Set objFolderItem = objFolder.ParseName("Internet Explorer.lnk")
                If (Not objFolderItem Is Nothing) Then
                    Dim objShellLink As ShellLinkObject
                    
                    Set objShellLink = objFolderItem.GetLink
                        If (Not objShellLink Is Nothing) Then
                            'Making a change to the ShellLinkObject.
                            objShellLink.Description = "New Description"
                            'Saving the changes
                            objShellLink.Save
                        End If
                    Set objShellLink = Nothing
                End If
            Set objFolderItem = Nothing
        End If
    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="9139b-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="9139b-116">Requirements</span></span>



| <span data-ttu-id="9139b-117">需求</span><span class="sxs-lookup"><span data-stu-id="9139b-117">Requirement</span></span> | <span data-ttu-id="9139b-118">值</span><span class="sxs-lookup"><span data-stu-id="9139b-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9139b-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9139b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="9139b-120">僅限 Windows 2000 Professional 含 SP3 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9139b-120">Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="9139b-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9139b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="9139b-122">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9139b-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="9139b-123">標頭</span><span class="sxs-lookup"><span data-stu-id="9139b-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="9139b-124"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="9139b-124"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="9139b-125">Idl</span><span class="sxs-lookup"><span data-stu-id="9139b-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9139b-126"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="9139b-126"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="9139b-127">DLL</span><span class="sxs-lookup"><span data-stu-id="9139b-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9139b-128"><dt>Shell32.dll (5.0 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="9139b-128"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 




