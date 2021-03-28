---
description: 在 Shell 專案上執行動詞命令。
ms.assetid: aac3f338-6074-4b1f-9b2f-e6206db52419
title: 'ShellFolderItem. InvokeVerbEx 方法 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderItem.InvokeVerbEx
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 627c2b40869ac9c509dcd645ec259de7db118235
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972452"
---
# <a name="shellfolderiteminvokeverbex-method"></a><span data-ttu-id="7e71e-103">ShellFolderItem. InvokeVerbEx 方法</span><span class="sxs-lookup"><span data-stu-id="7e71e-103">ShellFolderItem.InvokeVerbEx method</span></span>

<span data-ttu-id="7e71e-104">在 Shell 專案上執行動詞命令。</span><span class="sxs-lookup"><span data-stu-id="7e71e-104">Executes a verb on a Shell item.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e71e-105">語法</span><span class="sxs-lookup"><span data-stu-id="7e71e-105">Syntax</span></span>


```JScript
iRetVal = ShellFolderItem.InvokeVerbEx(
  [ vVerb ],
  [ vArgs ]
)
```



## <a name="parameters"></a><span data-ttu-id="7e71e-106">參數</span><span class="sxs-lookup"><span data-stu-id="7e71e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7e71e-107">*vVerb* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="7e71e-107">*vVerb* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7e71e-108">類型： **Variant**</span><span class="sxs-lookup"><span data-stu-id="7e71e-108">Type: **Variant**</span></span>

<span data-ttu-id="7e71e-109">**Variant** ，包含對應至要執行之命令的動詞字串。</span><span class="sxs-lookup"><span data-stu-id="7e71e-109">A **Variant** that contains the verb string that corresponds to the command to be executed.</span></span> <span data-ttu-id="7e71e-110">它必須是專案的 [**Name**](folderitemverb-name.md) 屬性所傳回的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="7e71e-110">It must be one of the values returned by the item's [**Name**](folderitemverb-name.md) property.</span></span> <span data-ttu-id="7e71e-111">如果未指定任何動詞，則會執行預設的動詞命令。</span><span class="sxs-lookup"><span data-stu-id="7e71e-111">If no verb is specified, the default verb is executed.</span></span>

</dd> <dt>

<span data-ttu-id="7e71e-112">*vArgs* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="7e71e-112">*vArgs* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7e71e-113">類型： **Variant**</span><span class="sxs-lookup"><span data-stu-id="7e71e-113">Type: **Variant**</span></span>

<span data-ttu-id="7e71e-114">由 *vVerb* 所指定之命令具有一個或多個引數的字串所組成的 **Variant** 。</span><span class="sxs-lookup"><span data-stu-id="7e71e-114">A **Variant** that consists of a string with one or more arguments to the command specified by *vVerb*.</span></span> <span data-ttu-id="7e71e-115">這個字串的格式取決於特定的動詞。</span><span class="sxs-lookup"><span data-stu-id="7e71e-115">The format of this string depends on the particular verb.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7e71e-116">備註</span><span class="sxs-lookup"><span data-stu-id="7e71e-116">Remarks</span></span>

<span data-ttu-id="7e71e-117">動詞命令是用來指定專案所支援之特定動作的字串。</span><span class="sxs-lookup"><span data-stu-id="7e71e-117">A verb is a string used to specify a particular action that an item supports.</span></span> <span data-ttu-id="7e71e-118">一般來說，呼叫動詞會啟動相關的應用程式。</span><span class="sxs-lookup"><span data-stu-id="7e71e-118">Typically, calling a verb launches a related application.</span></span> <span data-ttu-id="7e71e-119">例如，呼叫 .txt 檔案上的 **open** 動詞通常會以文字編輯器（通常是 Microsoft 記事本）開啟檔案。</span><span class="sxs-lookup"><span data-stu-id="7e71e-119">For example, calling the **open** verb on a .txt file normally opens the file with a text editor, usually Microsoft Notepad.</span></span> <span data-ttu-id="7e71e-120">[**FolderItemVerbs**](folderitemverbs.md)物件表示與專案相關聯的動詞集合。</span><span class="sxs-lookup"><span data-stu-id="7e71e-120">The [**FolderItemVerbs**](folderitemverbs.md) object represents the collection of verbs associated with the item.</span></span> <span data-ttu-id="7e71e-121">如需動詞的進一步討論，請參閱 [啟動應用程式](launch.md)。</span><span class="sxs-lookup"><span data-stu-id="7e71e-121">For further discussion of verbs, see [Launching Applications](launch.md).</span></span>

<span data-ttu-id="7e71e-122">這個方法類似于 [**InvokeVerb**](folderitem-invokeverb.md)，但它可讓您指定命令的引數以及命令本身。</span><span class="sxs-lookup"><span data-stu-id="7e71e-122">This method is similar to [**InvokeVerb**](folderitem-invokeverb.md), but it allows you to specify arguments to the command as well as the command itself.</span></span>

## <a name="examples"></a><span data-ttu-id="7e71e-123">範例</span><span class="sxs-lookup"><span data-stu-id="7e71e-123">Examples</span></span>

<span data-ttu-id="7e71e-124">下列範例示範如何在 JScript、VBScript 和 Visual Basic 中正確使用這個方法。</span><span class="sxs-lookup"><span data-stu-id="7e71e-124">The following examples show the proper use of this method in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="7e71e-125">Jscript：</span><span class="sxs-lookup"><span data-stu-id="7e71e-125">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFolderItem2InvokeVerbExJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder2;
        var ssfWINDOWS = 36;
        
        objFolder2 = objShell.NameSpace(ssfWINDOWS);
        if (objFolder2 != null)
        {
            var objFolderItem;
            
            objFolderItem = objFolder2.ParseName("NOTEPAD.EXE");
            if (objFolderItem != null)
            {
                objFolderItem.InvokeVerbEx("open", "c:\\autoexec.bat");
            }
        }
    }
</script>
```



<span data-ttu-id="7e71e-126">VBScript</span><span class="sxs-lookup"><span data-stu-id="7e71e-126">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnFolderItemInvokeVerbExVB()
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
                    objFolderItem.InvokeVerbEx()
                end if
                set objFolderItem = nothing
            end if
            set objFolder2 = nothing
        end if
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="7e71e-127">Visual Basic：</span><span class="sxs-lookup"><span data-stu-id="7e71e-127">Visual Basic:</span></span>


```VB
Private Sub fnFolderItem2InvokeVerbExVB()
    Dim objShell   As Shell
    Dim objFolder2 As Folder2
    Dim ssfWINDOWS As Long
    
    ssfWINDOWS = 36
    Set objShell = New Shell
    Set objFolder2 = objShell.NameSpace(ssfWINDOWS)
        If (Not objFolder2 Is Nothing) Then
            Dim objFolderItem2 As Object
            
            Set objFolderItem2 = objFolder2.ParseName("NOTEPAD.EXE")
                If (Not objFolderItem2 Is Nothing) Then
                    objFolderItem2.InvokeVerbEx ("open")
                Else
                    'FolderItem object returned nothing.
                End If
            Set objFolderItem2 = Nothing
        Else
            'Folder object returned nothing.
        End If
    Set objFolder2 = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="7e71e-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="7e71e-128">Requirements</span></span>



| <span data-ttu-id="7e71e-129">需求</span><span class="sxs-lookup"><span data-stu-id="7e71e-129">Requirement</span></span> | <span data-ttu-id="7e71e-130">值</span><span class="sxs-lookup"><span data-stu-id="7e71e-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e71e-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7e71e-131">Minimum supported client</span></span><br/> | <span data-ttu-id="7e71e-132">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7e71e-132">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7e71e-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7e71e-133">Minimum supported server</span></span><br/> | <span data-ttu-id="7e71e-134">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7e71e-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="7e71e-135">標頭</span><span class="sxs-lookup"><span data-stu-id="7e71e-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="7e71e-136"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="7e71e-136"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="7e71e-137">Idl</span><span class="sxs-lookup"><span data-stu-id="7e71e-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7e71e-138"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="7e71e-138"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="7e71e-139">DLL</span><span class="sxs-lookup"><span data-stu-id="7e71e-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7e71e-140"><dt>Shell32.dll (5.0 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="7e71e-140"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7e71e-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7e71e-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e71e-142">**ShellFolderItem**</span><span class="sxs-lookup"><span data-stu-id="7e71e-142">**ShellFolderItem**</span></span>](shellfolderitem-object.md)
</dt> <dt>

[<span data-ttu-id="7e71e-143">**InvokeVerb**</span><span class="sxs-lookup"><span data-stu-id="7e71e-143">**InvokeVerb**</span></span>](folderitem-invokeverb.md)
</dt> </dl>

 

 




