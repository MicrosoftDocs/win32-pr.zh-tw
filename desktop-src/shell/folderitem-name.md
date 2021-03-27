---
description: 設定或取得專案的名稱。
ms.assetid: 079efc8d-3d08-48b1-bdb1-83f4b89fd633
title: 'FolderItem.Name 屬性 (Shldisp) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItem.Name
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 5f5eb757455b8bbbd4161eae477ca4677eef4fc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847625"
---
# <a name="folderitemname-property"></a><span data-ttu-id="f30a9-103">FolderItem.Name 屬性</span><span class="sxs-lookup"><span data-stu-id="f30a9-103">FolderItem.Name property</span></span>

<span data-ttu-id="f30a9-104">設定或取得專案的名稱。</span><span class="sxs-lookup"><span data-stu-id="f30a9-104">Sets or gets the item's name.</span></span>

<span data-ttu-id="f30a9-105">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="f30a9-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="f30a9-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="f30a9-106">Syntax</span></span>


```JScript
strName = FolderItem.Name
FolderItem.Name = strName
```



## <a name="property-value"></a><span data-ttu-id="f30a9-107">屬性值</span><span class="sxs-lookup"><span data-stu-id="f30a9-107">Property value</span></span>

<span data-ttu-id="f30a9-108">指定或接收專案名稱之 [**BSTR**](/previous-versions/windows/desktop/automat/bstr) 類型的變數。</span><span class="sxs-lookup"><span data-stu-id="f30a9-108">A variable of type [**BSTR**](/previous-versions/windows/desktop/automat/bstr) that specifies or receives the item's name.</span></span>

## <a name="examples"></a><span data-ttu-id="f30a9-109">範例</span><span class="sxs-lookup"><span data-stu-id="f30a9-109">Examples</span></span>

<span data-ttu-id="f30a9-110">下列範例會使用 **名稱** 來取出 Autoexec.bat 檔案的名稱，然後將名稱重設為 Test.bat。</span><span class="sxs-lookup"><span data-stu-id="f30a9-110">The following example uses **Name** to retrieve the name of the Autoexec.bat file, then reset the name to Test.bat.</span></span> <span data-ttu-id="f30a9-111">JScript、VBScript 和 Visual Basic 會顯示適當的使用方式。</span><span class="sxs-lookup"><span data-stu-id="f30a9-111">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="f30a9-112">Jscript：</span><span class="sxs-lookup"><span data-stu-id="f30a9-112">JScript:</span></span>


```JScript
<script language="JScript">
    function fnNameGetSetJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder2;
        
        objFolder2 = objShell.NameSpace("C:\\");
        if (objFolder2 != null)
        {
            var objFolderItem;
            
            objFolderItem = objFolder2.ParseName("AUTOEXEC.BAT");
            if (objFolderItem != null)
            {
                var szReturn;
                
                szReturn = objFolderItem.Name;
                objFolderItem.Name = "TEST.BAT";
            }
        }
    }
</script>
```



<span data-ttu-id="f30a9-113">VBScript</span><span class="sxs-lookup"><span data-stu-id="f30a9-113">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnNameGetSetVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        if (not objShell is nothing) then
            dim objFolder2
                
            set objFolder2 = objShell.NameSpace("C:\")
            if (not objFolder2 is nothing) then
                dim objFolderItem
                        
                set objFolderItem = objFolder2.ParseName("AUTOEXEC.BAT")
                if (not objFolderItem is nothing) then
                    dim szReturn
                                
                    szReturn = objFolderItem.Name
                    objFolderItem.Name = "TEST.BAT"
                end if
                set objFolderItem = nothing
            end if
            set objFolder2 = nothing
        end if
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="f30a9-114">Visual Basic：</span><span class="sxs-lookup"><span data-stu-id="f30a9-114">Visual Basic:</span></span>


```VB
Private Sub fnNameGetSetVB()
    Dim objShell   As Shell
    Dim objFolder2 As Folder2
    
    Set objShell = New Shell
    Set objFolder2 = objShell.NameSpace("C:\")
        If (Not objFolder2 Is Nothing) Then
            Dim objFolderItem As FolderItem
            
            Set objFolderItem = objFolder2.ParseName("AUTOEXEC.BAT")
                If (Not objFolderItem Is Nothing) Then
                    Dim szReturn As String
                    
                    szReturn = objFolderItem.Name
                    objFolderItem.Name = "TEST.BAT"
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



## <a name="requirements"></a><span data-ttu-id="f30a9-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="f30a9-115">Requirements</span></span>



| <span data-ttu-id="f30a9-116">需求</span><span class="sxs-lookup"><span data-stu-id="f30a9-116">Requirement</span></span> | <span data-ttu-id="f30a9-117">值</span><span class="sxs-lookup"><span data-stu-id="f30a9-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f30a9-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f30a9-118">Minimum supported client</span></span><br/> | <span data-ttu-id="f30a9-119">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f30a9-119">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="f30a9-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f30a9-120">Minimum supported server</span></span><br/> | <span data-ttu-id="f30a9-121">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f30a9-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="f30a9-122">標頭</span><span class="sxs-lookup"><span data-stu-id="f30a9-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="f30a9-123"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="f30a9-123"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="f30a9-124">Idl</span><span class="sxs-lookup"><span data-stu-id="f30a9-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f30a9-125"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="f30a9-125"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="f30a9-126">DLL</span><span class="sxs-lookup"><span data-stu-id="f30a9-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f30a9-127"><dt>Shell32.dll (4.71 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="f30a9-127"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
