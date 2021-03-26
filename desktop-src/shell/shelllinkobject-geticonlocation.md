---
description: 取得指派給連結的圖示位置。
ms.assetid: 3bb7f0f0-7ab9-41e6-b738-274efbcd52ab
title: 'ShellLinkObject. GetIconLocation 方法 (Shlobj.h \_ core .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellLinkObject.GetIconLocation
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: ef2f502d30116def68aa43269b3020d404ce177d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193949"
---
# <a name="shelllinkobjectgeticonlocation-method"></a><span data-ttu-id="f1346-103">ShellLinkObject. GetIconLocation 方法</span><span class="sxs-lookup"><span data-stu-id="f1346-103">ShellLinkObject.GetIconLocation method</span></span>

<span data-ttu-id="f1346-104">取得指派給連結的圖示位置。</span><span class="sxs-lookup"><span data-stu-id="f1346-104">Gets the location of the icon assigned to the link.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1346-105">語法</span><span class="sxs-lookup"><span data-stu-id="f1346-105">Syntax</span></span>


```JScript
iRetVal = ShellLinkObject.GetIconLocation(
  sPath
)
```



## <a name="parameters"></a><span data-ttu-id="f1346-106">參數</span><span class="sxs-lookup"><span data-stu-id="f1346-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1346-107">*sPath* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="f1346-107">*sPath* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f1346-108">類型： \**[**BSTR**](/previous-versions/windows/desktop/automat/bstr) \** _</span><span class="sxs-lookup"><span data-stu-id="f1346-108">Type: \**[**BSTR**](/previous-versions/windows/desktop/automat/bstr)\** _</span></span>

<span data-ttu-id="f1346-109">當此方法傳回時，它會保存包含圖示之檔案的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="f1346-109">When this method returns, it holds the fully qualified path of the file that contains the icon.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1346-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="f1346-110">Return value</span></span>

<span data-ttu-id="f1346-111">類型： _*整數 \**_</span><span class="sxs-lookup"><span data-stu-id="f1346-111">Type: _*Integer\**_</span></span>

<span data-ttu-id="f1346-112">傳回 _sPath \* 所指定檔案中的圖示索引。</span><span class="sxs-lookup"><span data-stu-id="f1346-112">Returns the icon's index in the file specified by _sPath\*.</span></span>

## <a name="examples"></a><span data-ttu-id="f1346-113">範例</span><span class="sxs-lookup"><span data-stu-id="f1346-113">Examples</span></span>

<span data-ttu-id="f1346-114">下列範例會示範如何適當地使用此方法來進行 JScript、VBScript 和 Visual Basic。</span><span class="sxs-lookup"><span data-stu-id="f1346-114">The following example shows the proper usage of this method for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="f1346-115">Jscript：</span><span class="sxs-lookup"><span data-stu-id="f1346-115">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellShellLinkObjectGetIconLocationJ()
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
                    var nIcon;
                    
                    nIcon = objShellLink.GetIconLocation(objFolderItem.Path);
                    alert(nIcon);
                }
            }
        }
    }
</script>
```



<span data-ttu-id="f1346-116">VBScript</span><span class="sxs-lookup"><span data-stu-id="f1346-116">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellLinkObjectGetIconLocationVB()
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
                                dim nIcon
                                
                                nIcon = objShellLink.GetIconLocation(objFolderItem.Path)
                                alert(nIcon)
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



<span data-ttu-id="f1346-117">Visual Basic：</span><span class="sxs-lookup"><span data-stu-id="f1346-117">Visual Basic:</span></span>


```VB
Private Sub fnShellLinkObjectGetIconLocationVB()
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
                            Dim nIcon As Integer
                            
                            nIcon = objShellLink.GetIconLocation(objFolderItem.Path)
                            Debug.Print nIcon
                        End If
                    Set objShellLink = Nothing
                End If
            Set objFolderItem = Nothing
        End If
    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="f1346-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="f1346-118">Requirements</span></span>



| <span data-ttu-id="f1346-119">需求</span><span class="sxs-lookup"><span data-stu-id="f1346-119">Requirement</span></span> | <span data-ttu-id="f1346-120">值</span><span class="sxs-lookup"><span data-stu-id="f1346-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1346-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f1346-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f1346-122">僅限 Windows 2000 Professional 含 SP3 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f1346-122">Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="f1346-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f1346-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f1346-124">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f1346-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="f1346-125">標頭</span><span class="sxs-lookup"><span data-stu-id="f1346-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="f1346-126"><dt>Shlobj.h \_ core .h (包括 Shldisp) </dt></span><span class="sxs-lookup"><span data-stu-id="f1346-126"><dt>Shlobj\_core.h (include Shldisp.h)</dt></span></span> </dl> |
| <span data-ttu-id="f1346-127">Idl</span><span class="sxs-lookup"><span data-stu-id="f1346-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f1346-128"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="f1346-128"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="f1346-129">DLL</span><span class="sxs-lookup"><span data-stu-id="f1346-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f1346-130"><dt>Shell32.dll (5.0 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="f1346-130"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1346-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f1346-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1346-132">**ShellLinkObject**</span><span class="sxs-lookup"><span data-stu-id="f1346-132">**ShellLinkObject**</span></span>](shelllinkobject-object.md)
</dt> <dt>

[<span data-ttu-id="f1346-133">**SetIconLocation**</span><span class="sxs-lookup"><span data-stu-id="f1346-133">**SetIconLocation**</span></span>](shelllinkobject-seticonlocation.md)
</dt> </dl>

 

 
