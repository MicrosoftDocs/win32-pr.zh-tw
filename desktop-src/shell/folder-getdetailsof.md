---
description: 抓取資料夾中專案的詳細資料。 例如，其大小、類型或上次修改的時間。
ms.assetid: d2fe4550-f171-40d9-8bce-065b61826997
title: 'GetDetailsOf 方法 (Shlobj.h \_ core .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder.GetDetailsOf
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 3ab89f00f254778a2417644d894f1e9e81eb43cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936551"
---
# <a name="foldergetdetailsof-method"></a><span data-ttu-id="32f4c-104">GetDetailsOf 方法</span><span class="sxs-lookup"><span data-stu-id="32f4c-104">Folder.GetDetailsOf method</span></span>

<span data-ttu-id="32f4c-105">抓取資料夾中專案的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="32f4c-105">Retrieves details about an item in a folder.</span></span> <span data-ttu-id="32f4c-106">例如，其大小、類型或上次修改的時間。</span><span class="sxs-lookup"><span data-stu-id="32f4c-106">For example, its size, type, or the time of its last modification.</span></span>

## <a name="syntax"></a><span data-ttu-id="32f4c-107">語法</span><span class="sxs-lookup"><span data-stu-id="32f4c-107">Syntax</span></span>


```JScript
retVal = Folder.GetDetailsOf(
  vItem,
  iColumn
)
```



## <a name="parameters"></a><span data-ttu-id="32f4c-108">參數</span><span class="sxs-lookup"><span data-stu-id="32f4c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32f4c-109">*vItem*</span><span class="sxs-lookup"><span data-stu-id="32f4c-109">*vItem*</span></span> 
</dt> <dd>

<span data-ttu-id="32f4c-110">類型： **Variant**</span><span class="sxs-lookup"><span data-stu-id="32f4c-110">Type: **Variant**</span></span>

<span data-ttu-id="32f4c-111">要取得其資訊的專案。</span><span class="sxs-lookup"><span data-stu-id="32f4c-111">The item for which to retrieve the information.</span></span> <span data-ttu-id="32f4c-112">這必須是 [**FolderItem**](folderitem.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="32f4c-112">This must be a [**FolderItem**](folderitem.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="32f4c-113">*iColumn*</span><span class="sxs-lookup"><span data-stu-id="32f4c-113">*iColumn*</span></span> 
</dt> <dd>

<span data-ttu-id="32f4c-114">類型： **整數**</span><span class="sxs-lookup"><span data-stu-id="32f4c-114">Type: **Integer**</span></span>

<span data-ttu-id="32f4c-115">**整數** 值，指定要取出的資訊。</span><span class="sxs-lookup"><span data-stu-id="32f4c-115">An **Integer** value that specifies the information to be retrieved.</span></span> <span data-ttu-id="32f4c-116">專案的可用資訊取決於顯示它的資料夾。</span><span class="sxs-lookup"><span data-stu-id="32f4c-116">The information available for an item depends on the folder in which it is displayed.</span></span> <span data-ttu-id="32f4c-117">此值會對應至顯示在 Shell 視圖中以零為基底的資料行編號。</span><span class="sxs-lookup"><span data-stu-id="32f4c-117">This value corresponds to the zero-based column number that is displayed in a Shell view.</span></span> <span data-ttu-id="32f4c-118">針對檔案系統中的專案，這可以是下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="32f4c-118">For an item in the file system, this can be one of the following values:</span></span>

<dt>



 <span data-ttu-id="32f4c-119"> (0)</span><span class="sxs-lookup"><span data-stu-id="32f4c-119">(0)</span></span>


</dt> <dd>

<span data-ttu-id="32f4c-120">抓取專案的名稱。</span><span class="sxs-lookup"><span data-stu-id="32f4c-120">Retrieves the name of the item.</span></span>

</dd> <dt>



 <span data-ttu-id="32f4c-121">(1)</span><span class="sxs-lookup"><span data-stu-id="32f4c-121">(1)</span></span>


</dt> <dd>

<span data-ttu-id="32f4c-122">捕獲專案的大小。</span><span class="sxs-lookup"><span data-stu-id="32f4c-122">Retrieves the size of the item.</span></span>

</dd> <dt>



 <span data-ttu-id="32f4c-123">(2)</span><span class="sxs-lookup"><span data-stu-id="32f4c-123">(2)</span></span>


</dt> <dd>

<span data-ttu-id="32f4c-124">抓取專案的型別。</span><span class="sxs-lookup"><span data-stu-id="32f4c-124">Retrieves the type of the item.</span></span>

</dd> <dt>



 <span data-ttu-id="32f4c-125">(3)</span><span class="sxs-lookup"><span data-stu-id="32f4c-125">(3)</span></span>


</dt> <dd>

<span data-ttu-id="32f4c-126">抓取專案上次修改的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="32f4c-126">Retrieves the date and time that the item was last modified.</span></span>

</dd> <dt>



 <span data-ttu-id="32f4c-127">(4)</span><span class="sxs-lookup"><span data-stu-id="32f4c-127">(4)</span></span>


</dt> <dd>

<span data-ttu-id="32f4c-128">抓取專案的屬性。</span><span class="sxs-lookup"><span data-stu-id="32f4c-128">Retrieves the attributes of the item.</span></span>

</dd> <dt>



 <span data-ttu-id="32f4c-129"> (-1) </span><span class="sxs-lookup"><span data-stu-id="32f4c-129">(-1)</span></span>


</dt> <dd>

<span data-ttu-id="32f4c-130">抓取專案的資訊提示資訊。</span><span class="sxs-lookup"><span data-stu-id="32f4c-130">Retrieves the info tip information for the item.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="32f4c-131">傳回值</span><span class="sxs-lookup"><span data-stu-id="32f4c-131">Return value</span></span>

<span data-ttu-id="32f4c-132">類型： \**[**BSTR**](/previous-versions/windows/desktop/automat/bstr) \** _</span><span class="sxs-lookup"><span data-stu-id="32f4c-132">Type: \**[**BSTR**](/previous-versions/windows/desktop/automat/bstr)\** _</span></span>

<span data-ttu-id="32f4c-133">包含已抓取詳細資料的字串。</span><span class="sxs-lookup"><span data-stu-id="32f4c-133">String containing the retrieved detail.</span></span>

## <a name="remarks"></a><span data-ttu-id="32f4c-134">備註</span><span class="sxs-lookup"><span data-stu-id="32f4c-134">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="32f4c-135">並非所有的方法都會針對所有資料夾執行。</span><span class="sxs-lookup"><span data-stu-id="32f4c-135">Not all methods are implemented for all folders.</span></span> <span data-ttu-id="32f4c-136">例如， [_ *ParseName* \*](folder-parsename.md)方法不會針對主控台資料夾執行， (CSIDL \_ 控制項) 。</span><span class="sxs-lookup"><span data-stu-id="32f4c-136">For example, the [_ *ParseName*\*](folder-parsename.md) method is not implemented for the Control Panel folder (CSIDL\_CONTROLS).</span></span> <span data-ttu-id="32f4c-137">如果您嘗試呼叫未產生的方法，則會引發 0x800A01BD (decimal 445) 錯誤。</span><span class="sxs-lookup"><span data-stu-id="32f4c-137">If you attempt to call an unimplemented method, a 0x800A01BD (decimal 445) error is raised.</span></span>

 

## <a name="examples"></a><span data-ttu-id="32f4c-138">範例</span><span class="sxs-lookup"><span data-stu-id="32f4c-138">Examples</span></span>

<span data-ttu-id="32f4c-139">下列範例會使用 **GetDetailsOf** 來取出名為 Clock.avi 之檔案的類型。</span><span class="sxs-lookup"><span data-stu-id="32f4c-139">The following example uses **GetDetailsOf** to retrieve the type of the file named Clock.avi.</span></span> <span data-ttu-id="32f4c-140">JScript、VBScript 和 Visual Basic 會顯示適當的使用方式。</span><span class="sxs-lookup"><span data-stu-id="32f4c-140">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="32f4c-141">Jscript：</span><span class="sxs-lookup"><span data-stu-id="32f4c-141">JScript:</span></span>


```JScript
<script language="JScript">
    function fnGetDetailsOfJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder = new Object;
        
        objFolder = objShell.NameSpace("C:\\WINDOWS");
        if (objFolder != null)
        {
            var objFolderItem = new Object;

            objFolderItem = objFolder.ParseName("clock.avi");
            if (objFolderItem != null)
            {
                var objInfo = new Object;

                objInfo = objFolder.GetDetailsOf(objFolderItem, 2);
            }
        }
    }
</script>
```



<span data-ttu-id="32f4c-142">VBScript</span><span class="sxs-lookup"><span data-stu-id="32f4c-142">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnGetDetailsOfVB()
        dim objShell
        dim objFolder
        
        set objShell = CreateObject("shell.application")
        set objFolder = objShell.NameSpace("C:\WINDOWS")

        if (not objFolder is nothing) then
            dim objFolderItem

            set objFolderItem = objFolder.ParseName("clock.avi")

            if (not objFolderItem Is Nothing) then
                dim objInfo
                        
                objInfo = objFolder.GetDetailsOf(objFolderItem, 2)
            end if
            
            set objFolderItem = nothing
        end if
        
        set objFolder = nothing
        set objShell = nothing
    end function
</script>
```



<span data-ttu-id="32f4c-143">Visual Basic：</span><span class="sxs-lookup"><span data-stu-id="32f4c-143">Visual Basic:</span></span>


```VB
Private Sub btnGetDetailsOf_Click()
    Dim objShell  As Shell
    Dim objFolder As Folder

    Set objShell = New Shell
    Set objFolder = objShell.NameSpace("C:\WINDOWS")
    
    If (Not objFolder Is Nothing) Then
        Dim objFolderItem As FolderItem
        Set objFolderItem = objFolder.ParseName("clock.avi")
   
        If (Not objFolderItem Is Nothing) Then
            Dim szItem As String
            szItem = objFolder.GetDetailsOf(objFolderItem, 2)
        End If
        
        Set objFolderItem = Nothing
    End If
    
    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="32f4c-144">規格需求</span><span class="sxs-lookup"><span data-stu-id="32f4c-144">Requirements</span></span>



| <span data-ttu-id="32f4c-145">需求</span><span class="sxs-lookup"><span data-stu-id="32f4c-145">Requirement</span></span> | <span data-ttu-id="32f4c-146">值</span><span class="sxs-lookup"><span data-stu-id="32f4c-146">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="32f4c-147">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="32f4c-147">Minimum supported client</span></span><br/> | <span data-ttu-id="32f4c-148">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="32f4c-148">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="32f4c-149">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="32f4c-149">Minimum supported server</span></span><br/> | <span data-ttu-id="32f4c-150">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="32f4c-150">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="32f4c-151">標頭</span><span class="sxs-lookup"><span data-stu-id="32f4c-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="32f4c-152"><dt>Shlobj.h \_ core .h (包括 Shldisp) </dt></span><span class="sxs-lookup"><span data-stu-id="32f4c-152"><dt>Shlobj\_core.h (include Shldisp.h)</dt></span></span> </dl>  |
| <span data-ttu-id="32f4c-153">Idl</span><span class="sxs-lookup"><span data-stu-id="32f4c-153">IDL</span></span><br/>                      | <dl> <span data-ttu-id="32f4c-154"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="32f4c-154"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="32f4c-155">DLL</span><span class="sxs-lookup"><span data-stu-id="32f4c-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="32f4c-156"><dt>Shell32.dll (4.71 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="32f4c-156"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
