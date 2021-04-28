---
description: IShellDispatch2. ShellExecute 方法-在指定的檔案上執行指定的作業。
ms.assetid: a55e804c-ed7c-4b22-b86f-8e5653976654
title: 'IShellDispatch2. ShellExecute 方法 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch2.ShellExecute
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 5c058275948d5d96805ae24a76389321d7c69b8e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117016"
---
# <a name="ishelldispatch2shellexecute-method"></a><span data-ttu-id="eca9b-103">IShellDispatch2. ShellExecute 方法</span><span class="sxs-lookup"><span data-stu-id="eca9b-103">IShellDispatch2.ShellExecute method</span></span>

<span data-ttu-id="eca9b-104">在指定的檔案上執行指定的作業。</span><span class="sxs-lookup"><span data-stu-id="eca9b-104">Performs a specified operation on a specified file.</span></span>

## <a name="syntax"></a><span data-ttu-id="eca9b-105">語法</span><span class="sxs-lookup"><span data-stu-id="eca9b-105">Syntax</span></span>


```JScript
iRetVal = IShellDispatch2.ShellExecute(
  sFile,
  [ vArguments ],
  [ vDirectory ],
  [ vOperation ],
  [ vShow ]
)
```


```VB

IShellDispatch2.ShellExecute( _
  ByVal sFile As BSTR, _
  [ ByVal vArguments As Variant ], _
  [ ByVal vDirectory As Variant ], _
  [ ByVal vOperation As Variant ], _
  [ ByVal vShow As Variant ] _
) As Integer
```





## <a name="parameters"></a><span data-ttu-id="eca9b-106">參數</span><span class="sxs-lookup"><span data-stu-id="eca9b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eca9b-107">*sFile* \[在\]</span><span class="sxs-lookup"><span data-stu-id="eca9b-107">*sFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eca9b-108">類型： **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="eca9b-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="eca9b-109">**字串**，其中包含 **ShellExecute** 將執行 *vOperation* 所指定之動作的檔案名。</span><span class="sxs-lookup"><span data-stu-id="eca9b-109">A **String** that contains the name of the file on which **ShellExecute** will perform the action specified by *vOperation*.</span></span>

</dd> <dt>

<span data-ttu-id="eca9b-110">*vArguments* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="eca9b-110">*vArguments* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="eca9b-111">類型： **Variant**</span><span class="sxs-lookup"><span data-stu-id="eca9b-111">Type: **Variant**</span></span>

<span data-ttu-id="eca9b-112">包含作業參數值的字串。</span><span class="sxs-lookup"><span data-stu-id="eca9b-112">A string that contains parameter values for the operation.</span></span>

</dd> <dt>

<span data-ttu-id="eca9b-113">*vDirectory* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="eca9b-113">*vDirectory* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="eca9b-114">類型： **Variant**</span><span class="sxs-lookup"><span data-stu-id="eca9b-114">Type: **Variant**</span></span>

<span data-ttu-id="eca9b-115">目錄的完整路徑，其中包含 *sFile* 所指定的檔案。</span><span class="sxs-lookup"><span data-stu-id="eca9b-115">The fully qualified path of the directory that contains the file specified by *sFile*.</span></span> <span data-ttu-id="eca9b-116">如果未指定此參數，則會使用目前的工作目錄。</span><span class="sxs-lookup"><span data-stu-id="eca9b-116">If this parameter is not specified, the current working directory is used.</span></span>

</dd> <dt>

<span data-ttu-id="eca9b-117">*vOperation* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="eca9b-117">*vOperation* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="eca9b-118">類型： **Variant**</span><span class="sxs-lookup"><span data-stu-id="eca9b-118">Type: **Variant**</span></span>

<span data-ttu-id="eca9b-119">要執行的作業。</span><span class="sxs-lookup"><span data-stu-id="eca9b-119">The operation to be performed.</span></span> <span data-ttu-id="eca9b-120">此值會設定為檔案所支援的其中一個動詞字串。</span><span class="sxs-lookup"><span data-stu-id="eca9b-120">This value is set to one of the verb strings that is supported by the file.</span></span> <span data-ttu-id="eca9b-121">如需動詞的討論，請參閱「備註」一節。</span><span class="sxs-lookup"><span data-stu-id="eca9b-121">For a discussion of verbs, see the Remarks section.</span></span> <span data-ttu-id="eca9b-122">如果未指定此參數，則會執行預設作業。</span><span class="sxs-lookup"><span data-stu-id="eca9b-122">If this parameter is not specified, the default operation is performed.</span></span>

</dd> <dt>

<span data-ttu-id="eca9b-123">*vShow* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="eca9b-123">*vShow* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="eca9b-124">類型： **Variant**</span><span class="sxs-lookup"><span data-stu-id="eca9b-124">Type: **Variant**</span></span>

<span data-ttu-id="eca9b-125">一開始應該如何顯示應用程式視窗的建議。</span><span class="sxs-lookup"><span data-stu-id="eca9b-125">A recommendation as to how the application window should be displayed initially.</span></span> <span data-ttu-id="eca9b-126">應用程式可以忽略此建議。</span><span class="sxs-lookup"><span data-stu-id="eca9b-126">The application can ignore this recommendation.</span></span> <span data-ttu-id="eca9b-127">此參數可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="eca9b-127">This parameter can be one of the following values.</span></span> <span data-ttu-id="eca9b-128">如果未指定此參數，應用程式會使用其預設值。</span><span class="sxs-lookup"><span data-stu-id="eca9b-128">If this parameter is not specified, the application uses its default value.</span></span>



| <span data-ttu-id="eca9b-129">值</span><span class="sxs-lookup"><span data-stu-id="eca9b-129">Value</span></span>                                                                                                                               | <span data-ttu-id="eca9b-130">意義</span><span class="sxs-lookup"><span data-stu-id="eca9b-130">Meaning</span></span>                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="eca9b-131"><dt></dt><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="eca9b-131"><dt></dt> <dt>0</dt></span></span> </dl>  | <span data-ttu-id="eca9b-132">使用隱藏視窗開啟應用程式。</span><span class="sxs-lookup"><span data-stu-id="eca9b-132">Open the application with a hidden window.</span></span><br/>                                                                                                    |
| <dl> <span data-ttu-id="eca9b-133"><dt></dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="eca9b-133"><dt></dt> <dt>1</dt></span></span> </dl>  | <span data-ttu-id="eca9b-134">使用一般視窗開啟應用程式。</span><span class="sxs-lookup"><span data-stu-id="eca9b-134">Open the application with a normal window.</span></span> <span data-ttu-id="eca9b-135">如果視窗最小化或最大化，系統會將其還原為其原始大小和位置。</span><span class="sxs-lookup"><span data-stu-id="eca9b-135">If the window is minimized or maximized, the system restores it to its original size and position.</span></span><br/> |
| <dl> <span data-ttu-id="eca9b-136"><dt></dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="eca9b-136"><dt></dt> <dt>2</dt></span></span> </dl>  | <span data-ttu-id="eca9b-137">以最小化的視窗開啟應用程式。</span><span class="sxs-lookup"><span data-stu-id="eca9b-137">Open the application with a minimized window.</span></span><br/>                                                                                                 |
| <dl> <span data-ttu-id="eca9b-138"><dt></dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="eca9b-138"><dt></dt> <dt>3</dt></span></span> </dl>  | <span data-ttu-id="eca9b-139">以最大化的視窗開啟應用程式。</span><span class="sxs-lookup"><span data-stu-id="eca9b-139">Open the application with a maximized window.</span></span><br/>                                                                                                 |
| <dl> <span data-ttu-id="eca9b-140"><dt></dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="eca9b-140"><dt></dt> <dt>4</dt></span></span> </dl>  | <span data-ttu-id="eca9b-141">以最新的大小和位置開啟應用程式的視窗。</span><span class="sxs-lookup"><span data-stu-id="eca9b-141">Open the application with its window at its most recent size and position.</span></span> <span data-ttu-id="eca9b-142">使用中視窗仍維持使用中狀態。</span><span class="sxs-lookup"><span data-stu-id="eca9b-142">The active window remains active.</span></span><br/>                                  |
| <dl> <span data-ttu-id="eca9b-143"><dt></dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="eca9b-143"><dt></dt> <dt>5</dt></span></span> </dl>  | <span data-ttu-id="eca9b-144">以目前的大小和位置開啟應用程式的視窗。</span><span class="sxs-lookup"><span data-stu-id="eca9b-144">Open the application with its window at its current size and position.</span></span><br/>                                                                        |
| <dl> <span data-ttu-id="eca9b-145"><dt></dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="eca9b-145"><dt></dt> <dt>7</dt></span></span> </dl>  | <span data-ttu-id="eca9b-146">以最小化的視窗開啟應用程式。</span><span class="sxs-lookup"><span data-stu-id="eca9b-146">Open the application with a minimized window.</span></span> <span data-ttu-id="eca9b-147">使用中視窗仍維持使用中狀態。</span><span class="sxs-lookup"><span data-stu-id="eca9b-147">The active window remains active.</span></span><br/>                                                               |
| <dl> <span data-ttu-id="eca9b-148"><dt></dt><dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="eca9b-148"><dt></dt> <dt>10</dt></span></span> </dl> | <span data-ttu-id="eca9b-149">使用應用程式所指定的預設狀態，以其視窗開啟應用程式。</span><span class="sxs-lookup"><span data-stu-id="eca9b-149">Open the application with its window in the default state specified by the application.</span></span><br/>                                                       |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="eca9b-150">備註</span><span class="sxs-lookup"><span data-stu-id="eca9b-150">Remarks</span></span>

<span data-ttu-id="eca9b-151">這個方法是透過 [**ShellExecute**](./shell-shellexecute.md) 方法來執行和存取。</span><span class="sxs-lookup"><span data-stu-id="eca9b-151">This method is implemented and accessed through the [**Shell.ShellExecute**](./shell-shellexecute.md) method.</span></span>

<span data-ttu-id="eca9b-152">這個方法相當於啟動與檔案的快捷方式功能表相關聯的其中一個命令。</span><span class="sxs-lookup"><span data-stu-id="eca9b-152">This method is equivalent to launching one of the commands associated with a file's shortcut menu.</span></span> <span data-ttu-id="eca9b-153">每個命令都會以動詞字串表示。</span><span class="sxs-lookup"><span data-stu-id="eca9b-153">Each command is represented by a verb string.</span></span> <span data-ttu-id="eca9b-154">一組支援的動詞會因檔案而異。</span><span class="sxs-lookup"><span data-stu-id="eca9b-154">The set of supported verbs varies from file to file.</span></span> <span data-ttu-id="eca9b-155">最常支援的動詞為 "open"，這通常也是預設動詞。</span><span class="sxs-lookup"><span data-stu-id="eca9b-155">The most commonly supported verb is "open", which is also usually the default verb.</span></span> <span data-ttu-id="eca9b-156">只有某些類型的檔案可能會支援其他動詞。</span><span class="sxs-lookup"><span data-stu-id="eca9b-156">Other verbs might be supported by only certain types of files.</span></span> <span data-ttu-id="eca9b-157">如需 Shell 動詞命令的進一步討論，請參閱 [啟動應用程式](launch.md) 或 [擴充快捷方式功能表](context.md)。</span><span class="sxs-lookup"><span data-stu-id="eca9b-157">For further discussion of Shell verbs, see [Launching Applications](launch.md) or [Extending Shortcut Menus](context.md).</span></span>

<span data-ttu-id="eca9b-158">Microsoft Visual Basic 目前無法使用這個方法。</span><span class="sxs-lookup"><span data-stu-id="eca9b-158">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="eca9b-159">範例</span><span class="sxs-lookup"><span data-stu-id="eca9b-159">Examples</span></span>

<span data-ttu-id="eca9b-160">下列範例示範如何使用 **ShellExecute** 來開啟 [記事本]。</span><span class="sxs-lookup"><span data-stu-id="eca9b-160">The following examples show the use of **ShellExecute** to open Notepad.</span></span> <span data-ttu-id="eca9b-161">JScript 和 VBScript 會顯示使用方式。</span><span class="sxs-lookup"><span data-stu-id="eca9b-161">Usage is shown for JScript and VBScript.</span></span>

<span data-ttu-id="eca9b-162">Jscript：</span><span class="sxs-lookup"><span data-stu-id="eca9b-162">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellExecuteJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.ShellExecute("notepad.exe", "", "", "open", 1);
    }
</script>
```



<span data-ttu-id="eca9b-163">VBScript</span><span class="sxs-lookup"><span data-stu-id="eca9b-163">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellExecuteVB()
        dim objShell

        set objShell = CreateObject("shell.application")

        objShell.ShellExecute "notepad.exe", "", "", "open", 1

        set objShell = nothing
    end function
</script>
```



## <a name="requirements"></a><span data-ttu-id="eca9b-164">規格需求</span><span class="sxs-lookup"><span data-stu-id="eca9b-164">Requirements</span></span>



| <span data-ttu-id="eca9b-165">需求</span><span class="sxs-lookup"><span data-stu-id="eca9b-165">Requirement</span></span> | <span data-ttu-id="eca9b-166">值</span><span class="sxs-lookup"><span data-stu-id="eca9b-166">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eca9b-167">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="eca9b-167">Minimum supported client</span></span><br/> | <span data-ttu-id="eca9b-168">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="eca9b-168">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="eca9b-169">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="eca9b-169">Minimum supported server</span></span><br/> | <span data-ttu-id="eca9b-170">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="eca9b-170">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="eca9b-171">標頭</span><span class="sxs-lookup"><span data-stu-id="eca9b-171">Header</span></span><br/>                   | <dl> <span data-ttu-id="eca9b-172"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="eca9b-172"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="eca9b-173">Idl</span><span class="sxs-lookup"><span data-stu-id="eca9b-173">IDL</span></span><br/>                      | <dl> <span data-ttu-id="eca9b-174"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="eca9b-174"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="eca9b-175">DLL</span><span class="sxs-lookup"><span data-stu-id="eca9b-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eca9b-176"><dt>Shell32.dll (5.0 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="eca9b-176"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
