---
description: ExplorerPolicy 方法-取得指定之 Windows Internet Explorer 原則的值。
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
ms.openlocfilehash: 765e1dc46edbe5a27292c5d8ff940e29b269f8dc
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083696"
---
# <a name="shellexplorerpolicy-method"></a><span data-ttu-id="37852-103">ExplorerPolicy 方法</span><span class="sxs-lookup"><span data-stu-id="37852-103">Shell.ExplorerPolicy method</span></span>

<span data-ttu-id="37852-104">取得指定之 Windows Internet Explorer 原則的值。</span><span class="sxs-lookup"><span data-stu-id="37852-104">Gets the value for a specified Windows Internet Explorer policy.</span></span>

## <a name="syntax"></a><span data-ttu-id="37852-105">語法</span><span class="sxs-lookup"><span data-stu-id="37852-105">Syntax</span></span>


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





## <a name="parameters"></a><span data-ttu-id="37852-106">參數</span><span class="sxs-lookup"><span data-stu-id="37852-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37852-107">*bstrPolicyName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="37852-107">*bstrPolicyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37852-108">類型： **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="37852-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="37852-109">指定原則名稱的 **字串** 。</span><span class="sxs-lookup"><span data-stu-id="37852-109">A **String** that specifies the name of the policy.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="37852-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="37852-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="37852-111">JScript</span><span class="sxs-lookup"><span data-stu-id="37852-111">JScript</span></span>

<span data-ttu-id="37852-112">類型： **Variant \***</span><span class="sxs-lookup"><span data-stu-id="37852-112">Type: **Variant\***</span></span>

<span data-ttu-id="37852-113">與指定的原則名稱相關聯的值。</span><span class="sxs-lookup"><span data-stu-id="37852-113">The value associated with the specified policy name.</span></span>

### <a name="vb"></a><span data-ttu-id="37852-114">VB</span><span class="sxs-lookup"><span data-stu-id="37852-114">VB</span></span>

<span data-ttu-id="37852-115">類型： **Variant \***</span><span class="sxs-lookup"><span data-stu-id="37852-115">Type: **Variant\***</span></span>

<span data-ttu-id="37852-116">與指定的原則名稱相關聯的值。</span><span class="sxs-lookup"><span data-stu-id="37852-116">The value associated with the specified policy name.</span></span>

## <a name="remarks"></a><span data-ttu-id="37852-117">備註</span><span class="sxs-lookup"><span data-stu-id="37852-117">Remarks</span></span>

<span data-ttu-id="37852-118">網路系統管理員可以藉由設定原則來控制和管理其使用者的計算環境。</span><span class="sxs-lookup"><span data-stu-id="37852-118">Network Administrators can control and manage the computing environment of their users by setting policies.</span></span>

<span data-ttu-id="37852-119">指定的值名稱必須在 **HKEY \_ CURRENT \_ USER** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **原則** \\ **Explorer** 子機碼內。</span><span class="sxs-lookup"><span data-stu-id="37852-119">The specified value name must be within the **HKEY\_CURRENT\_USER**\\**Software**\\**Microsoft**\\**Windows**\\**CurrentVersion**\\**Policies**\\**Explorer** subkey.</span></span> <span data-ttu-id="37852-120">如果值名稱不存在，則方法會傳回 **null**。</span><span class="sxs-lookup"><span data-stu-id="37852-120">If the value name does not exist then the method returns **null**.</span></span>

## <a name="examples"></a><span data-ttu-id="37852-121">範例</span><span class="sxs-lookup"><span data-stu-id="37852-121">Examples</span></span>

<span data-ttu-id="37852-122">下列範例示範如何適當地使用 JScript、VBScript 和 Visual Basic 的 **ExplorerPolicy** 。</span><span class="sxs-lookup"><span data-stu-id="37852-122">The following examples show the proper use of **ExplorerPolicy** for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="37852-123">Jscript：</span><span class="sxs-lookup"><span data-stu-id="37852-123">JScript:</span></span>


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



<span data-ttu-id="37852-124">VBScript</span><span class="sxs-lookup"><span data-stu-id="37852-124">VBScript:</span></span>


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



<span data-ttu-id="37852-125">Visual Basic：</span><span class="sxs-lookup"><span data-stu-id="37852-125">Visual Basic:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="37852-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="37852-126">Requirements</span></span>



| <span data-ttu-id="37852-127">需求</span><span class="sxs-lookup"><span data-stu-id="37852-127">Requirement</span></span> | <span data-ttu-id="37852-128">值</span><span class="sxs-lookup"><span data-stu-id="37852-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37852-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="37852-129">Minimum supported client</span></span><br/> | <span data-ttu-id="37852-130">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="37852-130">Windows XP \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="37852-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="37852-131">Minimum supported server</span></span><br/> | <span data-ttu-id="37852-132">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="37852-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="37852-133">標頭</span><span class="sxs-lookup"><span data-stu-id="37852-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="37852-134"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="37852-134"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="37852-135">Idl</span><span class="sxs-lookup"><span data-stu-id="37852-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="37852-136"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="37852-136"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="37852-137">DLL</span><span class="sxs-lookup"><span data-stu-id="37852-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="37852-138"><dt>Shell32.dll (6.0 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="37852-138"><dt>Shell32.dll (version 6.0 or later)</dt></span></span> </dl> |



 

 
