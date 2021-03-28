---
description: 抓取 FolderItems 物件，該物件表示資料夾中的專案集合。
ms.assetid: ef2965ec-c8ab-4108-8e5e-b4fd5370521a
title: 'Folder 方法 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder.Items
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: c3cfa0fcd2d8e2e51a67a362b33af34abf5b1427
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104319139"
---
# <a name="folderitems-method"></a><span data-ttu-id="89f30-103">資料夾. 專案方法</span><span class="sxs-lookup"><span data-stu-id="89f30-103">Folder.Items method</span></span>

<span data-ttu-id="89f30-104">抓取 [**FolderItems**](folderitems.md) 物件，該物件表示資料夾中的專案集合。</span><span class="sxs-lookup"><span data-stu-id="89f30-104">Retrieves a [**FolderItems**](folderitems.md) object that represents the collection of items in the folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="89f30-105">語法</span><span class="sxs-lookup"><span data-stu-id="89f30-105">Syntax</span></span>


```JScript
retVal = Folder.Items()
```



## <a name="parameters"></a><span data-ttu-id="89f30-106">參數</span><span class="sxs-lookup"><span data-stu-id="89f30-106">Parameters</span></span>

<span data-ttu-id="89f30-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="89f30-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="89f30-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="89f30-108">Return value</span></span>

<span data-ttu-id="89f30-109">類型： **[ **FolderItems**](folderitems.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="89f30-109">Type: **[**FolderItems**](folderitems.md)\*\***</span></span>

<span data-ttu-id="89f30-110">[**FolderItems**](folderitems.md)物件的物件參考。</span><span class="sxs-lookup"><span data-stu-id="89f30-110">An object reference to the [**FolderItems**](folderitems.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="89f30-111">備註</span><span class="sxs-lookup"><span data-stu-id="89f30-111">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="89f30-112">並非所有的方法都會針對所有資料夾執行。</span><span class="sxs-lookup"><span data-stu-id="89f30-112">Not all methods are implemented for all folders.</span></span> <span data-ttu-id="89f30-113">例如， [**ParseName**](folder-parsename.md) 方法不會針對主控台資料夾執行， (CSIDL \_ 控制項) 。</span><span class="sxs-lookup"><span data-stu-id="89f30-113">For example, the [**ParseName**](folder-parsename.md) method is not implemented for the Control Panel folder (CSIDL\_CONTROLS).</span></span> <span data-ttu-id="89f30-114">如果您嘗試呼叫未產生的方法，則會引發 0x800A01BD (decimal 445) 錯誤。</span><span class="sxs-lookup"><span data-stu-id="89f30-114">If you attempt to call an unimplemented method, a 0x800A01BD (decimal 445) error is raised.</span></span>

 

## <a name="examples"></a><span data-ttu-id="89f30-115">範例</span><span class="sxs-lookup"><span data-stu-id="89f30-115">Examples</span></span>

<span data-ttu-id="89f30-116">下列範例會使用 **專案** 來判斷 C： Windows 資料夾中的專案數 \\ 。</span><span class="sxs-lookup"><span data-stu-id="89f30-116">The following example uses **Items** to determine the number of items in the C:\\Windows folder.</span></span> <span data-ttu-id="89f30-117">JScript、VBScript 和 Visual Basic 會顯示適當的使用方式。</span><span class="sxs-lookup"><span data-stu-id="89f30-117">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="89f30-118">Jscript：</span><span class="sxs-lookup"><span data-stu-id="89f30-118">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFolderObjectItemsJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder = new Object;
        
        objFolder = objShell.NameSpace("C:\\WINDOWS");
        if (objFolder != null)
        {
            var objFolderItems = new Object;
            
            objFolderItems = objFolder.Items();
            if (objFolderItems != null)
            {
                document.write (objFolderItems.Count);
            }
        }
    }
</script>
```



<span data-ttu-id="89f30-119">VBScript</span><span class="sxs-lookup"><span data-stu-id="89f30-119">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnFolderObjectItemsVB()
        dim objShell
        dim objFolder
        
        set objShell = CreateObject("shell.application")
        set objFolder = objShell.NameSpace("C:\WINDOWS")

        if (not objFolder is nothing) then
            dim objFolderItems

            set objFolderItems = objFolder.Items

            if (not objFolderItems Is Nothing) then
                document.write objFolderItems.Count
            end if

            set objFolderItem = nothing
        end if

        set objFolder = nothing
        set objShell = nothing
    end function
</script>
```



<span data-ttu-id="89f30-120">Visual Basic：</span><span class="sxs-lookup"><span data-stu-id="89f30-120">Visual Basic:</span></span>


```VB
Private Sub btnFolderObjectItems_Click()
    Dim objShell  As Shell
    Dim objFolder As Folder

    Set objShell = New Shell
    Set objFolder = objShell.NameSpace("C:\WINDOWS")

    If (Not objFolder Is Nothing) Then
        Dim objFolderItems As FolderItems

        Set objFolderItems = objFolder.Items()

        If (Not objFolderItems Is Nothing) Then
            Dim vCount As Variant

            vCount = objFolderItems.Count
        End If

        Set objFolderItems = Nothing
    End If

    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="89f30-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="89f30-121">Requirements</span></span>



| <span data-ttu-id="89f30-122">需求</span><span class="sxs-lookup"><span data-stu-id="89f30-122">Requirement</span></span> | <span data-ttu-id="89f30-123">值</span><span class="sxs-lookup"><span data-stu-id="89f30-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89f30-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="89f30-124">Minimum supported client</span></span><br/> | <span data-ttu-id="89f30-125">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="89f30-125">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="89f30-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="89f30-126">Minimum supported server</span></span><br/> | <span data-ttu-id="89f30-127">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="89f30-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="89f30-128">標頭</span><span class="sxs-lookup"><span data-stu-id="89f30-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="89f30-129"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="89f30-129"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="89f30-130">Idl</span><span class="sxs-lookup"><span data-stu-id="89f30-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="89f30-131"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="89f30-131"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="89f30-132">DLL</span><span class="sxs-lookup"><span data-stu-id="89f30-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="89f30-133"><dt>Shell32.dll (4.71 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="89f30-133"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




