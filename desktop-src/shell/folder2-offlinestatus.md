---
description: 包含資料夾的離線狀態。
ms.assetid: b50b130d-0675-49b5-b730-f67ea1c71d8c
title: 'Folder2. OfflineStatus 屬性 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder2.OfflineStatus
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: d456eae826e8a2e173b92fac4be716fb24bcb92d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104971908"
---
# <a name="folder2offlinestatus-property"></a><span data-ttu-id="53f22-103">Folder2. OfflineStatus 屬性</span><span class="sxs-lookup"><span data-stu-id="53f22-103">Folder2.OfflineStatus property</span></span>

<span data-ttu-id="53f22-104">包含資料夾的離線狀態。</span><span class="sxs-lookup"><span data-stu-id="53f22-104">Contains the offline status of the folder.</span></span>

<span data-ttu-id="53f22-105">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="53f22-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="53f22-106">語法</span><span class="sxs-lookup"><span data-stu-id="53f22-106">Syntax</span></span>


```JScript
iOfflineStatus = Folder2.OfflineStatus
```



## <a name="property-value"></a><span data-ttu-id="53f22-107">屬性值</span><span class="sxs-lookup"><span data-stu-id="53f22-107">Property value</span></span>

<span data-ttu-id="53f22-108">設定為下列其中一個值的 **整數** 。</span><span class="sxs-lookup"><span data-stu-id="53f22-108">An **Integer** that is set to one of the following values.</span></span>

<dt>



 <span data-ttu-id="53f22-109"> (.OFS \_ DIRTYCACHE) </span><span class="sxs-lookup"><span data-stu-id="53f22-109">(OFS\_DIRTYCACHE)</span></span>


</dt> <dd>

<span data-ttu-id="53f22-110">伺服器在線上，有未同步處理的變更。</span><span class="sxs-lookup"><span data-stu-id="53f22-110">Server is online with unsynchronized changes.</span></span>

</dd> <dt>



 <span data-ttu-id="53f22-111"> (.OFS \_ 非使用中) </span><span class="sxs-lookup"><span data-stu-id="53f22-111">(OFS\_INACTIVE)</span></span>


</dt> <dd>

<span data-ttu-id="53f22-112">未啟用此資料夾的離線快取。</span><span class="sxs-lookup"><span data-stu-id="53f22-112">Offline caching is not enabled for this folder.</span></span>

</dd> <dt>



 <span data-ttu-id="53f22-113"> (.OFS \_ 離線) </span><span class="sxs-lookup"><span data-stu-id="53f22-113">(OFS\_OFFLINE)</span></span>


</dt> <dd>

<span data-ttu-id="53f22-114">伺服器已離線。</span><span class="sxs-lookup"><span data-stu-id="53f22-114">Server is offline.</span></span>

</dd> <dt>



 <span data-ttu-id="53f22-115"> (.OFS \_ ONLINE) </span><span class="sxs-lookup"><span data-stu-id="53f22-115">(OFS\_ONLINE)</span></span>


</dt> <dd>

<span data-ttu-id="53f22-116">伺服器在線上。</span><span class="sxs-lookup"><span data-stu-id="53f22-116">Server is online.</span></span>

</dd> <dt>



 <span data-ttu-id="53f22-117"> (.OFS \_ SERVERBACK) </span><span class="sxs-lookup"><span data-stu-id="53f22-117">(OFS\_SERVERBACK)</span></span>


</dt> <dd>

<span data-ttu-id="53f22-118">伺服器已離線，但可達到。</span><span class="sxs-lookup"><span data-stu-id="53f22-118">Server is offline but can be reached.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="53f22-119">備註</span><span class="sxs-lookup"><span data-stu-id="53f22-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="53f22-120">離線檔案必須透過資料夾選項啟用， **OfflineStatus** 才能正確運作。</span><span class="sxs-lookup"><span data-stu-id="53f22-120">Offline Files must be enabled through Folder Options for **OfflineStatus** to work correctly.</span></span> <span data-ttu-id="53f22-121">如果未啟用離線檔案選項，屬性會傳回 **\_ 非** 使用中的 .ofs。</span><span class="sxs-lookup"><span data-stu-id="53f22-121">If the Offline Files option is not enabled, the property returns **OFS\_INACTIVE**.</span></span>

 

## <a name="examples"></a><span data-ttu-id="53f22-122">範例</span><span class="sxs-lookup"><span data-stu-id="53f22-122">Examples</span></span>

<span data-ttu-id="53f22-123">下列範例示範如何適當地使用 JScript、VBScript 和 Visual Basic 的 **OfflineStatus** 。</span><span class="sxs-lookup"><span data-stu-id="53f22-123">The following example shows the proper use of **OfflineStatus** for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="53f22-124">Jscript：</span><span class="sxs-lookup"><span data-stu-id="53f22-124">JScript:</span></span>


```JScript
<script language="JScript">
    function fnOfflineStatusJ()
    {
        var objShell   = new ActiveXObject("shell.application");
        var objFolder2 = new Object;
        
        objFolder2 = objShell.NameSpace("\\\\server\\share\\folder");
        if (objFolder2 != null)
        {
            var nReturn;

            nReturn = objFolder2.OfflineStatus;
        }
    }
</script>
```



<span data-ttu-id="53f22-125">VBScript</span><span class="sxs-lookup"><span data-stu-id="53f22-125">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnOfflineStatusVB()
        dim objShell
        dim objFolder2
       
        set objShell = CreateObject("shell.application")
        set objFolder2 = objShell.NameSpace("\\server\share\folder")

        if (not objFolder2 is nothing) then
            dim nReturn

            nReturn = objFolder2.OfflineStatus
        end if

        set objFolder = nothing
        set objShell = nothing
    end function
</script>
```



<span data-ttu-id="53f22-126">Visual Basic：</span><span class="sxs-lookup"><span data-stu-id="53f22-126">Visual Basic:</span></span>


```VB
Private Sub fnOfflineStatusVB()
    Dim objShell   As Shell
    Dim objFolder2 As Folder2
    
    Set objShell = New Shell
    Set objFolder2 = objShell.NameSpace("\\server\share\folder")

    If (Not objFolder2 Is Nothing) Then
        Dim nReturn As Integer
        
        nReturn = objFolder2.OfflineStatus()
    End If

    Set objFolder2 = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="53f22-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="53f22-127">Requirements</span></span>



| <span data-ttu-id="53f22-128">需求</span><span class="sxs-lookup"><span data-stu-id="53f22-128">Requirement</span></span> | <span data-ttu-id="53f22-129">值</span><span class="sxs-lookup"><span data-stu-id="53f22-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="53f22-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="53f22-130">Minimum supported client</span></span><br/> | <span data-ttu-id="53f22-131">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="53f22-131">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="53f22-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="53f22-132">Minimum supported server</span></span><br/> | <span data-ttu-id="53f22-133">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="53f22-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="53f22-134">標頭</span><span class="sxs-lookup"><span data-stu-id="53f22-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="53f22-135"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="53f22-135"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="53f22-136">Idl</span><span class="sxs-lookup"><span data-stu-id="53f22-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="53f22-137"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="53f22-137"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="53f22-138">DLL</span><span class="sxs-lookup"><span data-stu-id="53f22-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="53f22-139"><dt>Shell32.dll (5.0 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="53f22-139"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53f22-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="53f22-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53f22-141">**Folder2**</span><span class="sxs-lookup"><span data-stu-id="53f22-141">**Folder2**</span></span>](folder2-object.md)
</dt> <dt>

[<span data-ttu-id="53f22-142">**資料夾**</span><span class="sxs-lookup"><span data-stu-id="53f22-142">**Folder**</span></span>](folder.md)
</dt> </dl>

 

 




