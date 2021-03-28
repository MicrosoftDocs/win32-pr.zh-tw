---
description: 尋找 Shell 連結的目標，即使目標已移動或重新命名也一樣。
ms.assetid: 60e119be-8e45-4f63-a381-cad048de0765
title: 'ShellLinkObject 方法 (Shldisp) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellLinkObject.Resolve
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: b1cb0760f1ee19acfa10208711e73919fd084ecf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973772"
---
# <a name="shelllinkobjectresolve-method"></a><span data-ttu-id="529ae-103">ShellLinkObject 方法</span><span class="sxs-lookup"><span data-stu-id="529ae-103">ShellLinkObject.Resolve method</span></span>

<span data-ttu-id="529ae-104">尋找 Shell 連結的目標，即使目標已移動或重新命名也一樣。</span><span class="sxs-lookup"><span data-stu-id="529ae-104">Looks for the target of a Shell link, even if the target has been moved or renamed.</span></span>

## <a name="syntax"></a><span data-ttu-id="529ae-105">語法</span><span class="sxs-lookup"><span data-stu-id="529ae-105">Syntax</span></span>


```JScript
iRetVal = ShellLinkObject.Resolve(
  fFlags
)
```



## <a name="parameters"></a><span data-ttu-id="529ae-106">參數</span><span class="sxs-lookup"><span data-stu-id="529ae-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="529ae-107">*fFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="529ae-107">*fFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="529ae-108">類型： **整數**</span><span class="sxs-lookup"><span data-stu-id="529ae-108">Type: **Integer**</span></span>

<span data-ttu-id="529ae-109">指定要採取之動作的旗標。</span><span class="sxs-lookup"><span data-stu-id="529ae-109">Flags that specify the action to be taken.</span></span> <span data-ttu-id="529ae-110">這可以是下列值的組合：</span><span class="sxs-lookup"><span data-stu-id="529ae-110">This can be a combination of the following values:</span></span>

<dt>



 <span data-ttu-id="529ae-111">(1)</span><span class="sxs-lookup"><span data-stu-id="529ae-111">(1)</span></span>


</dt> <dd>

<span data-ttu-id="529ae-112">如果無法解析連結，請勿顯示對話方塊。</span><span class="sxs-lookup"><span data-stu-id="529ae-112">Do not display a dialog box if the link cannot be resolved.</span></span> <span data-ttu-id="529ae-113">設定此旗標時， *fFlags* 的高序位字會指定超時時間（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="529ae-113">When this flag is set, the high-order word of *fFlags* specifies a time-out duration, in milliseconds.</span></span> <span data-ttu-id="529ae-114">如果在超時時間內無法解析連結，則此方法會傳回。</span><span class="sxs-lookup"><span data-stu-id="529ae-114">The method returns if the link cannot be resolved within the time-out duration.</span></span> <span data-ttu-id="529ae-115">如果高序位字組設定為零，則超時期間預設為3000毫秒 (3 秒) 。</span><span class="sxs-lookup"><span data-stu-id="529ae-115">If the high-order word is set to zero, the time-out duration defaults to 3000 milliseconds (3 seconds).</span></span>

</dd> <dt>



 <span data-ttu-id="529ae-116">(4)</span><span class="sxs-lookup"><span data-stu-id="529ae-116">(4)</span></span>


</dt> <dd>

<span data-ttu-id="529ae-117">如果連結已變更，請更新其路徑和識別碼清單。</span><span class="sxs-lookup"><span data-stu-id="529ae-117">If the link has changed, update its path and list of identifiers.</span></span>

</dd> <dt>



 <span data-ttu-id="529ae-118">(8)</span><span class="sxs-lookup"><span data-stu-id="529ae-118">(8)</span></span>


</dt> <dd>

<span data-ttu-id="529ae-119">請勿更新連結資訊。</span><span class="sxs-lookup"><span data-stu-id="529ae-119">Do not update the link information.</span></span>

</dd> <dt>



 <span data-ttu-id="529ae-120">(16)</span><span class="sxs-lookup"><span data-stu-id="529ae-120">(16)</span></span>


</dt> <dd>

<span data-ttu-id="529ae-121">請勿執行搜尋啟發學習法。</span><span class="sxs-lookup"><span data-stu-id="529ae-121">Do not execute the search heuristics.</span></span>

</dd> <dt>



 <span data-ttu-id="529ae-122"> (32) </span><span class="sxs-lookup"><span data-stu-id="529ae-122">(32)</span></span>


</dt> <dd>

<span data-ttu-id="529ae-123">請勿使用分散式連結追蹤。</span><span class="sxs-lookup"><span data-stu-id="529ae-123">Do not use distributed link tracking.</span></span>

</dd> <dt>



 <span data-ttu-id="529ae-124">(64)</span><span class="sxs-lookup"><span data-stu-id="529ae-124">(64)</span></span>


</dt> <dd>

<span data-ttu-id="529ae-125">停用分散式連結追蹤。</span><span class="sxs-lookup"><span data-stu-id="529ae-125">Disable distributed link tracking.</span></span> <span data-ttu-id="529ae-126">根據預設，分散式連結追蹤會根據磁片區名稱來追蹤多個裝置上的卸載式媒體。</span><span class="sxs-lookup"><span data-stu-id="529ae-126">By default, distributed link tracking tracks removable media across multiple devices based on the volume name.</span></span> <span data-ttu-id="529ae-127">它也會使用 UNC 路徑來追蹤磁碟機號已變更的遠端檔案系統。</span><span class="sxs-lookup"><span data-stu-id="529ae-127">It also uses the UNC path to track remote file systems whose drive letter has changed.</span></span> <span data-ttu-id="529ae-128">設定此旗標會停用這兩種類型的追蹤。</span><span class="sxs-lookup"><span data-stu-id="529ae-128">Setting this flag disables both types of tracking.</span></span>

</dd> <dt>



 <span data-ttu-id="529ae-129"> (128) </span><span class="sxs-lookup"><span data-stu-id="529ae-129">(128)</span></span>


</dt> <dd>

<span data-ttu-id="529ae-130">呼叫 Windows Installer。</span><span class="sxs-lookup"><span data-stu-id="529ae-130">Call the Windows Installer.</span></span>

</dd> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="529ae-131">備註</span><span class="sxs-lookup"><span data-stu-id="529ae-131">Remarks</span></span>

<span data-ttu-id="529ae-132">這個方法基本上與要 [**解析**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-resolve)的功能完全相同。</span><span class="sxs-lookup"><span data-stu-id="529ae-132">This method is essentially identical in functionality to [**Resolve**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-resolve).</span></span> <span data-ttu-id="529ae-133">如需連結解析的進一步討論，請參閱該頁面的 [備註] 區段。</span><span class="sxs-lookup"><span data-stu-id="529ae-133">For further discussion of link resolution, see the Remarks section of that page.</span></span>

## <a name="examples"></a><span data-ttu-id="529ae-134">範例</span><span class="sxs-lookup"><span data-stu-id="529ae-134">Examples</span></span>

<span data-ttu-id="529ae-135">下列範例會示範如何適當地使用此方法來進行 JScript、VBScript 和 Visual Basic。</span><span class="sxs-lookup"><span data-stu-id="529ae-135">The following example shows the proper usage of this method for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="529ae-136">Jscript：</span><span class="sxs-lookup"><span data-stu-id="529ae-136">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellLinkObjectResolveJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder;
        var ssfPROGRAMS = 2;
        
        objFolder = objShell.NameSpace(ssfPROGRAMS);
        if (objFolder != null)
        {
            var objFolderItem;
            
            objFolderItem = objFolder.ParseName("Internet Explorer.lnk");
            if (objFolderItem != null)
            {
                var objShellLink;
                
                objShellLink = objFolderItem.GetLink;
                if (objShellLink != null)
                {
                    objShellLink.Resolve(1);
                }
            }
        }
    }
</script>
```



<span data-ttu-id="529ae-137">VBScript</span><span class="sxs-lookup"><span data-stu-id="529ae-137">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellLinkObjectResolveVB()
        dim objShell
        dim objFolder
        dim ssfPROGRAMS
        
        ssfPROGRAMS = 2
        set objShell = CreateObject("shell.application")
        set objFolder = objShell.NameSpace(ssfPROGRAMS)
            if (not objFolder is nothing) then
                dim objFolderItem
                
                set objFolderItem = objFolder.ParseName("Internet Explorer.lnk")
                    if (not objFolderItem is nothing) then
                        dim objShellLink
                        
                        set objShellLink = objFolderItem.GetLink
                            if (not objShellLink is nothing) then
                                objShellLink.Resolve(1)
                            end if
                        set objShellLink = nothing
                    end if
                set objFolderItem = nothing
            end if
        set objFolder = nothing
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="529ae-138">Visual Basic：</span><span class="sxs-lookup"><span data-stu-id="529ae-138">Visual Basic:</span></span>


```VB
Private Sub fnShellLinkObjectResolveVB()
    Dim objShell  As Shell
    Dim objFolder As Folder
    
    Set objShell = New Shell
    Set objFolder = objShell.NameSpace(ssfPROGRAMS)
        If (Not objFolder Is Nothing) Then
            Dim objFolderItem As FolderItem
            
            Set objFolderItem = objFolder.ParseName("Internet Explorer.lnk")
                If (Not objFolderItem Is Nothing) Then
                    Dim objShellLink As ShellLinkObject
                    
                    Set objShellLink = objFolderItem.GetLink
                        If (Not objShellLink Is Nothing) Then
                            objShellLink.Resolve (1)
                        End If
                    Set objShellLink = Nothing
                End If
            Set objFolderItem = Nothing
        End If
    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="529ae-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="529ae-139">Requirements</span></span>



| <span data-ttu-id="529ae-140">需求</span><span class="sxs-lookup"><span data-stu-id="529ae-140">Requirement</span></span> | <span data-ttu-id="529ae-141">值</span><span class="sxs-lookup"><span data-stu-id="529ae-141">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="529ae-142">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="529ae-142">Minimum supported client</span></span><br/> | <span data-ttu-id="529ae-143">僅限 Windows 2000 Professional 含 SP3 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="529ae-143">Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="529ae-144">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="529ae-144">Minimum supported server</span></span><br/> | <span data-ttu-id="529ae-145">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="529ae-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="529ae-146">標頭</span><span class="sxs-lookup"><span data-stu-id="529ae-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="529ae-147"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="529ae-147"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="529ae-148">Idl</span><span class="sxs-lookup"><span data-stu-id="529ae-148">IDL</span></span><br/>                      | <dl> <span data-ttu-id="529ae-149"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="529ae-149"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="529ae-150">DLL</span><span class="sxs-lookup"><span data-stu-id="529ae-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="529ae-151"><dt>Shell32.dll (5.0 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="529ae-151"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
