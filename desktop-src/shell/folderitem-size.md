---
description: 包含專案的大小。
ms.assetid: 0eda405e-d54f-48d2-a060-a1fdcdb23785
title: 'FolderItem. Size 屬性 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItem.Size
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 5d44d1c1ddd9b46f768f218250802562f9a36312
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510778"
---
# <a name="folderitemsize-property"></a><span data-ttu-id="f9cd8-103">FolderItem. Size 屬性</span><span class="sxs-lookup"><span data-stu-id="f9cd8-103">FolderItem.Size property</span></span>

<span data-ttu-id="f9cd8-104">包含專案的大小。</span><span class="sxs-lookup"><span data-stu-id="f9cd8-104">Contains the item's size.</span></span>

<span data-ttu-id="f9cd8-105">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="f9cd8-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9cd8-106">語法</span><span class="sxs-lookup"><span data-stu-id="f9cd8-106">Syntax</span></span>


```JScript
iSize = FolderItem.Size
```



## <a name="property-value"></a><span data-ttu-id="f9cd8-107">屬性值</span><span class="sxs-lookup"><span data-stu-id="f9cd8-107">Property value</span></span>

<span data-ttu-id="f9cd8-108">接收專案大小的 **整數** 。</span><span class="sxs-lookup"><span data-stu-id="f9cd8-108">An **Integer** that receives the item's size.</span></span>

## <a name="examples"></a><span data-ttu-id="f9cd8-109">範例</span><span class="sxs-lookup"><span data-stu-id="f9cd8-109">Examples</span></span>

<span data-ttu-id="f9cd8-110">下列範例會使用 **大小** 來取得「記事本」可執行檔的大小。</span><span class="sxs-lookup"><span data-stu-id="f9cd8-110">The following example uses **Size** to retrieve the size of the Notepad executable file.</span></span> <span data-ttu-id="f9cd8-111">JScript、VBScript 和 Visual Basic 會顯示適當的使用方式。</span><span class="sxs-lookup"><span data-stu-id="f9cd8-111">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="f9cd8-112">Jscript：</span><span class="sxs-lookup"><span data-stu-id="f9cd8-112">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFolderItemSizeJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder2;
        var ssfWINDOWS = 36;
        
        objFolder2 = objShell.NameSpace(ssfWINDOWS);
        if (objFolder2 != null)
        {
            var objFolderItem;
            
            objFolderItem = objFolder2.ParseName("NOTEPAD.EXE");
            if (objFolderItem != null)
            {
                var szReturn;
                
                szReturn = objFolderItem.Size;
            }
        }
    }
</script>
```



<span data-ttu-id="f9cd8-113">VBScript</span><span class="sxs-lookup"><span data-stu-id="f9cd8-113">VBScript:</span></span>


```VB
 <script language="VBScript">
    function fnFolderItemSizeVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        if (not objShell is nothing) then
            dim objFolder2
            dim ssfWINDOWS
                
            ssfWINDOWS = 36
            set objFolder2 = objShell.NameSpace(ssfWINDOWS)
            if (not objFolder2 is nothing) then
                dim objFolderItem
                        
                set objFolderItem = objFolder2.ParseName("NOTEPAD.EXE")
                if (not objFolderItem is nothing) then
                    dim szReturn
                                
                    szReturn = objFolderItem.Size
                end if
                set objFolderItem = nothing
            end if
            set objFolder2 = nothing
        end if
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="f9cd8-114">Visual Basic：</span><span class="sxs-lookup"><span data-stu-id="f9cd8-114">Visual Basic:</span></span>


```VB
Private Sub fnFolderItemSizeVB()
    Dim objShell   As Shell
    Dim objFolder2 As Folder2
    Dim ssfWINDOWS As Long
    
    ssfWINDOWS = 36
    Set objShell = New Shell
    Set objFolder2 = objShell.NameSpace(ssfWINDOWS)
        If (Not objFolder2 Is Nothing) Then
            Dim objFolderItem As FolderItem
            
            Set objFolderItem = objFolder2.ParseName("NOTEPAD.EXE")
                If (Not objFolderItem Is Nothing) Then
                    Dim szReturn As String
                    
                    szReturn = objFolderItem.Size
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



## <a name="requirements"></a><span data-ttu-id="f9cd8-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="f9cd8-115">Requirements</span></span>



| <span data-ttu-id="f9cd8-116">需求</span><span class="sxs-lookup"><span data-stu-id="f9cd8-116">Requirement</span></span> | <span data-ttu-id="f9cd8-117">值</span><span class="sxs-lookup"><span data-stu-id="f9cd8-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9cd8-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f9cd8-118">Minimum supported client</span></span><br/> | <span data-ttu-id="f9cd8-119">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f9cd8-119">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="f9cd8-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f9cd8-120">Minimum supported server</span></span><br/> | <span data-ttu-id="f9cd8-121">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f9cd8-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="f9cd8-122">標頭</span><span class="sxs-lookup"><span data-stu-id="f9cd8-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="f9cd8-123"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="f9cd8-123"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="f9cd8-124">Idl</span><span class="sxs-lookup"><span data-stu-id="f9cd8-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f9cd8-125"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="f9cd8-125"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="f9cd8-126">DLL</span><span class="sxs-lookup"><span data-stu-id="f9cd8-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f9cd8-127"><dt>Shell32.dll (4.71 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="f9cd8-127"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




