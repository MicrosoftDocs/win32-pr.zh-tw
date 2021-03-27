---
description: 如果專案是資料夾，則包含專案的資料夾物件。
ms.assetid: 87afd0b6-245b-4550-9f21-aa0426ba8470
title: 'FolderItem. GetFolder 屬性 (Shlobj.h .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItem.GetFolder
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: d08c774b53d1fa0db74a7d8d282c4f88f237cfd4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689263"
---
# <a name="folderitemgetfolder-property"></a><span data-ttu-id="2d12c-103">FolderItem. GetFolder 屬性</span><span class="sxs-lookup"><span data-stu-id="2d12c-103">FolderItem.GetFolder property</span></span>

<span data-ttu-id="2d12c-104">如果專案是資料夾，則包含專案的 [**資料夾**](folder.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="2d12c-104">Contains the item's [**Folder**](folder.md) object, if the item is a folder.</span></span>

<span data-ttu-id="2d12c-105">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="2d12c-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d12c-106">語法</span><span class="sxs-lookup"><span data-stu-id="2d12c-106">Syntax</span></span>


```JScript
objGetFolder = FolderItem.GetFolder
```



## <a name="property-value"></a><span data-ttu-id="2d12c-107">屬性值</span><span class="sxs-lookup"><span data-stu-id="2d12c-107">Property value</span></span>

<span data-ttu-id="2d12c-108">[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)型別的變數，會接收 [**資料夾**](folder.md)物件。</span><span class="sxs-lookup"><span data-stu-id="2d12c-108">A variable of type [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) that receives the [**Folder**](folder.md) object.</span></span>

## <a name="examples"></a><span data-ttu-id="2d12c-109">範例</span><span class="sxs-lookup"><span data-stu-id="2d12c-109">Examples</span></span>

<span data-ttu-id="2d12c-110">下列範例會使用 **GetFolder** 來取得 System32 資料夾的 [**資料夾**](folder.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="2d12c-110">The following example uses **GetFolder** to retrieve the [**Folder**](folder.md) object for the System32 folder.</span></span> <span data-ttu-id="2d12c-111">JScript、VBScript 和 Visual Basic 會顯示適當的使用方式。</span><span class="sxs-lookup"><span data-stu-id="2d12c-111">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="2d12c-112">Jscript：</span><span class="sxs-lookup"><span data-stu-id="2d12c-112">JScript:</span></span>


```JScript
<script language="JScript">
    function fnGetFolderJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder2;
        var ssfWINDOWS = 36;
        
        objFolder2 = objShell.NameSpace(ssfWINDOWS);
        if (objFolder2 != null)
        {
            var objFolderItem;
            
            objFolderItem = objFolder2.ParseName("system32");
            if (objFolderItem != null)
            {
                var objFolder;
                
                objFolder = objFolderItem.GetFolder;
                if (objFolder != null)
                {
                    ...
                }
            }
        }
    }
 </script>
```



<span data-ttu-id="2d12c-113">VBScript</span><span class="sxs-lookup"><span data-stu-id="2d12c-113">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnGetFolderVB()
        dim objShell
        dim bReturn

        set objShell = CreateObject("shell.application")
        if (not objShell is nothing) then
            dim objFolder2
            dim ssfWINDOWS
                
            ssfWINDOWS = 36
            set objFolder2 = objShell.NameSpace(36)
            if (not objFolder2 is nothing) then
                dim objFolderItem
                        
                set objFolderItem = objFolder2.ParseName("system32")
                if (not objFolderItem is nothing) then
                    dim objFolder
                                
                    set objFolder = objFolderItem.GetFolder
                    if (not objFolder is nothing) then
                        'Add code here         
                    end if
                    set objFolder = nothing
                end if
                set objFolderItem = nothing
            end if
            set objFolder2 = nothing
        end if
        set objShell = nothing
    end function
</script>
```



<span data-ttu-id="2d12c-114">Visual Basic：</span><span class="sxs-lookup"><span data-stu-id="2d12c-114">Visual Basic:</span></span>


```VB
Private Sub fnGetFolderVB()
    Dim objShell   As Shell
    Dim objFolder2 As Folder2
    Dim ssfWINDOWS As Long
    
    ssfWINDOWS = 36
    Set objShell = New Shell
    Set objFolder2 = objShell.NameSpace(ssfWINDOWS)
        If (Not objFolder2 Is Nothing) Then
            Dim objFolderItem As FolderItem
            
            Set objFolderItem = objFolder2.ParseName("system32")
                If (Not objFolderItem Is Nothing) Then
                    Dim objFolder As Folder2
                    
                    Set objFolder = objFolderItem.GetFolder
                        If (Not objFolder Is Nothing) Then
                            'Add code here
                            Debug.Print "Yes"
                        Else
                            'Folder object returned nothing
                        End If
                    Set objFolder = Nothing
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



## <a name="requirements"></a><span data-ttu-id="2d12c-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="2d12c-115">Requirements</span></span>



| <span data-ttu-id="2d12c-116">需求</span><span class="sxs-lookup"><span data-stu-id="2d12c-116">Requirement</span></span> | <span data-ttu-id="2d12c-117">值</span><span class="sxs-lookup"><span data-stu-id="2d12c-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d12c-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2d12c-118">Minimum supported client</span></span><br/> | <span data-ttu-id="2d12c-119">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2d12c-119">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="2d12c-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2d12c-120">Minimum supported server</span></span><br/> | <span data-ttu-id="2d12c-121">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2d12c-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="2d12c-122">標頭</span><span class="sxs-lookup"><span data-stu-id="2d12c-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="2d12c-123"><dt>Shlobj.h (包含 Shldisp) </dt></span><span class="sxs-lookup"><span data-stu-id="2d12c-123"><dt>Shlobj.h (include Shldisp.h)</dt></span></span> </dl>        |
| <span data-ttu-id="2d12c-124">Idl</span><span class="sxs-lookup"><span data-stu-id="2d12c-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2d12c-125"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="2d12c-125"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="2d12c-126">DLL</span><span class="sxs-lookup"><span data-stu-id="2d12c-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2d12c-127"><dt>Shell32.dll (4.71 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="2d12c-127"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2d12c-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2d12c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d12c-129">**FolderItem**</span><span class="sxs-lookup"><span data-stu-id="2d12c-129">**FolderItem**</span></span>](folderitem.md)
</dt> <dt>

[<span data-ttu-id="2d12c-130">**IsFolder**</span><span class="sxs-lookup"><span data-stu-id="2d12c-130">**IsFolder**</span></span>](folderitem-isfolder.md)
</dt> </dl>

 

 
