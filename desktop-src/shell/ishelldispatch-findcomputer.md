---
<span data-ttu-id="2b17a-101">描述： IShellDispatch. FindComputer 方法-' 顯示搜尋結果：電腦對話方塊。</span><span class="sxs-lookup"><span data-stu-id="2b17a-101">description: IShellDispatch.FindComputer method - 'Displays the Search Results: Computers dialog box.</span></span> <span data-ttu-id="2b17a-102">此對話方塊會顯示指定電腦的搜尋結果。</span><span class="sxs-lookup"><span data-stu-id="2b17a-102">The dialog box shows the result of the search for a specified computer.'</span></span>
<span data-ttu-id="2b17a-103">assetid： 9B687A8A-BB29-49a0-8AE3-11A75FAF3257 title： IShellDispatch. FindComputer 方法 (Shldisp .h) ms. 主題： reference ms. date： 05/31/2018 topic_type：</span><span class="sxs-lookup"><span data-stu-id="2b17a-103">ms.assetid: 9B687A8A-BB29-49a0-8AE3-11A75FAF3257 title: IShellDispatch.FindComputer method (Shldisp.h) ms.topic: reference ms.date: 05/31/2018 topic_type:</span></span> 
- <span data-ttu-id="2b17a-104">APIRef</span><span class="sxs-lookup"><span data-stu-id="2b17a-104">APIRef</span></span>
- <span data-ttu-id="2b17a-105">kbSyntax api_name：</span><span class="sxs-lookup"><span data-stu-id="2b17a-105">kbSyntax api_name:</span></span> 
- <span data-ttu-id="2b17a-106">IShellDispatch. FindComputer api_type：</span><span class="sxs-lookup"><span data-stu-id="2b17a-106">IShellDispatch.FindComputer api_type:</span></span> 
- <span data-ttu-id="2b17a-107">COM api_location：</span><span class="sxs-lookup"><span data-stu-id="2b17a-107">COM api_location:</span></span> 
- <span data-ttu-id="2b17a-108">Shell32.dll</span><span class="sxs-lookup"><span data-stu-id="2b17a-108">Shell32.dll</span></span>
---

# <a name="ishelldispatchfindcomputer-method"></a><span data-ttu-id="2b17a-109">IShellDispatch. FindComputer 方法</span><span class="sxs-lookup"><span data-stu-id="2b17a-109">IShellDispatch.FindComputer method</span></span>

<span data-ttu-id="2b17a-110">顯示 [ **搜尋結果：電腦** ] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="2b17a-110">Displays the **Search Results: Computers** dialog box.</span></span> <span data-ttu-id="2b17a-111">此對話方塊會顯示指定電腦的搜尋結果。</span><span class="sxs-lookup"><span data-stu-id="2b17a-111">The dialog box shows the result of the search for a specified computer.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b17a-112">語法</span><span class="sxs-lookup"><span data-stu-id="2b17a-112">Syntax</span></span>


```JScript
IShellDispatch.FindComputer()
```


```VB

IShellDispatch.FindComputer()
```





## <a name="parameters"></a><span data-ttu-id="2b17a-113">參數</span><span class="sxs-lookup"><span data-stu-id="2b17a-113">Parameters</span></span>

<span data-ttu-id="2b17a-114">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="2b17a-114">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2b17a-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="2b17a-115">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="2b17a-116">JScript</span><span class="sxs-lookup"><span data-stu-id="2b17a-116">JScript</span></span>

<span data-ttu-id="2b17a-117">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="2b17a-117">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="2b17a-118">VB</span><span class="sxs-lookup"><span data-stu-id="2b17a-118">VB</span></span>

<span data-ttu-id="2b17a-119">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="2b17a-119">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2b17a-120">備註</span><span class="sxs-lookup"><span data-stu-id="2b17a-120">Remarks</span></span>

<span data-ttu-id="2b17a-121">這個方法是透過 [**FindComputer**](shell-findcomputer.md) 方法來執行和存取。</span><span class="sxs-lookup"><span data-stu-id="2b17a-121">This method is implemented and accessed through the [**Shell.FindComputer**](shell-findcomputer.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="2b17a-122">範例</span><span class="sxs-lookup"><span data-stu-id="2b17a-122">Examples</span></span>

<span data-ttu-id="2b17a-123">下列範例示範如何在 JScript、VBScript 和 Visual Basic 中使用 **FindComputer** 。</span><span class="sxs-lookup"><span data-stu-id="2b17a-123">The following examples show the use of **FindComputer** in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="2b17a-124">Jscript：</span><span class="sxs-lookup"><span data-stu-id="2b17a-124">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellFindComputerJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.FindComputer();
    }
</script>
```



<span data-ttu-id="2b17a-125">VBScript</span><span class="sxs-lookup"><span data-stu-id="2b17a-125">VBScript:</span></span>


```VB
 <script language="VBScript">
    function fnShellFindComputerVB()
        dim objShell
        dim ssfWINDOWS
        ssfWINDOWS = 36

        set objShell = CreateObject("shell.application")
        objshell.FindComputer

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="2b17a-126">Visual Basic：</span><span class="sxs-lookup"><span data-stu-id="2b17a-126">Visual Basic:</span></span>


```VB
Private Sub fnShellFindComputerVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objshell.FindComputer

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="2b17a-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="2b17a-127">Requirements</span></span>



| <span data-ttu-id="2b17a-128">需求</span><span class="sxs-lookup"><span data-stu-id="2b17a-128">Requirement</span></span> | <span data-ttu-id="2b17a-129">值</span><span class="sxs-lookup"><span data-stu-id="2b17a-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b17a-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2b17a-130">Minimum supported client</span></span><br/> | <span data-ttu-id="2b17a-131">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2b17a-131">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="2b17a-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2b17a-132">Minimum supported server</span></span><br/> | <span data-ttu-id="2b17a-133">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2b17a-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="2b17a-134">標頭</span><span class="sxs-lookup"><span data-stu-id="2b17a-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="2b17a-135"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="2b17a-135"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="2b17a-136">Idl</span><span class="sxs-lookup"><span data-stu-id="2b17a-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2b17a-137"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="2b17a-137"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="2b17a-138">DLL</span><span class="sxs-lookup"><span data-stu-id="2b17a-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2b17a-139"><dt>Shell32.dll (4.71 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="2b17a-139"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




