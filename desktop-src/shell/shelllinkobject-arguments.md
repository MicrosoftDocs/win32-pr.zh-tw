---
description: 包含連結的引數。
ms.assetid: 938db958-4b59-4dd6-ac56-f21db05ec989
title: 'ShellLinkObject 引數屬性 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellLinkObject.Arguments
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: c9b8a32eb4b935b5164ef91bf299777b36d7e53d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194431"
---
# <a name="shelllinkobjectarguments-property"></a><span data-ttu-id="cd272-103">ShellLinkObject. Arguments 屬性</span><span class="sxs-lookup"><span data-stu-id="cd272-103">ShellLinkObject.Arguments property</span></span>

<span data-ttu-id="cd272-104">包含連結的引數。</span><span class="sxs-lookup"><span data-stu-id="cd272-104">Contains a link's arguments.</span></span>

<span data-ttu-id="cd272-105">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="cd272-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd272-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="cd272-106">Syntax</span></span>


```JScript
strArguments = ShellLinkObject.Arguments
ShellLinkObject.Arguments(sArguments) = strArguments
```



## <a name="property-value"></a><span data-ttu-id="cd272-107">屬性值</span><span class="sxs-lookup"><span data-stu-id="cd272-107">Property value</span></span>

<span data-ttu-id="cd272-108">連結的引數。</span><span class="sxs-lookup"><span data-stu-id="cd272-108">the link's arguments.</span></span>

## <a name="examples"></a><span data-ttu-id="cd272-109">範例</span><span class="sxs-lookup"><span data-stu-id="cd272-109">Examples</span></span>

<span data-ttu-id="cd272-110">下列範例會使用 **引數** ，以取得使用者 [開始] 功能表中所找到 Internet Explorer 連結的引數。</span><span class="sxs-lookup"><span data-stu-id="cd272-110">The following example uses **Arguments** to retrieve the arguments for a link to Internet Explorer found in the user's Start menu.</span></span> <span data-ttu-id="cd272-111">JScript、VBScript 和 Visual Basic 會顯示適當的使用方式。</span><span class="sxs-lookup"><span data-stu-id="cd272-111">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="cd272-112">Jscript：</span><span class="sxs-lookup"><span data-stu-id="cd272-112">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellShellLinkObjectArgumentJ()
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
                    var szArguments;
                    
                    // Get the arguments for the ShellLinkObject
                    szArguments = objShellLink.Arguments;
                    alert(szArguments);
                    
                    // Set the arguments for the ShellLinkObject
                    objShellLink.Arguments = "/s"
                }
            }
        }
    }
</script>
```



<span data-ttu-id="cd272-113">VBScript</span><span class="sxs-lookup"><span data-stu-id="cd272-113">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellLinkObjectArgumentVB()
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
                    dim szArguments
                    
                    'Get the arguments for the ShellLinkObject
                    szArguments = objShellLink.Arguments
                    alert(szArguments)
                    
                    'Set the arguments for the ShellLinkObject
                    objShellLink.Arguments = "/s"
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



<span data-ttu-id="cd272-114">Visual Basic：</span><span class="sxs-lookup"><span data-stu-id="cd272-114">Visual Basic:</span></span>


```VB
Private Sub fnShellLinkObjectArgumentsVB()
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
                    Dim szArguments As String
                    
                    'Get the arguments for the ShellLinkObject
                    szArguments = objShellLink.Arguments
                    Debug.Print szArguments
                    
                    'Set the arguments for the ShellLinkObject
                    objShellLink.Arguments = "/s"
                End If

                Set objShellLink = Nothing
            End If

            Set objFolderItem = Nothing
        End If
    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="cd272-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="cd272-115">Requirements</span></span>



| <span data-ttu-id="cd272-116">需求</span><span class="sxs-lookup"><span data-stu-id="cd272-116">Requirement</span></span> | <span data-ttu-id="cd272-117">值</span><span class="sxs-lookup"><span data-stu-id="cd272-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd272-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cd272-118">Minimum supported client</span></span><br/> | <span data-ttu-id="cd272-119">僅限 Windows 2000 Professional 含 SP3 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cd272-119">Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="cd272-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cd272-120">Minimum supported server</span></span><br/> | <span data-ttu-id="cd272-121">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cd272-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="cd272-122">標頭</span><span class="sxs-lookup"><span data-stu-id="cd272-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="cd272-123"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="cd272-123"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="cd272-124">Idl</span><span class="sxs-lookup"><span data-stu-id="cd272-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="cd272-125"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="cd272-125"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="cd272-126">DLL</span><span class="sxs-lookup"><span data-stu-id="cd272-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cd272-127"><dt>Shell32.dll (5.0 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="cd272-127"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 




