---
description: 指出專案是否為快捷方式。
ms.assetid: f3400f0b-5c7f-4d41-a162-1c35014082ac
title: 'FolderItem. IsLink 屬性 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItem.IsLink
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: bd4357485dce3f3d236f31797d8b2df7028f3d65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847626"
---
# <a name="folderitemislink-property"></a><span data-ttu-id="7a9fd-103">FolderItem. IsLink 屬性</span><span class="sxs-lookup"><span data-stu-id="7a9fd-103">FolderItem.IsLink property</span></span>

<span data-ttu-id="7a9fd-104">指出專案是否為快捷方式。</span><span class="sxs-lookup"><span data-stu-id="7a9fd-104">Indicates whether the item is a shortcut.</span></span>

<span data-ttu-id="7a9fd-105">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="7a9fd-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a9fd-106">語法</span><span class="sxs-lookup"><span data-stu-id="7a9fd-106">Syntax</span></span>


```JScript
bIsLink = FolderItem.IsLink
```



## <a name="property-value"></a><span data-ttu-id="7a9fd-107">屬性值</span><span class="sxs-lookup"><span data-stu-id="7a9fd-107">Property value</span></span>

<span data-ttu-id="7a9fd-108">如果專案是快捷方式，則為收到 **true** 的 **布林值**; 如果不是，則為 **false** 。</span><span class="sxs-lookup"><span data-stu-id="7a9fd-108">A **Boolean** that receives **true** if the item is a shortcut or **false** if not.</span></span>

## <a name="examples"></a><span data-ttu-id="7a9fd-109">範例</span><span class="sxs-lookup"><span data-stu-id="7a9fd-109">Examples</span></span>

<span data-ttu-id="7a9fd-110">下列範例會使用 **IsLink** 來判斷特定物件是否為連結。</span><span class="sxs-lookup"><span data-stu-id="7a9fd-110">The following example uses **IsLink** to determine whether a particular object is a link.</span></span> <span data-ttu-id="7a9fd-111">在此情況下，物件是 Internet Explorer 的快捷方式，因此應該會傳回 **true**。</span><span class="sxs-lookup"><span data-stu-id="7a9fd-111">In this case, the object is a shortcut to Internet Explorer and so should return **true**.</span></span> <span data-ttu-id="7a9fd-112">JScript、VBScript 和 Visual Basic 會顯示適當的使用方式。</span><span class="sxs-lookup"><span data-stu-id="7a9fd-112">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="7a9fd-113">Jscript：</span><span class="sxs-lookup"><span data-stu-id="7a9fd-113">JScript:</span></span>


```JScript
<script language="JScript">
    function fnIsLinkJ()
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
                var bReturn;
                
                bReturn = objFolderItem.IsLink;
            }
        }
    }
</script>
```



<span data-ttu-id="7a9fd-114">VBScript</span><span class="sxs-lookup"><span data-stu-id="7a9fd-114">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnIsLinkVB()
        dim objShell
        
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
                    dim bReturn
                                
                    bReturn = objFolderItem.IsLink
                end if
                set objFolderItem = nothing
            end if
            set objFolder2 = nothing
        end if
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="7a9fd-115">Visual Basic：</span><span class="sxs-lookup"><span data-stu-id="7a9fd-115">Visual Basic:</span></span>


```VB
Private Sub fnIsLinkVB()
    Dim objShell    As Shell
    Dim objFolder2  As Folder2
    Dim ssfPROGRAMS As Long
    
    ssfPROGRAMS = 2
    Set objShell = New Shell
    Set objFolder2 = objShell.NameSpace(ssfPROGRAMS)
        If (Not objFolder2 Is Nothing) Then
            Dim objFolderItem As FolderItem
            
            Set objFolderItem = objFolder2.ParseName("Internet Explorer.lnk")
                If (Not objFolderItem Is Nothing) Then
                    Dim bReturn As Boolean
                    
                    bReturn = objFolderItem.IsLink
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



## <a name="requirements"></a><span data-ttu-id="7a9fd-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="7a9fd-116">Requirements</span></span>



| <span data-ttu-id="7a9fd-117">需求</span><span class="sxs-lookup"><span data-stu-id="7a9fd-117">Requirement</span></span> | <span data-ttu-id="7a9fd-118">值</span><span class="sxs-lookup"><span data-stu-id="7a9fd-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a9fd-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7a9fd-119">Minimum supported client</span></span><br/> | <span data-ttu-id="7a9fd-120">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7a9fd-120">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="7a9fd-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7a9fd-121">Minimum supported server</span></span><br/> | <span data-ttu-id="7a9fd-122">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7a9fd-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="7a9fd-123">標頭</span><span class="sxs-lookup"><span data-stu-id="7a9fd-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="7a9fd-124"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="7a9fd-124"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="7a9fd-125">Idl</span><span class="sxs-lookup"><span data-stu-id="7a9fd-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7a9fd-126"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="7a9fd-126"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="7a9fd-127">DLL</span><span class="sxs-lookup"><span data-stu-id="7a9fd-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7a9fd-128"><dt>Shell32.dll (4.71 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="7a9fd-128"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




