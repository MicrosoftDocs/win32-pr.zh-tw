---
description: 從登錄抓取群組的限制設定。
ms.assetid: 04275c5f-c3ed-4962-882f-2cce0258a9f4
title: 'IShellDispatch2. IsRestricted 方法 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch2.IsRestricted
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: f666a9ed3407d12eb9cf2c28ae062a9886d7a2cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972405"
---
# <a name="ishelldispatch2isrestricted-method"></a><span data-ttu-id="54306-103">IShellDispatch2. IsRestricted 方法</span><span class="sxs-lookup"><span data-stu-id="54306-103">IShellDispatch2.IsRestricted method</span></span>

<span data-ttu-id="54306-104">從登錄抓取群組的限制設定。</span><span class="sxs-lookup"><span data-stu-id="54306-104">Retrieves a group's restriction setting from the registry.</span></span>

## <a name="syntax"></a><span data-ttu-id="54306-105">語法</span><span class="sxs-lookup"><span data-stu-id="54306-105">Syntax</span></span>


```JScript
iRetVal = IShellDispatch2.IsRestricted(
  sGroup,
  sRestriction
)
```


```VB

IShellDispatch2.IsRestricted( _
  ByVal sGroup As BSTR, _
  ByVal sRestriction As BSTR _
) As Integer
```





## <a name="parameters"></a><span data-ttu-id="54306-106">參數</span><span class="sxs-lookup"><span data-stu-id="54306-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54306-107">*sGroup* \[在\]</span><span class="sxs-lookup"><span data-stu-id="54306-107">*sGroup* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54306-108">類型： **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="54306-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="54306-109">包含組名的 **字串** 。</span><span class="sxs-lookup"><span data-stu-id="54306-109">A **String** that contains the group name.</span></span> <span data-ttu-id="54306-110">此值是用來檢查限制的登錄子機碼名稱。</span><span class="sxs-lookup"><span data-stu-id="54306-110">This value is the name of a registry subkey under which to check for the restriction.</span></span>

</dd> <dt>

<span data-ttu-id="54306-111">*sRestriction* \[在\]</span><span class="sxs-lookup"><span data-stu-id="54306-111">*sRestriction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54306-112">類型： **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="54306-112">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="54306-113">**字串**，包含要取出其值的限制。</span><span class="sxs-lookup"><span data-stu-id="54306-113">A **String** that contains the restriction whose value is to be retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54306-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="54306-114">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="54306-115">JScript</span><span class="sxs-lookup"><span data-stu-id="54306-115">JScript</span></span>

<span data-ttu-id="54306-116">類型： \**整數 \** _</span><span class="sxs-lookup"><span data-stu-id="54306-116">Type: \**Integer\** _</span></span>

<span data-ttu-id="54306-117">限制的值。</span><span class="sxs-lookup"><span data-stu-id="54306-117">The value of the restriction.</span></span> <span data-ttu-id="54306-118">如果找不到指定的限制，則傳回值為0。</span><span class="sxs-lookup"><span data-stu-id="54306-118">If the specified restriction is not found, the return value is 0.</span></span>

### <a name="vb"></a><span data-ttu-id="54306-119">VB</span><span class="sxs-lookup"><span data-stu-id="54306-119">VB</span></span>

<span data-ttu-id="54306-120">類型： _*整數 \**_</span><span class="sxs-lookup"><span data-stu-id="54306-120">Type: _*Integer\**_</span></span>

<span data-ttu-id="54306-121">限制的值。</span><span class="sxs-lookup"><span data-stu-id="54306-121">The value of the restriction.</span></span> <span data-ttu-id="54306-122">如果找不到指定的限制，則傳回值為0。</span><span class="sxs-lookup"><span data-stu-id="54306-122">If the specified restriction is not found, the return value is 0.</span></span>

## <a name="remarks"></a><span data-ttu-id="54306-123">備註</span><span class="sxs-lookup"><span data-stu-id="54306-123">Remarks</span></span>

<span data-ttu-id="54306-124">這個方法是透過 [_ *Shell. IsRestricted* \*](./shell-isrestricted.md)方法來執行和存取。</span><span class="sxs-lookup"><span data-stu-id="54306-124">This method is implemented and accessed through the [_ *Shell.IsRestricted*\*](./shell-isrestricted.md) method.</span></span>

<span data-ttu-id="54306-125">**IsRestricted** 會先尋找符合下列索引鍵之 *sGroup* 的子機碼名稱。</span><span class="sxs-lookup"><span data-stu-id="54306-125">**IsRestricted** first looks for a subkey name that matches *sGroup* under the following key.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Policies
```

<span data-ttu-id="54306-126">限制會宣告為個別原則子機碼的值。</span><span class="sxs-lookup"><span data-stu-id="54306-126">Restrictions are declared as values of the individual policy subkeys.</span></span> <span data-ttu-id="54306-127">如果在 *sGroup* 中名為的子機碼中找到名為 *sRestriction* 的限制，則 **IsRestricted** 會傳回限制的目前值。</span><span class="sxs-lookup"><span data-stu-id="54306-127">If the restriction named in *sRestriction* is found in the subkey named in *sGroup*, **IsRestricted** returns the restriction's current value.</span></span> <span data-ttu-id="54306-128">如果在 **HKEY \_ 本機 \_ 電腦** 下找不到限制，則會在 [ **HKEY 目前的 \_ \_ 使用者**] 底下檢查相同的子機碼。</span><span class="sxs-lookup"><span data-stu-id="54306-128">If the restriction is not found under **HKEY\_LOCAL\_MACHINE**, the same subkey is checked under **HKEY\_CURRENT\_USER**.</span></span>

<span data-ttu-id="54306-129">Microsoft Visual Basic 目前無法使用這個方法。</span><span class="sxs-lookup"><span data-stu-id="54306-129">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="54306-130">範例</span><span class="sxs-lookup"><span data-stu-id="54306-130">Examples</span></span>

<span data-ttu-id="54306-131">下列範例示範如何使用 **IsRestricted** 從 **系統** 子機碼取出 **undockwithoutlogon** 限制的資料值。</span><span class="sxs-lookup"><span data-stu-id="54306-131">The following examples show the use of **IsRestricted** to retrieve the data value of the **undockwithoutlogon** restriction from the **System** subkey.</span></span> <span data-ttu-id="54306-132">JScript 和 VBScript 會顯示使用方式。</span><span class="sxs-lookup"><span data-stu-id="54306-132">Usage is shown for JScript and VBScript.</span></span>

<span data-ttu-id="54306-133">Jscript：</span><span class="sxs-lookup"><span data-stu-id="54306-133">JScript:</span></span>


```JScript
<script language="JScript">
    function fnIsRestricedJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var lReturn;
        
        lReturn = objShell.IsRestricted("system", "undockwithoutlogon");
        document.write(lReturn);
    }
</script>
```



<span data-ttu-id="54306-134">VBScript</span><span class="sxs-lookup"><span data-stu-id="54306-134">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnIsRestricedVB()
        dim objShell
        dim lReturn

        set objShell = CreateObject("shell.application")

        lReturn = objShell.IsRestricted("system", "undockwithoutlogon")
        document.write(lReturn)

        set objShell = nothing
    end function
</script>
```



## <a name="requirements"></a><span data-ttu-id="54306-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="54306-135">Requirements</span></span>



| <span data-ttu-id="54306-136">需求</span><span class="sxs-lookup"><span data-stu-id="54306-136">Requirement</span></span> | <span data-ttu-id="54306-137">值</span><span class="sxs-lookup"><span data-stu-id="54306-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="54306-138">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="54306-138">Minimum supported client</span></span><br/> | <span data-ttu-id="54306-139">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="54306-139">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="54306-140">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="54306-140">Minimum supported server</span></span><br/> | <span data-ttu-id="54306-141">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="54306-141">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="54306-142">標頭</span><span class="sxs-lookup"><span data-stu-id="54306-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="54306-143"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="54306-143"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="54306-144">Idl</span><span class="sxs-lookup"><span data-stu-id="54306-144">IDL</span></span><br/>                      | <dl> <span data-ttu-id="54306-145"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="54306-145"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="54306-146">DLL</span><span class="sxs-lookup"><span data-stu-id="54306-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="54306-147"><dt>Shell32.dll (5.0 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="54306-147"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
