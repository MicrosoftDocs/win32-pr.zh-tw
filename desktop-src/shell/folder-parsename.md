---
description: 建立並傳回 FolderItem 物件，該物件表示指定的專案。
ms.assetid: 3af7052c-fb81-4a96-9bf9-379b0365a376
title: 'ParseName 方法 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder.ParseName
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: ea9a8090a794f23693ae4fef10556bc207f16531
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689264"
---
# <a name="folderparsename-method"></a><span data-ttu-id="09e1d-103">ParseName 方法</span><span class="sxs-lookup"><span data-stu-id="09e1d-103">Folder.ParseName method</span></span>

<span data-ttu-id="09e1d-104">建立並傳回 [**FolderItem**](folderitem.md) 物件，該物件表示指定的專案。</span><span class="sxs-lookup"><span data-stu-id="09e1d-104">Creates and returns a [**FolderItem**](folderitem.md) object that represents a specified item.</span></span>

## <a name="syntax"></a><span data-ttu-id="09e1d-105">語法</span><span class="sxs-lookup"><span data-stu-id="09e1d-105">Syntax</span></span>


```JScript
retVal = Folder.ParseName(
  bName
)
```



## <a name="parameters"></a><span data-ttu-id="09e1d-106">參數</span><span class="sxs-lookup"><span data-stu-id="09e1d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09e1d-107">*bName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="09e1d-107">*bName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09e1d-108">類型： **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="09e1d-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="09e1d-109">指定專案名稱的字串。</span><span class="sxs-lookup"><span data-stu-id="09e1d-109">A string that specifies the name of the item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="09e1d-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="09e1d-110">Return value</span></span>

<span data-ttu-id="09e1d-111">類型： **[ **FolderItem**](folderitem.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="09e1d-111">Type: **[**FolderItem**](folderitem.md)\*\***</span></span>

<span data-ttu-id="09e1d-112">[**FolderItem**](folderitem.md)物件的物件參考。</span><span class="sxs-lookup"><span data-stu-id="09e1d-112">An object reference to the [**FolderItem**](folderitem.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="09e1d-113">備註</span><span class="sxs-lookup"><span data-stu-id="09e1d-113">Remarks</span></span>

<span data-ttu-id="09e1d-114">**ParseName** 不能用於虛擬資料夾，例如我的檔。</span><span class="sxs-lookup"><span data-stu-id="09e1d-114">**ParseName** should not be used for virtual folders such as My Documents.</span></span>

## <a name="examples"></a><span data-ttu-id="09e1d-115">範例</span><span class="sxs-lookup"><span data-stu-id="09e1d-115">Examples</span></span>

<span data-ttu-id="09e1d-116">下列範例會使用 **ParseName** 建立物件，代表 C： Windows 資料夾中 Clock.avi 的資料夾專案 \\ 。</span><span class="sxs-lookup"><span data-stu-id="09e1d-116">The following example uses **ParseName** to create an object representing the folder item Clock.avi in the C:\\Windows folder.</span></span> <span data-ttu-id="09e1d-117">JScript、VBScript 和 Visual Basic 會顯示適當的使用方式。</span><span class="sxs-lookup"><span data-stu-id="09e1d-117">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="09e1d-118">Jscript：</span><span class="sxs-lookup"><span data-stu-id="09e1d-118">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFolderObjectParseNameJ()
    {
        var objShell  = new ActiveXObject("shell.application");
        var objFolder = new Object;
        
        objFolder = objShell.NameSpace("C:\\WINDOWS");
        if (objFolder != null)
        {
            var objFolderItem = new Object;
            
            objFolderItem = objFolder.ParseName("clock.avi");
            if (objFolderItem != null)
            {
                //Add code here.
            }
        }
    }
</script>
```



<span data-ttu-id="09e1d-119">VBScript</span><span class="sxs-lookup"><span data-stu-id="09e1d-119">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnFolderObjectParseNameVB()
        dim objShell
        dim objFolder
        
        set objShell = CreateObject("shell.application")
        set objFolder = objShell.NameSpace("C:\WINDOWS")

        if (not objFolder is nothing) then
            dim objFolderItem
            
            set objFolderItem = objFolder.ParseName("clock.avi")

            if (not objFolderItem is nothing) then
                'Add code here.
            end if
        end if

        set objFolder = nothing
        set objShell = nothing
    end function
</script>
```



<span data-ttu-id="09e1d-120">Visual Basic：</span><span class="sxs-lookup"><span data-stu-id="09e1d-120">Visual Basic:</span></span>


```VB
Private Sub btnParseName_Click()
    Dim objShell  As Shell
    Dim objFolder As Folder

    Set objShell = New Shell
    Set objFolder = objShell.NameSpace("C:\WINDOWS")

    If (Not objFolder Is Nothing) Then
        Dim objFolderItem As FolderItem
        
        Set objFolderItem = objFolder.ParseName("clock.avi")
            'Add code here.
            Debug.Print "passed"
        Set objFolderItem = Nothing
    End If

    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="09e1d-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="09e1d-121">Requirements</span></span>



| <span data-ttu-id="09e1d-122">需求</span><span class="sxs-lookup"><span data-stu-id="09e1d-122">Requirement</span></span> | <span data-ttu-id="09e1d-123">值</span><span class="sxs-lookup"><span data-stu-id="09e1d-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="09e1d-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="09e1d-124">Minimum supported client</span></span><br/> | <span data-ttu-id="09e1d-125">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="09e1d-125">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="09e1d-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="09e1d-126">Minimum supported server</span></span><br/> | <span data-ttu-id="09e1d-127">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="09e1d-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="09e1d-128">標頭</span><span class="sxs-lookup"><span data-stu-id="09e1d-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="09e1d-129"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="09e1d-129"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="09e1d-130">Idl</span><span class="sxs-lookup"><span data-stu-id="09e1d-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="09e1d-131"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="09e1d-131"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="09e1d-132">DLL</span><span class="sxs-lookup"><span data-stu-id="09e1d-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="09e1d-133"><dt>Shell32.dll (4.71 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="09e1d-133"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
