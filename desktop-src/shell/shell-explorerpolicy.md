---
description: 取得指定之 Windows Internet Explorer 原則的值。
ms.assetid: 47E17F6A-ED43-44cd-AF77-A6E49865E1B5
title: 'ExplorerPolicy 方法 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.ExplorerPolicy
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: fea5192990b8c19c8ddfe8ffad6efe21b98625c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973804"
---
# <a name="shellexplorerpolicy-method"></a><span data-ttu-id="e1805-103">ExplorerPolicy 方法</span><span class="sxs-lookup"><span data-stu-id="e1805-103">Shell.ExplorerPolicy method</span></span>

<span data-ttu-id="e1805-104">取得指定之 Windows Internet Explorer 原則的值。</span><span class="sxs-lookup"><span data-stu-id="e1805-104">Gets the value for a specified Windows Internet Explorer policy.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1805-105">語法</span><span class="sxs-lookup"><span data-stu-id="e1805-105">Syntax</span></span>


```JScript
retVal = Shell.ExplorerPolicy(
  bstrPolicyName
)
```


```VB

Shell.ExplorerPolicy( _
  ByVal bstrPolicyName As BSTR _
) As Variant
```





## <a name="parameters"></a><span data-ttu-id="e1805-106">參數</span><span class="sxs-lookup"><span data-stu-id="e1805-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e1805-107">*bstrPolicyName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e1805-107">*bstrPolicyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1805-108">類型： **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="e1805-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="e1805-109">指定原則名稱的 **字串** 。</span><span class="sxs-lookup"><span data-stu-id="e1805-109">A **String** that specifies the name of the policy.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e1805-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="e1805-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="e1805-111">JScript</span><span class="sxs-lookup"><span data-stu-id="e1805-111">JScript</span></span>

<span data-ttu-id="e1805-112">類型： \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="e1805-112">Type: \**Variant\** _</span></span>

<span data-ttu-id="e1805-113">與指定的原則名稱相關聯的值。</span><span class="sxs-lookup"><span data-stu-id="e1805-113">The value associated with the specified policy name.</span></span>

### <a name="vb"></a><span data-ttu-id="e1805-114">VB</span><span class="sxs-lookup"><span data-stu-id="e1805-114">VB</span></span>

<span data-ttu-id="e1805-115">類型： _*Variant \**_</span><span class="sxs-lookup"><span data-stu-id="e1805-115">Type: _*Variant\**_</span></span>

<span data-ttu-id="e1805-116">與指定的原則名稱相關聯的值。</span><span class="sxs-lookup"><span data-stu-id="e1805-116">The value associated with the specified policy name.</span></span>

## <a name="remarks"></a><span data-ttu-id="e1805-117">備註</span><span class="sxs-lookup"><span data-stu-id="e1805-117">Remarks</span></span>

<span data-ttu-id="e1805-118">網路系統管理員可以藉由設定原則來控制和管理其使用者的計算環境。</span><span class="sxs-lookup"><span data-stu-id="e1805-118">Network Administrators can control and manage the computing environment of their users by setting policies.</span></span>

<span data-ttu-id="e1805-119">指定的值名稱必須在 _ *HKEY \_ CURRENT \_ USER **\\** Software **\\** Microsoft **\\** Windows **\\** CurrentVersion **\\** 原則 **\\** Explorer*\* 子機碼內。</span><span class="sxs-lookup"><span data-stu-id="e1805-119">The specified value name must be within the _ *HKEY\_CURRENT\_USER **\\** Software **\\** Microsoft **\\** Windows **\\** CurrentVersion **\\** Policies **\\** Explorer*\* subkey.</span></span> <span data-ttu-id="e1805-120">如果值名稱不存在，則方法會傳回 **null**。</span><span class="sxs-lookup"><span data-stu-id="e1805-120">If the value name does not exist then the method returns **null**.</span></span>

## <a name="examples"></a><span data-ttu-id="e1805-121">範例</span><span class="sxs-lookup"><span data-stu-id="e1805-121">Examples</span></span>

<span data-ttu-id="e1805-122">下列範例示範如何適當地使用 JScript、VBScript 和 Visual Basic 的 **ExplorerPolicy** 。</span><span class="sxs-lookup"><span data-stu-id="e1805-122">The following examples show the proper use of **ExplorerPolicy** for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="e1805-123">Jscript：</span><span class="sxs-lookup"><span data-stu-id="e1805-123">JScript:</span></span>


```JScript
<script language="JScript">
    function fnIShellDispatch4ExplorerPolicyJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var vReturn;
        
        vReturn = objShell.ExplorerPolicy("ValueName");
        alert(vReturn);
    }
</script>
```



<span data-ttu-id="e1805-124">VBScript</span><span class="sxs-lookup"><span data-stu-id="e1805-124">VBScript:</span></span>


```VB
<script language="VBScript">
     function fnIShellDispatch4ExplorerPolicyVB()
        dim objShell
        dim vReturn
        
        set objShell = CreateObject("shell.application")
            vReturn = objShell.ExplorerPolicy("ValueName")
            alert(vReturn)
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="e1805-125">Visual Basic：</span><span class="sxs-lookup"><span data-stu-id="e1805-125">Visual Basic:</span></span>


```VB
Private Sub fnIShellDispatch4ExplorerPolicyVB()
    Dim objShell As Shell
    Dim vReturn  As Variant
    
    Set objShell = New Shell
        vReturn = objShell.ExplorerPolicy("ValueName")
        Debug.Print vReturn
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="e1805-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="e1805-126">Requirements</span></span>



| <span data-ttu-id="e1805-127">需求</span><span class="sxs-lookup"><span data-stu-id="e1805-127">Requirement</span></span> | <span data-ttu-id="e1805-128">值</span><span class="sxs-lookup"><span data-stu-id="e1805-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1805-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e1805-129">Minimum supported client</span></span><br/> | <span data-ttu-id="e1805-130">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e1805-130">Windows XP \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="e1805-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e1805-131">Minimum supported server</span></span><br/> | <span data-ttu-id="e1805-132">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e1805-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="e1805-133">標頭</span><span class="sxs-lookup"><span data-stu-id="e1805-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="e1805-134"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="e1805-134"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="e1805-135">Idl</span><span class="sxs-lookup"><span data-stu-id="e1805-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e1805-136"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="e1805-136"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="e1805-137">DLL</span><span class="sxs-lookup"><span data-stu-id="e1805-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e1805-138"><dt>Shell32.dll (6.0 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="e1805-138"><dt>Shell32.dll (version 6.0 or later)</dt></span></span> </dl> |



 

 
