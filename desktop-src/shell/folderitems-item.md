---
description: 抓取集合中指定之專案的 FolderItem 物件。
ms.assetid: 164f823d-12d9-4950-a881-63837c53760d
title: 'FolderItems 專案方法 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItems.Item
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: ed670ed4af3882e38faf2699429c3d1c076f3056
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104971892"
---
# <a name="folderitemsitem-method"></a><span data-ttu-id="6df97-103">FolderItems 專案方法</span><span class="sxs-lookup"><span data-stu-id="6df97-103">FolderItems.Item method</span></span>

<span data-ttu-id="6df97-104">抓取集合中指定之專案的 [**FolderItem**](folderitem.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="6df97-104">Retrieves the [**FolderItem**](folderitem.md) object for a specified item in the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="6df97-105">語法</span><span class="sxs-lookup"><span data-stu-id="6df97-105">Syntax</span></span>


```JScript
FolderItems.Item(
  [ iIndex ]
)
```



## <a name="parameters"></a><span data-ttu-id="6df97-106">參數</span><span class="sxs-lookup"><span data-stu-id="6df97-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6df97-107">*iIndex* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="6df97-107">*iIndex* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6df97-108">類型： **Variant**</span><span class="sxs-lookup"><span data-stu-id="6df97-108">Type: **Variant**</span></span>

<span data-ttu-id="6df97-109">要擷取之項目的索引，此索引以零起始。</span><span class="sxs-lookup"><span data-stu-id="6df97-109">The zero-based index of the item to retrieve.</span></span> <span data-ttu-id="6df97-110">這個值必須小於 [**Count**](folderitems-count.md) 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="6df97-110">This value must be less than the value of the [**Count**](folderitems-count.md) property.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6df97-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="6df97-111">Return value</span></span>

<span data-ttu-id="6df97-112">[**FolderItem**](folderitem.md)物件的物件參考。</span><span class="sxs-lookup"><span data-stu-id="6df97-112">An object reference to the [**FolderItem**](folderitem.md) object.</span></span>

## <a name="examples"></a><span data-ttu-id="6df97-113">範例</span><span class="sxs-lookup"><span data-stu-id="6df97-113">Examples</span></span>

<span data-ttu-id="6df97-114">下列範例會使用 **專案** 來取出 [**FolderItem**](folderitem.md) 物件，代表在 Windows 資料夾中找到的 Notepad.exe 檔案。</span><span class="sxs-lookup"><span data-stu-id="6df97-114">The following example uses **Item** to retrieve the [**FolderItem**](folderitem.md) object representing the Notepad.exe file found in the Windows folder.</span></span> <span data-ttu-id="6df97-115">JScript、VBScript 和 Visual Basic 會顯示適當的使用方式。</span><span class="sxs-lookup"><span data-stu-id="6df97-115">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="6df97-116">Jscript：</span><span class="sxs-lookup"><span data-stu-id="6df97-116">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFolderItemsItemJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder;
        var ssfWINDOWS = 36;
        
        objFolder = objShell.NameSpace(ssfWINDOWS);
        if (objFolder != null)
        {
            var objFolderItems;
            
            objFolderItems = objFolder.Items();
            if (objFolderItems != null)
            {
                var objFolderItem;
                
                objFolderItem = objFolderItems.Item(objFolderItems.Count - 1);
                alert(objFolderItem.Name);
            }
        }
    }
</script>
```



<span data-ttu-id="6df97-117">VBScript</span><span class="sxs-lookup"><span data-stu-id="6df97-117">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnFolderItemsItemVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        if (not objShell is nothing) then
            dim objFolder
            dim ssfWINDOWS
                
            ssfWINDOWS = 36
            set objFolder = objShell.NameSpace(ssfWINDOWS)
            if (not objFolder is nothing) then
                dim objFolderItems
                        
                set objFolderItems = objFolder.Items()
                if (not objFolderItems is nothing) then
                    dim objFolderItem
                    
                    set objFolderItem = objFolderItems.Item
                        if (not objFolderItem is nothing) then
                            alert(objFolderItem.Name)
                        end if
                    set objFolderItem = nothing
                end if
                set objFolderItems = nothing
            end if
            set objFolder = nothing
        end if
        set objShell = nothing
    end function
</script>
```



<span data-ttu-id="6df97-118">Visual Basic：</span><span class="sxs-lookup"><span data-stu-id="6df97-118">Visual Basic:</span></span>


```VB
Private Sub fnFolderItemsItemVB()
    Dim objShell   As Shell
    Dim objFolder  As Folder
    Dim ssfWINDOWS As Long
    
    ssfWINDOWS = 36
    Set objShell = New Shell
    Set objFolder = objShell.NameSpace(ssfWINDOWS)
        If (Not objFolder Is Nothing) Then
            Dim objFolderItems As FolderItems
            
            Set objFolderItems = objFolder.Items
                If (Not objFolderItems Is Nothing) Then
                    Dim objFolderItem As FolderItem
                    
                    Set objFolderItem = objFolderItems.Item("NOTEPAD.EXE")
                        If (Not objFolderItem Is Nothing) Then
                            Debug.Print objFolderItem.Path
                        End If
                    Set objFolderItem = Nothing
                End If
            Set objFolderItems = Nothing
        End If
    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="6df97-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="6df97-119">Requirements</span></span>



| <span data-ttu-id="6df97-120">需求</span><span class="sxs-lookup"><span data-stu-id="6df97-120">Requirement</span></span> | <span data-ttu-id="6df97-121">值</span><span class="sxs-lookup"><span data-stu-id="6df97-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6df97-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6df97-122">Minimum supported client</span></span><br/> | <span data-ttu-id="6df97-123">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6df97-123">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="6df97-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6df97-124">Minimum supported server</span></span><br/> | <span data-ttu-id="6df97-125">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6df97-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="6df97-126">標頭</span><span class="sxs-lookup"><span data-stu-id="6df97-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="6df97-127"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="6df97-127"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="6df97-128">Idl</span><span class="sxs-lookup"><span data-stu-id="6df97-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6df97-129"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="6df97-129"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="6df97-130">DLL</span><span class="sxs-lookup"><span data-stu-id="6df97-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6df97-131"><dt>Shell32.dll (4.71 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="6df97-131"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6df97-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6df97-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6df97-133">**FolderItems**</span><span class="sxs-lookup"><span data-stu-id="6df97-133">**FolderItems**</span></span>](folderitems.md)
</dt> </dl>

 

 




