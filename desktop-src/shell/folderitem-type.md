---
description: 包含專案類型的字串表示。
ms.assetid: e851d632-9562-4194-a24c-12e757227b5b
title: 'FolderItem，Type 屬性 (Shldisp. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItem.Type
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 12c3ffe3b32a6d2b2f3021312905839bc5cc1744
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026031"
---
# <a name="folderitemtype-property"></a><span data-ttu-id="67ddc-103">FolderItem。 Type 屬性</span><span class="sxs-lookup"><span data-stu-id="67ddc-103">FolderItem.Type property</span></span>

<span data-ttu-id="67ddc-104">包含專案類型的字串表示。</span><span class="sxs-lookup"><span data-stu-id="67ddc-104">Contains a string representation of the item's type.</span></span>

<span data-ttu-id="67ddc-105">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="67ddc-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="67ddc-106">語法</span><span class="sxs-lookup"><span data-stu-id="67ddc-106">Syntax</span></span>


```JScript
strType = FolderItem.Type
```



## <a name="property-value"></a><span data-ttu-id="67ddc-107">屬性值</span><span class="sxs-lookup"><span data-stu-id="67ddc-107">Property value</span></span>

<span data-ttu-id="67ddc-108">[**BSTR**](/previous-versions/windows/desktop/automat/bstr)類型的變數，可接收專案的型別。</span><span class="sxs-lookup"><span data-stu-id="67ddc-108">A variable of type [**BSTR**](/previous-versions/windows/desktop/automat/bstr) that receives the item's type.</span></span>

## <a name="examples"></a><span data-ttu-id="67ddc-109">範例</span><span class="sxs-lookup"><span data-stu-id="67ddc-109">Examples</span></span>

<span data-ttu-id="67ddc-110">下列範例會使用 **型** 別來取得專案的型別。</span><span class="sxs-lookup"><span data-stu-id="67ddc-110">The following example uses **Type** to retrieve the item's type.</span></span> <span data-ttu-id="67ddc-111">JScript、VBScript 和 Visual Basic 會顯示適當的使用方式。</span><span class="sxs-lookup"><span data-stu-id="67ddc-111">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="67ddc-112">Jscript：</span><span class="sxs-lookup"><span data-stu-id="67ddc-112">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFolderItemTypeJ()
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
                
                szReturn = objFolderItem.Type;
                alert(szReturn);
            }
        }
    }
</script>
```



<span data-ttu-id="67ddc-113">VBScript</span><span class="sxs-lookup"><span data-stu-id="67ddc-113">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnFolderItemTypeVB()
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
                                
                    szReturn = objFolderItem.Type
                end if
                set objFolderItem = nothing
            end if
            set objFolder2 = nothing
        end if
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="67ddc-114">Visual Basic：</span><span class="sxs-lookup"><span data-stu-id="67ddc-114">Visual Basic:</span></span>


```VB
Private Sub fnFolderItemTypeVB()
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
                    
                    szReturn = objFolderItem.Type
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



## <a name="requirements"></a><span data-ttu-id="67ddc-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="67ddc-115">Requirements</span></span>



| <span data-ttu-id="67ddc-116">需求</span><span class="sxs-lookup"><span data-stu-id="67ddc-116">Requirement</span></span> | <span data-ttu-id="67ddc-117">值</span><span class="sxs-lookup"><span data-stu-id="67ddc-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67ddc-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="67ddc-118">Minimum supported client</span></span><br/> | <span data-ttu-id="67ddc-119">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="67ddc-119">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="67ddc-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="67ddc-120">Minimum supported server</span></span><br/> | <span data-ttu-id="67ddc-121">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="67ddc-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="67ddc-122">標頭</span><span class="sxs-lookup"><span data-stu-id="67ddc-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="67ddc-123"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="67ddc-123"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="67ddc-124">Idl</span><span class="sxs-lookup"><span data-stu-id="67ddc-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="67ddc-125"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="67ddc-125"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="67ddc-126">DLL</span><span class="sxs-lookup"><span data-stu-id="67ddc-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="67ddc-127"><dt>Shell32.dll (4.71 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="67ddc-127"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
