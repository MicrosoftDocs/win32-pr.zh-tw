---
description: 如果專案是快捷方式，則包含專案的 ShellLinkObject 物件。
ms.assetid: 6444476a-a065-4f69-9330-584e30dbe30d
title: 'FolderItem. GetLink 屬性 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItem.GetLink
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: d12c0fbd296610174c8b8363602288f59fcb9714
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111736"
---
# <a name="folderitemgetlink-property"></a><span data-ttu-id="f366e-103">FolderItem. GetLink 屬性</span><span class="sxs-lookup"><span data-stu-id="f366e-103">FolderItem.GetLink property</span></span>

<span data-ttu-id="f366e-104">如果專案是快捷方式，則包含專案的 [**ShellLinkObject**](shelllinkobject-object.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="f366e-104">Contains the item's [**ShellLinkObject**](shelllinkobject-object.md) object, if the item is a shortcut.</span></span>

<span data-ttu-id="f366e-105">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="f366e-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f366e-106">語法</span><span class="sxs-lookup"><span data-stu-id="f366e-106">Syntax</span></span>


```JScript
objGetLink = FolderItem.GetLink
```



## <a name="property-value"></a><span data-ttu-id="f366e-107">屬性值</span><span class="sxs-lookup"><span data-stu-id="f366e-107">Property value</span></span>

<span data-ttu-id="f366e-108">[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)型別的變數，可接收 [**ShellLinkObject**](shelllinkobject-object.md)物件。</span><span class="sxs-lookup"><span data-stu-id="f366e-108">A variable of type [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) that receives the [**ShellLinkObject**](shelllinkobject-object.md) object.</span></span>

## <a name="examples"></a><span data-ttu-id="f366e-109">範例</span><span class="sxs-lookup"><span data-stu-id="f366e-109">Examples</span></span>

<span data-ttu-id="f366e-110">下列範例會使用 **GetLink** 來捕獲 [**ShellLinkObject**](shelllinkobject-object.md) 物件，以取得 Internet Explorer 的快捷方式。</span><span class="sxs-lookup"><span data-stu-id="f366e-110">The following example uses **GetLink** to retrieve the [**ShellLinkObject**](shelllinkobject-object.md) object for a shortcut to Internet Explorer.</span></span> <span data-ttu-id="f366e-111">JScript、VBScript 和 Visual Basic 會顯示適當的使用方式。</span><span class="sxs-lookup"><span data-stu-id="f366e-111">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="f366e-112">Jscript：</span><span class="sxs-lookup"><span data-stu-id="f366e-112">JScript:</span></span>


```JScript
<script language="JScript">
    function fnGetLinkJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder2;
        var ssfPROGRAMS = 2;
        
        objFolder2 = objShell.NameSpace(ssfPROGRAMS);
        if (objFolder2 != null)
        {
            var objFolderItem;
            
            objFolderItem = objFolder2.ParseName("Internet Explorer.lnk");
            if (objFolderItem != null)
            {
                var objLink;
                
                objLink = objFolderItem.GetLink;
                if (objLink != null)
                {
                    // Add code here
                }
            }
        }
    }
</script>
```



<span data-ttu-id="f366e-113">VBScript</span><span class="sxs-lookup"><span data-stu-id="f366e-113">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnGetLinkVB()
        dim objShell
        dim bReturn

        set objShell = CreateObject("shell.application")
        if (not objShell is nothing) then
            dim objFolder2
            dim ssfPROGRAMS
                
            ssfPROGRAMS = 2
            set objFolder2 = objShell.NameSpace(ssfPROGRAMS)
            if (not objFolder2 is nothing) then
                dim objFolderItem
                        
                set objFolderItem = objFolder2.ParseName("Internet Explorer.lnk")
                if (not objFolderItem is nothing) then
                    dim objLink
                                
                    set objLink = objFolderItem.GetLink
                    if (not objLink is nothing) then
                        'Add code here          
                    end if
                    set objLink = nothing
                end if
                set objFolderItem = nothing
            end if
            set objFolder2 = nothing
        end if
        set objShell = nothing
    end function
</script>
```



<span data-ttu-id="f366e-114">Visual Basic：</span><span class="sxs-lookup"><span data-stu-id="f366e-114">Visual Basic:</span></span>


```VB
Private Sub fnGetLinkVB()
    Dim objShell   As Shell
    Dim objFolder2 As Folder2
    Dim ssfPROGRAMS As Long
    
    ssfPROGRAMS = 2
    Set objShell = New Shell
    Set objFolder2 = objShell.NameSpace(ssfPROGRAMS)
        If (Not objFolder2 Is Nothing) Then
            Dim objFolderItem As FolderItem
            
            Set objFolderItem = objFolder2.ParseName("Internet Explorer.lnk")
                If (Not objFolderItem Is Nothing) Then
                    Dim objLink As ShellLinkObject
                    
                    Set objLink = objFolderItem.GetLink
                        If (Not objLink Is Nothing) Then
                            'Add code here
                        Else
                            'Folder object returned nothing
                        End If
                    Set objLink = Nothing
                Else
                    'FolderItem object returned nothing.
                End If
            Set objFolderItem = Nothing
        Else
            'Folder object returned nothing.
        End If
    Set objFolder2 = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="f366e-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="f366e-115">Requirements</span></span>



| <span data-ttu-id="f366e-116">需求</span><span class="sxs-lookup"><span data-stu-id="f366e-116">Requirement</span></span> | <span data-ttu-id="f366e-117">值</span><span class="sxs-lookup"><span data-stu-id="f366e-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f366e-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f366e-118">Minimum supported client</span></span><br/> | <span data-ttu-id="f366e-119">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f366e-119">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="f366e-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f366e-120">Minimum supported server</span></span><br/> | <span data-ttu-id="f366e-121">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f366e-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="f366e-122">標頭</span><span class="sxs-lookup"><span data-stu-id="f366e-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="f366e-123"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="f366e-123"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="f366e-124">Idl</span><span class="sxs-lookup"><span data-stu-id="f366e-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f366e-125"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="f366e-125"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="f366e-126">DLL</span><span class="sxs-lookup"><span data-stu-id="f366e-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f366e-127"><dt>Shell32.dll (4.71 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="f366e-127"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f366e-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f366e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f366e-129">**FolderItem**</span><span class="sxs-lookup"><span data-stu-id="f366e-129">**FolderItem**</span></span>](folderitem.md)
</dt> <dt>

[<span data-ttu-id="f366e-130">**IsLink**</span><span class="sxs-lookup"><span data-stu-id="f366e-130">**IsLink**</span></span>](folderitem-islink.md)
</dt> </dl>

 

 
