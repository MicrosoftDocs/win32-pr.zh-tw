---
description: 取得或設定連結的鍵盤快速鍵。
ms.assetid: edc65fe8-c7f3-46d0-86ca-1c0c93e7ca64
title: 'ShellLinkObject 快速鍵屬性 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellLinkObject.Hotkey
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 23ab8615421eee7289e5f0bb58582bf8e0d48f17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973669"
---
# <a name="shelllinkobjecthotkey-property"></a><span data-ttu-id="3015d-103">ShellLinkObject 熱鍵屬性</span><span class="sxs-lookup"><span data-stu-id="3015d-103">ShellLinkObject.Hotkey property</span></span>

<span data-ttu-id="3015d-104">取得或設定連結的鍵盤快速鍵。</span><span class="sxs-lookup"><span data-stu-id="3015d-104">Gets or sets the keyboard shortcut for the link.</span></span>

<span data-ttu-id="3015d-105">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="3015d-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="3015d-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="3015d-106">Syntax</span></span>


```JScript
iHotkey = ShellLinkObject.Hotkey
ShellLinkObject.Hotkey(iHotkey) = iHotkey
```



## <a name="property-value"></a><span data-ttu-id="3015d-107">屬性值</span><span class="sxs-lookup"><span data-stu-id="3015d-107">Property value</span></span>

<span data-ttu-id="3015d-108">連結的鍵盤快速鍵。</span><span class="sxs-lookup"><span data-stu-id="3015d-108">the link's keyboard shortcut.</span></span> <span data-ttu-id="3015d-109">虛擬鍵盤快速鍵是在低序位位元組中，而修飾詞旗標則是在高序位位元組中。</span><span class="sxs-lookup"><span data-stu-id="3015d-109">The virtual keyboard shortcut is in the low-order byte, and the modifier flags are in the high-order byte.</span></span> <span data-ttu-id="3015d-110">修飾詞旗標可以是下列值的組合。</span><span class="sxs-lookup"><span data-stu-id="3015d-110">The modifier flags can be a combination of the following values.</span></span>

<dt>



 <span data-ttu-id="3015d-111">(1)</span><span class="sxs-lookup"><span data-stu-id="3015d-111">(1)</span></span>


</dt> <dd>

<span data-ttu-id="3015d-112">SHIFT 鍵</span><span class="sxs-lookup"><span data-stu-id="3015d-112">SHIFT key</span></span>

</dd> <dt>



 <span data-ttu-id="3015d-113">(2)</span><span class="sxs-lookup"><span data-stu-id="3015d-113">(2)</span></span>


</dt> <dd>

<span data-ttu-id="3015d-114">CTRL 鍵</span><span class="sxs-lookup"><span data-stu-id="3015d-114">CTRL key</span></span>

</dd> <dt>



 <span data-ttu-id="3015d-115">(4)</span><span class="sxs-lookup"><span data-stu-id="3015d-115">(4)</span></span>


</dt> <dd>

<span data-ttu-id="3015d-116">ALT 鍵</span><span class="sxs-lookup"><span data-stu-id="3015d-116">ALT key</span></span>

</dd> <dt>



 <span data-ttu-id="3015d-117">(8)</span><span class="sxs-lookup"><span data-stu-id="3015d-117">(8)</span></span>


</dt> <dd>

<span data-ttu-id="3015d-118">擴充金鑰</span><span class="sxs-lookup"><span data-stu-id="3015d-118">Extended key</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="3015d-119">範例</span><span class="sxs-lookup"><span data-stu-id="3015d-119">Examples</span></span>

<span data-ttu-id="3015d-120">下列範例示範如何在 JScript、VBScript 和 Visual Basic 中正確使用此屬性。</span><span class="sxs-lookup"><span data-stu-id="3015d-120">The following example shows the proper usage of this property in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="3015d-121">Jscript：</span><span class="sxs-lookup"><span data-stu-id="3015d-121">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellShellLinkObjectHotkeyJ()
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
                    var nHotkey;
                    
                    // Get the keyboard shortcut for the ShellLinkObject.
                    nHotkey = objShellLink.Hotkey;
                    alert(nHotkey);
                    
                    // Set the keyboard shortcut for the ShellLinkObject.
                    objShellLink.Hotkey = 4;
                }
            }
        }
    }
</script>
```



<span data-ttu-id="3015d-122">VBScript</span><span class="sxs-lookup"><span data-stu-id="3015d-122">VBScript:</span></span>


```VB
<script language="VBScript">
     function fnShellLinkObjectHotkeyVB()
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
                                dim nHotkey
                                
                                'Get the keyboard shortcut for the ShellLinkObject.
                                nHotkey = objShellLink.Hotkey
                                alert(nHotkey)
                                
                                'Set the keyboard shortcut for the ShellLinkObject.
                                objShellLink.Hotkey = 4
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



<span data-ttu-id="3015d-123">Visual Basic：</span><span class="sxs-lookup"><span data-stu-id="3015d-123">Visual Basic:</span></span>


```VB
Private Sub fnShellLinkObjectHotkeyVB()
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
                            Dim nHotkey As Integer
                            
                            'Get the keyboard shortcut for the ShellLinkObject.
                            nHotkey = objShellLink.Hotkey
                            Debug.Print nHotkey
                            
                            'Set the keyboard shortcut for the ShellLinkObject.
                            objShellLink.Hotkey = 4
                        End If
                    Set objShellLink = Nothing
                End If
            Set objFolderItem = Nothing
        End If
    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="3015d-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="3015d-124">Requirements</span></span>



| <span data-ttu-id="3015d-125">需求</span><span class="sxs-lookup"><span data-stu-id="3015d-125">Requirement</span></span> | <span data-ttu-id="3015d-126">值</span><span class="sxs-lookup"><span data-stu-id="3015d-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3015d-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3015d-127">Minimum supported client</span></span><br/> | <span data-ttu-id="3015d-128">僅限 Windows 2000 Professional 含 SP3 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3015d-128">Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="3015d-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3015d-129">Minimum supported server</span></span><br/> | <span data-ttu-id="3015d-130">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3015d-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="3015d-131">標頭</span><span class="sxs-lookup"><span data-stu-id="3015d-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="3015d-132"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="3015d-132"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="3015d-133">Idl</span><span class="sxs-lookup"><span data-stu-id="3015d-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3015d-134"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="3015d-134"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="3015d-135">DLL</span><span class="sxs-lookup"><span data-stu-id="3015d-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3015d-136"><dt>Shell32.dll (5.0 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="3015d-136"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 




