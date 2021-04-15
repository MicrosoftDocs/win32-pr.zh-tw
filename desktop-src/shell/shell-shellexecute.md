---
description: 在指定的檔案上執行指定的作業。
ms.assetid: 62E59A1C-51BD-4864-AF09-35FFD49FAB9D
title: Shell.ShellExecute 方法 (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.ShellExecute
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 83ab9741199bff675245f15dc2ad1ffb20592a35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973316"
---
# <a name="shellshellexecute-method"></a><span data-ttu-id="72697-103">ShellExecute 方法</span><span class="sxs-lookup"><span data-stu-id="72697-103">Shell.ShellExecute method</span></span>

<span data-ttu-id="72697-104">在指定的檔案上執行指定的作業。</span><span class="sxs-lookup"><span data-stu-id="72697-104">Performs a specified operation on a specified file.</span></span>

## <a name="syntax"></a><span data-ttu-id="72697-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="72697-105">Syntax</span></span>

<span data-ttu-id="72697-106">Jscript：</span><span class="sxs-lookup"><span data-stu-id="72697-106">JScript:</span></span>

```js
iRetVal = Shell.ShellExecute(
  sFile,
  [ vArguments ],
  [ vDirectory ],
  [ vOperation ],
  [ vShow ]
);
```

<span data-ttu-id="72697-107">VBScript</span><span class="sxs-lookup"><span data-stu-id="72697-107">VBScript:</span></span>

```vb
iRetVal = Shell.ShellExecute( _
  sFile, _
  [ ByVal vArguments ], _
  [ ByVal vDirectory ], _
  [ ByVal vOperation ], _
  [ ByVal vShow ] _
)
```

<span data-ttu-id="72697-108">VB：</span><span class="sxs-lookup"><span data-stu-id="72697-108">VB:</span></span>

```vb
Shell.ShellExecute( _
  ByVal sFile As BSTR, _
  [ ByVal vArguments As Variant ], _
  [ ByVal vDirectory As Variant ], _
  [ ByVal vOperation As Variant ], _
  [ ByVal vShow As Variant ] _
) As Integer
```

## <a name="parameters"></a><span data-ttu-id="72697-109">參數</span><span class="sxs-lookup"><span data-stu-id="72697-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="72697-110">*sFile* \[在\]</span><span class="sxs-lookup"><span data-stu-id="72697-110">*sFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72697-111">類型： **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="72697-111">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="72697-112">**字串**，其中包含 **ShellExecute** 將執行 *vOperation* 所指定之動作的檔案名。</span><span class="sxs-lookup"><span data-stu-id="72697-112">A **String** that contains the name of the file on which **ShellExecute** will perform the action specified by *vOperation*.</span></span>

</dd> <dt>

<span data-ttu-id="72697-113">*vArguments* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="72697-113">*vArguments* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="72697-114">類型： **Variant**</span><span class="sxs-lookup"><span data-stu-id="72697-114">Type: **Variant**</span></span>

<span data-ttu-id="72697-115">包含作業參數值的字串。</span><span class="sxs-lookup"><span data-stu-id="72697-115">A string that contains parameter values for the operation.</span></span>

</dd> <dt>

<span data-ttu-id="72697-116">*vDirectory* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="72697-116">*vDirectory* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="72697-117">類型： **Variant**</span><span class="sxs-lookup"><span data-stu-id="72697-117">Type: **Variant**</span></span>

<span data-ttu-id="72697-118">目錄的完整路徑，其中包含 *sFile* 所指定的檔案。</span><span class="sxs-lookup"><span data-stu-id="72697-118">The fully qualified path of the directory that contains the file specified by *sFile*.</span></span> <span data-ttu-id="72697-119">如果未指定此參數，則會使用目前的工作目錄。</span><span class="sxs-lookup"><span data-stu-id="72697-119">If this parameter is not specified, the current working directory is used.</span></span>

</dd> <dt>

<span data-ttu-id="72697-120">*vOperation* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="72697-120">*vOperation* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="72697-121">類型： **Variant**</span><span class="sxs-lookup"><span data-stu-id="72697-121">Type: **Variant**</span></span>

<span data-ttu-id="72697-122">要執行的作業。</span><span class="sxs-lookup"><span data-stu-id="72697-122">The operation to be performed.</span></span> <span data-ttu-id="72697-123">此值會設定為檔案所支援的其中一個動詞字串。</span><span class="sxs-lookup"><span data-stu-id="72697-123">This value is set to one of the verb strings that is supported by the file.</span></span> <span data-ttu-id="72697-124">如需動詞的討論，請參閱「備註」一節。</span><span class="sxs-lookup"><span data-stu-id="72697-124">For a discussion of verbs, see the Remarks section.</span></span> <span data-ttu-id="72697-125">如果未指定此參數，則會執行預設作業。</span><span class="sxs-lookup"><span data-stu-id="72697-125">If this parameter is not specified, the default operation is performed.</span></span>

</dd> <dt>

<span data-ttu-id="72697-126">*vShow* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="72697-126">*vShow* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="72697-127">類型： **Variant**</span><span class="sxs-lookup"><span data-stu-id="72697-127">Type: **Variant**</span></span>

<span data-ttu-id="72697-128">一開始應該如何顯示應用程式視窗的建議。</span><span class="sxs-lookup"><span data-stu-id="72697-128">A recommendation as to how the application window should be displayed initially.</span></span> <span data-ttu-id="72697-129">應用程式可以忽略此建議。</span><span class="sxs-lookup"><span data-stu-id="72697-129">The application can ignore this recommendation.</span></span> <span data-ttu-id="72697-130">此參數可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="72697-130">This parameter can be one of the following values.</span></span> <span data-ttu-id="72697-131">如果未指定此參數，應用程式會使用其預設值。</span><span class="sxs-lookup"><span data-stu-id="72697-131">If this parameter is not specified, the application uses its default value.</span></span>



| <span data-ttu-id="72697-132">值</span><span class="sxs-lookup"><span data-stu-id="72697-132">Value</span></span>                                                                                                                               | <span data-ttu-id="72697-133">意義</span><span class="sxs-lookup"><span data-stu-id="72697-133">Meaning</span></span>                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="72697-134"><dt></dt><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="72697-134"><dt></dt> <dt>0</dt></span></span> </dl>  | <span data-ttu-id="72697-135">使用隱藏視窗開啟應用程式。</span><span class="sxs-lookup"><span data-stu-id="72697-135">Open the application with a hidden window.</span></span><br/>                                                                                                    |
| <dl> <span data-ttu-id="72697-136"><dt></dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="72697-136"><dt></dt> <dt>1</dt></span></span> </dl>  | <span data-ttu-id="72697-137">使用一般視窗開啟應用程式。</span><span class="sxs-lookup"><span data-stu-id="72697-137">Open the application with a normal window.</span></span> <span data-ttu-id="72697-138">如果視窗最小化或最大化，系統會將其還原為其原始大小和位置。</span><span class="sxs-lookup"><span data-stu-id="72697-138">If the window is minimized or maximized, the system restores it to its original size and position.</span></span><br/> |
| <dl> <span data-ttu-id="72697-139"><dt></dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="72697-139"><dt></dt> <dt>2</dt></span></span> </dl>  | <span data-ttu-id="72697-140">以最小化的視窗開啟應用程式。</span><span class="sxs-lookup"><span data-stu-id="72697-140">Open the application with a minimized window.</span></span><br/>                                                                                                 |
| <dl> <span data-ttu-id="72697-141"><dt></dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="72697-141"><dt></dt> <dt>3</dt></span></span> </dl>  | <span data-ttu-id="72697-142">以最大化的視窗開啟應用程式。</span><span class="sxs-lookup"><span data-stu-id="72697-142">Open the application with a maximized window.</span></span><br/>                                                                                                 |
| <dl> <span data-ttu-id="72697-143"><dt></dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="72697-143"><dt></dt> <dt>4</dt></span></span> </dl>  | <span data-ttu-id="72697-144">以最新的大小和位置開啟應用程式的視窗。</span><span class="sxs-lookup"><span data-stu-id="72697-144">Open the application with its window at its most recent size and position.</span></span> <span data-ttu-id="72697-145">使用中視窗仍維持使用中狀態。</span><span class="sxs-lookup"><span data-stu-id="72697-145">The active window remains active.</span></span><br/>                                  |
| <dl> <span data-ttu-id="72697-146"><dt></dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="72697-146"><dt></dt> <dt>5</dt></span></span> </dl>  | <span data-ttu-id="72697-147">以目前的大小和位置開啟應用程式的視窗。</span><span class="sxs-lookup"><span data-stu-id="72697-147">Open the application with its window at its current size and position.</span></span><br/>                                                                        |
| <dl> <span data-ttu-id="72697-148"><dt></dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="72697-148"><dt></dt> <dt>7</dt></span></span> </dl>  | <span data-ttu-id="72697-149">以最小化的視窗開啟應用程式。</span><span class="sxs-lookup"><span data-stu-id="72697-149">Open the application with a minimized window.</span></span> <span data-ttu-id="72697-150">使用中視窗仍維持使用中狀態。</span><span class="sxs-lookup"><span data-stu-id="72697-150">The active window remains active.</span></span><br/>                                                               |
| <dl> <span data-ttu-id="72697-151"><dt></dt><dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="72697-151"><dt></dt> <dt>10</dt></span></span> </dl> | <span data-ttu-id="72697-152">使用應用程式所指定的預設狀態，以其視窗開啟應用程式。</span><span class="sxs-lookup"><span data-stu-id="72697-152">Open the application with its window in the default state specified by the application.</span></span><br/>                                                       |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="72697-153">備註</span><span class="sxs-lookup"><span data-stu-id="72697-153">Remarks</span></span>

<span data-ttu-id="72697-154">這個方法相當於啟動與檔案的快捷方式功能表相關聯的其中一個命令。</span><span class="sxs-lookup"><span data-stu-id="72697-154">This method is equivalent to launching one of the commands associated with a file's shortcut menu.</span></span> <span data-ttu-id="72697-155">每個命令都會以動詞字串表示。</span><span class="sxs-lookup"><span data-stu-id="72697-155">Each command is represented by a verb string.</span></span> <span data-ttu-id="72697-156">一組支援的動詞會因檔案而異。</span><span class="sxs-lookup"><span data-stu-id="72697-156">The set of supported verbs varies from file to file.</span></span> <span data-ttu-id="72697-157">最常支援的動詞為 "open"，這通常也是預設動詞。</span><span class="sxs-lookup"><span data-stu-id="72697-157">The most commonly supported verb is "open", which is also usually the default verb.</span></span> <span data-ttu-id="72697-158">只有某些類型的檔案可能會支援其他動詞。</span><span class="sxs-lookup"><span data-stu-id="72697-158">Other verbs might be supported by only certain types of files.</span></span> <span data-ttu-id="72697-159">如需 Shell 動詞命令的進一步討論，請參閱 [啟動應用程式](launch.md) 或 [擴充快捷方式功能表](context.md)。</span><span class="sxs-lookup"><span data-stu-id="72697-159">For further discussion of Shell verbs, see [Launching Applications](launch.md) or [Extending Shortcut Menus](context.md).</span></span>

<span data-ttu-id="72697-160">Microsoft Visual Basic 目前無法使用這個方法。</span><span class="sxs-lookup"><span data-stu-id="72697-160">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="72697-161">範例</span><span class="sxs-lookup"><span data-stu-id="72697-161">Examples</span></span>

<span data-ttu-id="72697-162">下列範例示範如何使用 **ShellExecute** 來開啟 [記事本]。</span><span class="sxs-lookup"><span data-stu-id="72697-162">The following examples show the use of **ShellExecute** to open Notepad.</span></span> <span data-ttu-id="72697-163">JScript 和 VBScript 會顯示使用方式。</span><span class="sxs-lookup"><span data-stu-id="72697-163">Usage is shown for JScript and VBScript.</span></span>

<span data-ttu-id="72697-164">Jscript：</span><span class="sxs-lookup"><span data-stu-id="72697-164">JScript:</span></span>


```JScript
function ShellExecuteJS()
{
    var objShell = new ActiveXObject("Shell.Application");
    objShell.ShellExecute("notepad.exe", "", "", "open", 1);
}
```

<span data-ttu-id="72697-165">VBScript</span><span class="sxs-lookup"><span data-stu-id="72697-165">VBScript:</span></span>

```vb
Function ShellExecuteVB()
    Dim objShell
    Set objShell = CreateObject("Shell.Application")
    Call objShell.ShellExecute("notepad.exe", "", "", "open", 1)
End Function
```



## <a name="requirements"></a><span data-ttu-id="72697-166">規格需求</span><span class="sxs-lookup"><span data-stu-id="72697-166">Requirements</span></span>



| <span data-ttu-id="72697-167">需求</span><span class="sxs-lookup"><span data-stu-id="72697-167">Requirement</span></span> | <span data-ttu-id="72697-168">值</span><span class="sxs-lookup"><span data-stu-id="72697-168">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="72697-169">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="72697-169">Minimum supported client</span></span><br/> | <span data-ttu-id="72697-170">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="72697-170">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="72697-171">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="72697-171">Minimum supported server</span></span><br/> | <span data-ttu-id="72697-172">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="72697-172">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="72697-173">標頭</span><span class="sxs-lookup"><span data-stu-id="72697-173">Header</span></span><br/>                   | <dl> <span data-ttu-id="72697-174"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="72697-174"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="72697-175">Idl</span><span class="sxs-lookup"><span data-stu-id="72697-175">IDL</span></span><br/>                      | <dl> <span data-ttu-id="72697-176"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="72697-176"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="72697-177">DLL</span><span class="sxs-lookup"><span data-stu-id="72697-177">DLL</span></span><br/>                      | <dl> <span data-ttu-id="72697-178"><dt>Shell32.dll (5.0 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="72697-178"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
