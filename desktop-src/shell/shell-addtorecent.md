---
description: 將檔案加入最近使用的 (MRU) 清單中。
ms.assetid: 26D2AE5A-FC7E-4c7c-9F10-8D3D7AA236E7
title: 'AddToRecent 方法 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.AddToRecent
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: c4372cc6cfac25f94e607f14734a9f544cd4fcbb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973776"
---
# <a name="shelladdtorecent-method"></a><span data-ttu-id="70dd2-103">AddToRecent 方法</span><span class="sxs-lookup"><span data-stu-id="70dd2-103">Shell.AddToRecent method</span></span>

<span data-ttu-id="70dd2-104">將檔案加入最近使用的 (MRU) 清單中。</span><span class="sxs-lookup"><span data-stu-id="70dd2-104">Adds a file to the most recently used (MRU) list.</span></span>

## <a name="syntax"></a><span data-ttu-id="70dd2-105">語法</span><span class="sxs-lookup"><span data-stu-id="70dd2-105">Syntax</span></span>


```JScript
Shell.AddToRecent(
  varFile,
  [ bstrCategory ]
)
```


```VB

Shell.AddToRecent( _
  ByVal varFile As Variant, _
  [ ByVal bstrCategory As BSTR ] _
)
```





## <a name="parameters"></a><span data-ttu-id="70dd2-106">參數</span><span class="sxs-lookup"><span data-stu-id="70dd2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="70dd2-107">*varFile* \[在\]</span><span class="sxs-lookup"><span data-stu-id="70dd2-107">*varFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70dd2-108">類型： **Variant**</span><span class="sxs-lookup"><span data-stu-id="70dd2-108">Type: **Variant**</span></span>

<span data-ttu-id="70dd2-109">**字串**，其中包含要新增至最近使用之檔案清單的檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="70dd2-109">A **String** that contains the path of the file to add to the list of recently used documents.</span></span>

<span data-ttu-id="70dd2-110">**Windows Vista**：將此參數設定為 **null** 以清除 [最近使用的檔] 資料夾。</span><span class="sxs-lookup"><span data-stu-id="70dd2-110">**Windows Vista**: Set this parameter to **null** to clear the recent documents folder.</span></span>

</dd> <dt>

<span data-ttu-id="70dd2-111">*bstrCategory* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="70dd2-111">*bstrCategory* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="70dd2-112">類型： **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="70dd2-112">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="70dd2-113">**字串**，其中包含要在其中放置檔案的類別目錄名稱。</span><span class="sxs-lookup"><span data-stu-id="70dd2-113">A **String** that contains the name of the category in which to place the file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="70dd2-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="70dd2-114">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="70dd2-115">JScript</span><span class="sxs-lookup"><span data-stu-id="70dd2-115">JScript</span></span>

<span data-ttu-id="70dd2-116">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="70dd2-116">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="70dd2-117">VB</span><span class="sxs-lookup"><span data-stu-id="70dd2-117">VB</span></span>

<span data-ttu-id="70dd2-118">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="70dd2-118">This method does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="70dd2-119">範例</span><span class="sxs-lookup"><span data-stu-id="70dd2-119">Examples</span></span>

<span data-ttu-id="70dd2-120">下列範例示範如何使用 JScript、VBScript 和 Visual Basic 的 **AddToRecent** 。</span><span class="sxs-lookup"><span data-stu-id="70dd2-120">The following examples show the use of **AddToRecent** for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="70dd2-121">Jscript：</span><span class="sxs-lookup"><span data-stu-id="70dd2-121">JScript:</span></span>


```JScript
<script language="JScript">
    function fnIShellDispatch3AddToRecentJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var ssfWINDOWS = 36;
        var objFolder;
        
        objFolder = objShell.NameSpace(ssfWINDOWS);
        if (objFolder != null)
        {
            var objFolderItem;
            
            objFolderItem = objFolder.ParseName("system.ini");
            if (objFolderItem != null)
            {
                objShell.AddToRecent(objFolderItem.Path);
            }
        }
    }
</script>
```



<span data-ttu-id="70dd2-122">VBScript</span><span class="sxs-lookup"><span data-stu-id="70dd2-122">VBScript:</span></span>


```VB
<script language="VBScript">
     function fnIShellDispatch3AddToRecentVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        if (not objShell is nothing) then
            dim objFolder
            dim ssfWINDOWS
            
            ssfWINDOWS = 36
            set objFolder = objShell.NameSpace(ssfWINDOWS)
            if (not objFolder is nothing) then
                dim objFolderItem
                        
                set objFolderItem = objFolder.ParseName("system.ini")
                if (not objFolderItem is nothing) then
                    objShell.AddToRecent (objFolderItem.Path)
                end if
                set objFolderItem = nothing
            end if
            set objFolder = nothing
        end if
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="70dd2-123">Visual Basic：</span><span class="sxs-lookup"><span data-stu-id="70dd2-123">Visual Basic:</span></span>


```VB
Private Sub fnIShellDispatch3AddToRecent()
    Dim objShell  As Shell
    Dim objFolder As Folder
    Dim ssfWINDOWS As Long

    ssfWINDOWS = 36
    Set objShell = New Shell
    Set objFolder = objShell.NameSpace(ssfWINDOWS)
    If (Not objFolder Is Nothing) Then
        Dim objFolderItem As FolderItem

        Set objFolderItem = objFolder.ParseName("system.ini")
        If (Not objFolderItem Is Nothing) Then
            objShell.AddToRecent (objFolderItem.Path)
        End If
        Set objFolderItem = Nothing
    End If
    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="70dd2-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="70dd2-124">Requirements</span></span>



| <span data-ttu-id="70dd2-125">需求</span><span class="sxs-lookup"><span data-stu-id="70dd2-125">Requirement</span></span> | <span data-ttu-id="70dd2-126">值</span><span class="sxs-lookup"><span data-stu-id="70dd2-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70dd2-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="70dd2-127">Minimum supported client</span></span><br/> | <span data-ttu-id="70dd2-128">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="70dd2-128">Windows XP \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="70dd2-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="70dd2-129">Minimum supported server</span></span><br/> | <span data-ttu-id="70dd2-130">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="70dd2-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="70dd2-131">標頭</span><span class="sxs-lookup"><span data-stu-id="70dd2-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="70dd2-132"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="70dd2-132"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="70dd2-133">Idl</span><span class="sxs-lookup"><span data-stu-id="70dd2-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="70dd2-134"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="70dd2-134"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="70dd2-135">DLL</span><span class="sxs-lookup"><span data-stu-id="70dd2-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="70dd2-136"><dt>Shell32.dll (6.0 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="70dd2-136"><dt>Shell32.dll (version 6.0 or later)</dt></span></span> </dl> |



 

 
