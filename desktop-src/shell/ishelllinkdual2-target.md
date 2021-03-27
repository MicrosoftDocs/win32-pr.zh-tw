---
description: 包含連結化物件的目標。
ms.assetid: 26da562b-a1d6-4150-9d9a-05b11e3972d9
title: 'IShellLinkDual2： Target 屬性 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellLinkDual2.Target
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 8e5f29623cf94ef5f17f06e52337928c0c345e42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972325"
---
# <a name="ishelllinkdual2target-property"></a><span data-ttu-id="48ef7-103">IShellLinkDual2。目標屬性</span><span class="sxs-lookup"><span data-stu-id="48ef7-103">IShellLinkDual2.Target property</span></span>

<span data-ttu-id="48ef7-104">包含連結化物件的目標。</span><span class="sxs-lookup"><span data-stu-id="48ef7-104">Contains the link object's target.</span></span>

<span data-ttu-id="48ef7-105">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="48ef7-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="48ef7-106">語法</span><span class="sxs-lookup"><span data-stu-id="48ef7-106">Syntax</span></span>


```JScript
Target = IShellLinkDual2.Target
```



## <a name="property-value"></a><span data-ttu-id="48ef7-107">屬性值</span><span class="sxs-lookup"><span data-stu-id="48ef7-107">Property value</span></span>

<span data-ttu-id="48ef7-108">評估為目標 [**FolderItem**](folderitem.md) 物件的物件運算式。</span><span class="sxs-lookup"><span data-stu-id="48ef7-108">An object expression that evaluates to the target's [**FolderItem**](folderitem.md) object.</span></span>

## <a name="examples"></a><span data-ttu-id="48ef7-109">範例</span><span class="sxs-lookup"><span data-stu-id="48ef7-109">Examples</span></span>

<span data-ttu-id="48ef7-110">下列範例會使用 **target** 來取得 Internet Explorer 之快捷方式的目標。</span><span class="sxs-lookup"><span data-stu-id="48ef7-110">The following example uses **Target** to retrieve the target of a shortcut to Internet Explorer.</span></span> <span data-ttu-id="48ef7-111">JScript、VBScript 和 Visual Basic 會顯示適當的使用方式。</span><span class="sxs-lookup"><span data-stu-id="48ef7-111">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="48ef7-112">Jscript：</span><span class="sxs-lookup"><span data-stu-id="48ef7-112">JScript:</span></span>


```JScript
<script language="JScript">
    function fnIShellLinkDual2TargetJ()
    {
        var objShell    = new ActiveXObject("shell.application");
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
                    var objTargetItem;
                            
                    objTargetItem = objShellLink.Target;
                    if (objTargetItem != null)
                    {
                        // Add code here.
                    }
                }
            }
        }
    }
</script>
```



<span data-ttu-id="48ef7-113">VBScript</span><span class="sxs-lookup"><span data-stu-id="48ef7-113">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnIShellLinkDual2TargetVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        if (not objShell is nothing) then
            dim objFolder
            dim ssfPROGRAMS
            
            ssfPROGRAMS = 2
            set objFolder = objShell.NameSpace(ssfPROGRAMS)
            if (not objFolder is nothing) then
                dim objFolderItem
                        
                set objFolderItem = objFolder.ParseName("Internet Explorer.lnk")
                if (not objFolderItem is nothing) then
                    dim objShellLink
                    
                    set objShellLink = objFolderItem.GetLink
                        if (not objShellLink is nothing) then
                            dim objTargetItem
                            
                            set objTargetItem = objShellLink.Target
                                if (not objTargetItem is nothing) then
                                    'Add code here.
                                end if
                            set objTargetItem = nothing
                        end if
                    set objShellLink = nothing
                end if
                set objFolderItem = nothing
            end if
            set objFolder = nothing
        end if
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="48ef7-114">Visual Basic：</span><span class="sxs-lookup"><span data-stu-id="48ef7-114">Visual Basic:</span></span>


```VB
Private Sub fnIShellLinkDual2TargetVB()
    Dim objShell   As Shell
    Dim objFolder  As Folder
    Dim ssfPROGRAMS
            
    ssfPROGRAMS = 2
    Set objShell = New Shell
    Set objFolder = objShell.NameSpace(ssfPROGRAMS)
    If (Not objFolder Is Nothing) Then
        Dim objFolderItem As FolderItem
                
        Set objFolderItem = objFolder.ParseName("Internet Explorer.lnk")
        If (Not objFolderItem Is Nothing) Then
            Dim objShellLink As ShellLinkObject
            
            Set objShellLink = objFolderItem.GetLink
                If (Not objShellLink Is Nothing) Then
                    Dim objTargetItem As FolderItem
                    
                    Set objTargetItem = objShellLink.Target
                        If (Not objTargetItem Is Nothing) Then
                            'Add code here
                        End If
                    Set objTargetItem = Nothing
                End If
            Set objShellLink = Nothing
        End If
        Set objFolderItem = Nothing
    End If
    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="48ef7-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="48ef7-115">Requirements</span></span>



| <span data-ttu-id="48ef7-116">需求</span><span class="sxs-lookup"><span data-stu-id="48ef7-116">Requirement</span></span> | <span data-ttu-id="48ef7-117">值</span><span class="sxs-lookup"><span data-stu-id="48ef7-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="48ef7-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="48ef7-118">Minimum supported client</span></span><br/> | <span data-ttu-id="48ef7-119">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="48ef7-119">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="48ef7-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="48ef7-120">Minimum supported server</span></span><br/> | <span data-ttu-id="48ef7-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="48ef7-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="48ef7-122">標頭</span><span class="sxs-lookup"><span data-stu-id="48ef7-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="48ef7-123"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="48ef7-123"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="48ef7-124">Idl</span><span class="sxs-lookup"><span data-stu-id="48ef7-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="48ef7-125"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="48ef7-125"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="48ef7-126">DLL</span><span class="sxs-lookup"><span data-stu-id="48ef7-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="48ef7-127"><dt>Shell32.dll (5.0 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="48ef7-127"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48ef7-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="48ef7-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48ef7-129">**IShellLinkDual2**</span><span class="sxs-lookup"><span data-stu-id="48ef7-129">**IShellLinkDual2**</span></span>](ishelllinkdual2-object.md)
</dt> <dt>

[<span data-ttu-id="48ef7-130">**ShellLinkObject**</span><span class="sxs-lookup"><span data-stu-id="48ef7-130">**ShellLinkObject**</span></span>](shelllinkobject-object.md)
</dt> </dl>

 

 




