---
description: 包含專案的完整路徑和名稱。
ms.assetid: c94c7c1c-9dc9-4bb8-b7ec-01541baa2924
title: 'FolderItem： Path 屬性 (Shldisp. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItem.Path
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: a9562fc94cc0d4253ce80f6bd494c818689c71a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111732"
---
# <a name="folderitempath-property"></a><span data-ttu-id="e6c21-103">FolderItem 路徑屬性</span><span class="sxs-lookup"><span data-stu-id="e6c21-103">FolderItem.Path property</span></span>

<span data-ttu-id="e6c21-104">包含專案的完整路徑和名稱。</span><span class="sxs-lookup"><span data-stu-id="e6c21-104">Contains the item's full path and name.</span></span>

<span data-ttu-id="e6c21-105">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="e6c21-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6c21-106">語法</span><span class="sxs-lookup"><span data-stu-id="e6c21-106">Syntax</span></span>


```JScript
strPath = FolderItem.Path
```



## <a name="property-value"></a><span data-ttu-id="e6c21-107">屬性值</span><span class="sxs-lookup"><span data-stu-id="e6c21-107">Property value</span></span>

<span data-ttu-id="e6c21-108">[**BSTR**](/previous-versions/windows/desktop/automat/bstr)類型的變數，可接收專案的完整路徑和名稱。</span><span class="sxs-lookup"><span data-stu-id="e6c21-108">A variable of type [**BSTR**](/previous-versions/windows/desktop/automat/bstr) that receives the item's full path and name.</span></span>

## <a name="examples"></a><span data-ttu-id="e6c21-109">範例</span><span class="sxs-lookup"><span data-stu-id="e6c21-109">Examples</span></span>

<span data-ttu-id="e6c21-110">下列範例會使用 **路徑** 來取得 Windows 資料夾的路徑。</span><span class="sxs-lookup"><span data-stu-id="e6c21-110">The following example uses **Path** to retrieve the path of the Windows folder.</span></span> <span data-ttu-id="e6c21-111">JScript、VBScript 和 Visual Basic 會顯示適當的使用方式。</span><span class="sxs-lookup"><span data-stu-id="e6c21-111">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="e6c21-112">Jscript：</span><span class="sxs-lookup"><span data-stu-id="e6c21-112">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFolderItemPathJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder2;
        var ssfWINDOWS = 36;
        
        objFolder2 = objShell.NameSpace(ssfWINDOWS);
        if (objFolder2 != null)
        {
            var objFolderItem;
            
            objFolderItem = objFolder2.Self;
            if (objFolderItem != null)
            {
                var szReturn;
                
                szReturn = objFolderItem.Path;
            }
        }
    }
</script>
```



<span data-ttu-id="e6c21-113">VBScript</span><span class="sxs-lookup"><span data-stu-id="e6c21-113">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnFolderItemPathVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        if (not objShell is nothing) then
            dim objFolder2
            dim ssfWINDOWS
                
            ssfWINDOWS = 36
            set objFolder2 = objShell.NameSpace(ssfWINDOWS)
            if (not objFolder2 is nothing) then
                dim objFolderItem
                        
                set objFolderItem = objFolder2.Self
                if (not objFolderItem is nothing) then
                    dim szReturn
                                
                    szReturn = objFolderItem.Path
                end if
                set objFolderItem = nothing
            end if
            set objFolder2 = nothing
        end if
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="e6c21-114">Visual Basic：</span><span class="sxs-lookup"><span data-stu-id="e6c21-114">Visual Basic:</span></span>


```VB
Private Sub fnFolderItemPathVB()
    Dim objShell   As Shell
    Dim objFolder2 As Folder2
    Dim ssfWINDOWS As Long
    
    ssfWINDOWS = 36
    Set objShell = New Shell
    Set objFolder2 = objShell.NameSpace(ssfWINDOWS)
        If (Not objFolder2 Is Nothing) Then
            Dim objFolderItem As FolderItem
            
            Set objFolderItem = objFolder2.Self
                If (Not objFolderItem Is Nothing) Then
                    Dim szReturn As String
                    
                    szReturn = objFolderItem.Path
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



## <a name="requirements"></a><span data-ttu-id="e6c21-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="e6c21-115">Requirements</span></span>



| <span data-ttu-id="e6c21-116">需求</span><span class="sxs-lookup"><span data-stu-id="e6c21-116">Requirement</span></span> | <span data-ttu-id="e6c21-117">值</span><span class="sxs-lookup"><span data-stu-id="e6c21-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6c21-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e6c21-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e6c21-119">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e6c21-119">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="e6c21-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e6c21-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e6c21-121">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e6c21-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="e6c21-122">標頭</span><span class="sxs-lookup"><span data-stu-id="e6c21-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="e6c21-123"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="e6c21-123"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="e6c21-124">Idl</span><span class="sxs-lookup"><span data-stu-id="e6c21-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e6c21-125"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="e6c21-125"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="e6c21-126">DLL</span><span class="sxs-lookup"><span data-stu-id="e6c21-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e6c21-127"><dt>Shell32.dll (4.71 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="e6c21-127"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
