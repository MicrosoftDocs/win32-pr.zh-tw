---
description: 同步處理資料夾中的所有離線檔案。
ms.assetid: b149df96-0c8e-47b9-b71e-2ad5dcfdeb8f
title: Folder2) 同步處理方法 (Shldisp
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder2.Synchronize
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: e9c39c37ff0e44e58aa71c69496dec8bee2745bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104386020"
---
# <a name="folder2synchronize-method"></a><span data-ttu-id="3b0d0-103">Folder2 同步方法</span><span class="sxs-lookup"><span data-stu-id="3b0d0-103">Folder2.Synchronize method</span></span>

<span data-ttu-id="3b0d0-104">同步處理資料夾中的所有離線檔案。</span><span class="sxs-lookup"><span data-stu-id="3b0d0-104">Synchronizes all offline files in the folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b0d0-105">語法</span><span class="sxs-lookup"><span data-stu-id="3b0d0-105">Syntax</span></span>


```JScript
iRetVal = Folder2.Synchronize()
```



## <a name="parameters"></a><span data-ttu-id="3b0d0-106">參數</span><span class="sxs-lookup"><span data-stu-id="3b0d0-106">Parameters</span></span>

<span data-ttu-id="3b0d0-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="3b0d0-107">This method has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="3b0d0-108">備註</span><span class="sxs-lookup"><span data-stu-id="3b0d0-108">Remarks</span></span>

<span data-ttu-id="3b0d0-109">若要使用這個方法，必須啟用離線檔案功能。</span><span class="sxs-lookup"><span data-stu-id="3b0d0-109">To use this method, the Offline Files feature must be enabled.</span></span>

## <a name="examples"></a><span data-ttu-id="3b0d0-110">範例</span><span class="sxs-lookup"><span data-stu-id="3b0d0-110">Examples</span></span>

<span data-ttu-id="3b0d0-111">下列範例示範如何適當地使用 JScript、VBScript 和 Visual Basic 的 **同步處理** 。</span><span class="sxs-lookup"><span data-stu-id="3b0d0-111">The following example shows the proper use of **Synchronize** for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="3b0d0-112">Jscript：</span><span class="sxs-lookup"><span data-stu-id="3b0d0-112">JScript:</span></span>


```JScript
<script language="JScript">
    function fnSynchronizeJ()
    {
        var objShell   = new ActiveXObject("shell.application");
        var objFolder2 = new Object;
        
        objFolder2 = objShell.NameSpace("\\\\server\\share\\folder");
        if (objFolder2 != null)
        {
            objFolder2.Synchronize();
        }
    }
</script>
```



<span data-ttu-id="3b0d0-113">VBScript</span><span class="sxs-lookup"><span data-stu-id="3b0d0-113">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnSynchronizeVB()
        dim objShell
        dim objFolder2
       
        set objShell = CreateObject("shell.application")
        set objFolder2 = objShell.NameSpace("\\server\share\folder")

        if (not objFolder2 is nothing) then
            objFolder2.Synchronize
        end if

        set objFolder = nothing
        set objShell = nothing
    end function
</script>
```



<span data-ttu-id="3b0d0-114">Visual Basic：</span><span class="sxs-lookup"><span data-stu-id="3b0d0-114">Visual Basic:</span></span>


```VB
Private Sub fnSynchronizeVB()
    Dim objShell   As Shell
    Dim objFolder2 As Folder2
    
    Set objShell = New Shell
    Set objFolder2 = objShell.NameSpace("\\server\share\folder")

    If (Not objFolder2 Is Nothing) Then
        objFolder2.Synchronize
    End If

    Set objFolder2 = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="3b0d0-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="3b0d0-115">Requirements</span></span>



| <span data-ttu-id="3b0d0-116">需求</span><span class="sxs-lookup"><span data-stu-id="3b0d0-116">Requirement</span></span> | <span data-ttu-id="3b0d0-117">值</span><span class="sxs-lookup"><span data-stu-id="3b0d0-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b0d0-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3b0d0-118">Minimum supported client</span></span><br/> | <span data-ttu-id="3b0d0-119">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3b0d0-119">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3b0d0-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3b0d0-120">Minimum supported server</span></span><br/> | <span data-ttu-id="3b0d0-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3b0d0-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="3b0d0-122">標頭</span><span class="sxs-lookup"><span data-stu-id="3b0d0-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="3b0d0-123"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="3b0d0-123"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="3b0d0-124">Idl</span><span class="sxs-lookup"><span data-stu-id="3b0d0-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3b0d0-125"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="3b0d0-125"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="3b0d0-126">DLL</span><span class="sxs-lookup"><span data-stu-id="3b0d0-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3b0d0-127"><dt>Shell32.dll (5.0 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="3b0d0-127"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b0d0-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3b0d0-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b0d0-129">**Folder2**</span><span class="sxs-lookup"><span data-stu-id="3b0d0-129">**Folder2**</span></span>](folder2-object.md)
</dt> <dt>

[<span data-ttu-id="3b0d0-130">**資料夾**</span><span class="sxs-lookup"><span data-stu-id="3b0d0-130">**Folder**</span></span>](folder.md)
</dt> </dl>

 

 




