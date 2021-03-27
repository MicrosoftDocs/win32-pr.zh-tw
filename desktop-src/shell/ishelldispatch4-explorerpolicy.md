---
description: 取得指定之 Windows Internet Explorer 原則的值。
ms.assetid: 490c3e18-b606-456a-9016-dc4f7bad2bc3
title: 'IShellDispatch4. ExplorerPolicy 方法 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch4.ExplorerPolicy
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 57247ad328c647cf9cdde32ac1a2951dd8e364ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848299"
---
# <a name="ishelldispatch4explorerpolicy-method"></a><span data-ttu-id="703ea-103">IShellDispatch4. ExplorerPolicy 方法</span><span class="sxs-lookup"><span data-stu-id="703ea-103">IShellDispatch4.ExplorerPolicy method</span></span>

<span data-ttu-id="703ea-104">取得指定之 Windows Internet Explorer 原則的值。</span><span class="sxs-lookup"><span data-stu-id="703ea-104">Gets the value for a specified Windows Internet Explorer policy.</span></span>

## <a name="syntax"></a><span data-ttu-id="703ea-105">語法</span><span class="sxs-lookup"><span data-stu-id="703ea-105">Syntax</span></span>


```JScript
retVal = IShellDispatch4.ExplorerPolicy(
  bstrPolicyName
)
```


```VB

IShellDispatch4.ExplorerPolicy( _
  ByVal bstrPolicyName As BSTR _
) As Variant
```





## <a name="parameters"></a><span data-ttu-id="703ea-106">參數</span><span class="sxs-lookup"><span data-stu-id="703ea-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="703ea-107">*bstrPolicyName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="703ea-107">*bstrPolicyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="703ea-108">類型： **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="703ea-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="703ea-109">指定原則名稱的 **字串** 。</span><span class="sxs-lookup"><span data-stu-id="703ea-109">A **String** that specifies the name of the policy.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="703ea-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="703ea-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="703ea-111">JScript</span><span class="sxs-lookup"><span data-stu-id="703ea-111">JScript</span></span>

<span data-ttu-id="703ea-112">類型： \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="703ea-112">Type: \**Variant\** _</span></span>

<span data-ttu-id="703ea-113">與指定的原則名稱相關聯的值。</span><span class="sxs-lookup"><span data-stu-id="703ea-113">The value associated with the specified policy name.</span></span>

### <a name="vb"></a><span data-ttu-id="703ea-114">VB</span><span class="sxs-lookup"><span data-stu-id="703ea-114">VB</span></span>

<span data-ttu-id="703ea-115">類型： _*Variant \**_</span><span class="sxs-lookup"><span data-stu-id="703ea-115">Type: _*Variant\**_</span></span>

<span data-ttu-id="703ea-116">與指定的原則名稱相關聯的值。</span><span class="sxs-lookup"><span data-stu-id="703ea-116">The value associated with the specified policy name.</span></span>

## <a name="remarks"></a><span data-ttu-id="703ea-117">備註</span><span class="sxs-lookup"><span data-stu-id="703ea-117">Remarks</span></span>

<span data-ttu-id="703ea-118">網路系統管理員可以藉由設定原則來控制和管理其使用者的計算環境。</span><span class="sxs-lookup"><span data-stu-id="703ea-118">Network Administrators can control and manage the computing environment of their users by setting policies.</span></span>

<span data-ttu-id="703ea-119">指定的值名稱必須在 _ *HKEY \_ CURRENT \_ USER **\\** Software **\\** Microsoft **\\** Windows **\\** CurrentVersion **\\** 原則 **\\** Explorer*\* 子機碼內。</span><span class="sxs-lookup"><span data-stu-id="703ea-119">The specified value name must be within the _ *HKEY\_CURRENT\_USER **\\** Software **\\** Microsoft **\\** Windows **\\** CurrentVersion **\\** Policies **\\** Explorer*\* subkey.</span></span> <span data-ttu-id="703ea-120">如果值名稱不存在，則方法會傳回 **null**。</span><span class="sxs-lookup"><span data-stu-id="703ea-120">If the value name does not exist then the method returns **null**.</span></span>

## <a name="examples"></a><span data-ttu-id="703ea-121">範例</span><span class="sxs-lookup"><span data-stu-id="703ea-121">Examples</span></span>

<span data-ttu-id="703ea-122">下列範例示範如何適當地使用 JScript、VBScript 和 Visual Basic 的 **ExplorerPolicy** 。</span><span class="sxs-lookup"><span data-stu-id="703ea-122">The following examples show the proper use of **ExplorerPolicy** for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="703ea-123">Jscript：</span><span class="sxs-lookup"><span data-stu-id="703ea-123">JScript:</span></span>


```JScript
<script language="JScript">
    function fnIShellDispatch4ExplorerPolicyJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var vReturn;
        
        vReturn = objshell.ExplorerPolicy("ValueName");
        alert(vReturn);
    }
</script>
```



<span data-ttu-id="703ea-124">VBScript</span><span class="sxs-lookup"><span data-stu-id="703ea-124">VBScript:</span></span>


```VB
<script language="VBScript">
     function fnIShellDispatch4ExplorerPolicyVB()
        dim objShell
        dim vReturn
        
        set objShell = CreateObject("shell.application")
            vReturn = objshell.ExplorerPolicy("ValueName")
            alert(vReturn)
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="703ea-125">Visual Basic：</span><span class="sxs-lookup"><span data-stu-id="703ea-125">Visual Basic:</span></span>


```VB
Private Sub fnIShellDispatch4ExplorerPolicyVB()
    Dim objShell As Shell
    Dim vReturn  As Variant
    
    Set objShell = New Shell
        vReturn = objshell.ExplorerPolicy("ValueName")
        Debug.Print vReturn
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="703ea-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="703ea-126">Requirements</span></span>



| <span data-ttu-id="703ea-127">需求</span><span class="sxs-lookup"><span data-stu-id="703ea-127">Requirement</span></span> | <span data-ttu-id="703ea-128">值</span><span class="sxs-lookup"><span data-stu-id="703ea-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="703ea-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="703ea-129">Minimum supported client</span></span><br/> | <span data-ttu-id="703ea-130">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="703ea-130">Windows XP \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="703ea-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="703ea-131">Minimum supported server</span></span><br/> | <span data-ttu-id="703ea-132">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="703ea-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="703ea-133">標頭</span><span class="sxs-lookup"><span data-stu-id="703ea-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="703ea-134"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="703ea-134"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="703ea-135">Idl</span><span class="sxs-lookup"><span data-stu-id="703ea-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="703ea-136"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="703ea-136"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="703ea-137">DLL</span><span class="sxs-lookup"><span data-stu-id="703ea-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="703ea-138"><dt>Shell32.dll (6.0 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="703ea-138"><dt>Shell32.dll (version 6.0 or later)</dt></span></span> </dl> |



 

 
