---
description: 在專案上執行動詞。
ms.assetid: 569bdc88-15ef-4d08-923c-4f41e5ae5a38
title: 'FolderItem. InvokeVerb 方法 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItem.InvokeVerb
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 259ff9613756940d5da8a37585dbf39fb2dc0a26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510781"
---
# <a name="folderiteminvokeverb-method"></a><span data-ttu-id="bcf9e-103">FolderItem. InvokeVerb 方法</span><span class="sxs-lookup"><span data-stu-id="bcf9e-103">FolderItem.InvokeVerb method</span></span>

<span data-ttu-id="bcf9e-104">在專案上執行動詞。</span><span class="sxs-lookup"><span data-stu-id="bcf9e-104">Executes a verb on the item.</span></span>

## <a name="syntax"></a><span data-ttu-id="bcf9e-105">語法</span><span class="sxs-lookup"><span data-stu-id="bcf9e-105">Syntax</span></span>


```JScript
FolderItem.InvokeVerb(
  [ vVerb ]
)
```



## <a name="parameters"></a><span data-ttu-id="bcf9e-106">參數</span><span class="sxs-lookup"><span data-stu-id="bcf9e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bcf9e-107">*vVerb* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="bcf9e-107">*vVerb* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="bcf9e-108">類型： **Variant**</span><span class="sxs-lookup"><span data-stu-id="bcf9e-108">Type: **Variant**</span></span>

<span data-ttu-id="bcf9e-109">字串，指定要執行的動詞。</span><span class="sxs-lookup"><span data-stu-id="bcf9e-109">A string that specifies the verb to be executed.</span></span> <span data-ttu-id="bcf9e-110">它必須是專案的 [**FolderItemVerb.Name**](folderitemverb-name.md) 屬性所傳回的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="bcf9e-110">It must be one of the values returned by the item's [**FolderItemVerb.Name**](folderitemverb-name.md) property.</span></span> <span data-ttu-id="bcf9e-111">如果未指定任何動詞，將會叫用預設動詞。</span><span class="sxs-lookup"><span data-stu-id="bcf9e-111">If no verb is specified, the default verb will be invoked.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bcf9e-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="bcf9e-112">Return value</span></span>

<span data-ttu-id="bcf9e-113">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="bcf9e-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="bcf9e-114">備註</span><span class="sxs-lookup"><span data-stu-id="bcf9e-114">Remarks</span></span>

<span data-ttu-id="bcf9e-115">動詞命令是用來指定專案所支援之特定動作的字串。</span><span class="sxs-lookup"><span data-stu-id="bcf9e-115">A verb is a string used to specify a particular action that an item supports.</span></span> <span data-ttu-id="bcf9e-116">叫用動詞相當於從專案的快捷方式功能表中選取命令。</span><span class="sxs-lookup"><span data-stu-id="bcf9e-116">Invoking a verb is equivalent to selecting a command from an item's shortcut menu.</span></span> <span data-ttu-id="bcf9e-117">一般來說，叫用動詞會啟動相關的應用程式。</span><span class="sxs-lookup"><span data-stu-id="bcf9e-117">Typically, invoking a verb launches a related application.</span></span> <span data-ttu-id="bcf9e-118">例如，在 .txt 檔案上叫用 "open" 動詞命令會以文字編輯器（通常是 Microsoft 記事本）開啟檔案。</span><span class="sxs-lookup"><span data-stu-id="bcf9e-118">For example, invoking the "open" verb on a .txt file opens the file with a text editor, usually Microsoft Notepad.</span></span> <span data-ttu-id="bcf9e-119">請參閱 [啟動應用程式](launch.md) ，以進一步討論動詞。</span><span class="sxs-lookup"><span data-stu-id="bcf9e-119">See [Launching Applications](launch.md) for further discussion of verbs.</span></span>

<span data-ttu-id="bcf9e-120">[**FolderItemVerbs**](folderitemverbs.md)物件表示與專案相關聯的動詞集合。</span><span class="sxs-lookup"><span data-stu-id="bcf9e-120">The [**FolderItemVerbs**](folderitemverbs.md) object represents the collection of verbs associated with the item.</span></span> <span data-ttu-id="bcf9e-121">不同的專案預設動詞命令可能會有所不同，但通常為 "open"。</span><span class="sxs-lookup"><span data-stu-id="bcf9e-121">The default verb may vary for different items, but it is typically "open".</span></span>

## <a name="examples"></a><span data-ttu-id="bcf9e-122">範例</span><span class="sxs-lookup"><span data-stu-id="bcf9e-122">Examples</span></span>

<span data-ttu-id="bcf9e-123">下列範例會使用 **InvokeVerb** 來叫用預設動詞 ( 「開啟」，在此案例中) 在 Windows 資料夾上。</span><span class="sxs-lookup"><span data-stu-id="bcf9e-123">The following example uses **InvokeVerb** to invoke the default verb ("open" in this case) on the Windows folder.</span></span> <span data-ttu-id="bcf9e-124">JScript、VBScript 和 Visual Basic 會顯示適當的使用方式。</span><span class="sxs-lookup"><span data-stu-id="bcf9e-124">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="bcf9e-125">Jscript：</span><span class="sxs-lookup"><span data-stu-id="bcf9e-125">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFolderItemInvokeVerbJ()
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
                
                objFolderItem.InvokeVerb();
            }
        }
    }
</script>
```



<span data-ttu-id="bcf9e-126">VBScript</span><span class="sxs-lookup"><span data-stu-id="bcf9e-126">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnFolderItemInvokeVerbVB()
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
                                
                    objFolderItem.InvokeVerb()
                end if
                set objFolderItem = nothing
            end if
            set objFolder2 = nothing
        end if
        set objShell = nothing
    end function
</script>
```



<span data-ttu-id="bcf9e-127">Visual Basic：</span><span class="sxs-lookup"><span data-stu-id="bcf9e-127">Visual Basic:</span></span>


```VB
Private Sub fnFolderItemInvokeVerbVB()
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
                    
                    objFolderItem.InvokeVerb
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



## <a name="requirements"></a><span data-ttu-id="bcf9e-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="bcf9e-128">Requirements</span></span>



| <span data-ttu-id="bcf9e-129">需求</span><span class="sxs-lookup"><span data-stu-id="bcf9e-129">Requirement</span></span> | <span data-ttu-id="bcf9e-130">值</span><span class="sxs-lookup"><span data-stu-id="bcf9e-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bcf9e-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bcf9e-131">Minimum supported client</span></span><br/> | <span data-ttu-id="bcf9e-132">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bcf9e-132">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="bcf9e-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bcf9e-133">Minimum supported server</span></span><br/> | <span data-ttu-id="bcf9e-134">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bcf9e-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="bcf9e-135">標頭</span><span class="sxs-lookup"><span data-stu-id="bcf9e-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="bcf9e-136"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="bcf9e-136"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="bcf9e-137">Idl</span><span class="sxs-lookup"><span data-stu-id="bcf9e-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="bcf9e-138"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="bcf9e-138"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="bcf9e-139">DLL</span><span class="sxs-lookup"><span data-stu-id="bcf9e-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bcf9e-140"><dt>Shell32.dll (4.71 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="bcf9e-140"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bcf9e-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bcf9e-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bcf9e-142">**FolderItem**</span><span class="sxs-lookup"><span data-stu-id="bcf9e-142">**FolderItem**</span></span>](folderitem.md)
</dt> <dt>

[<span data-ttu-id="bcf9e-143">**動詞**</span><span class="sxs-lookup"><span data-stu-id="bcf9e-143">**Verbs**</span></span>](folderitem-verbs.md)
</dt> <dt>

[<span data-ttu-id="bcf9e-144">**Doit r**</span><span class="sxs-lookup"><span data-stu-id="bcf9e-144">**DoIt**</span></span>](folderitemverb-doit.md)
</dt> </dl>

 

 




