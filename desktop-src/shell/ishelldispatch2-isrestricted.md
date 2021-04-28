---
description: IShellDispatch2. IsRestricted 方法-從登錄中抓取群組的限制設定。
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
ms.openlocfilehash: b4f482407fadd16d7ecfe9deeafd91b032a9a24f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117096"
---
# <a name="ishelldispatch2isrestricted-method"></a><span data-ttu-id="eb469-103">IShellDispatch2. IsRestricted 方法</span><span class="sxs-lookup"><span data-stu-id="eb469-103">IShellDispatch2.IsRestricted method</span></span>

<span data-ttu-id="eb469-104">從登錄抓取群組的限制設定。</span><span class="sxs-lookup"><span data-stu-id="eb469-104">Retrieves a group's restriction setting from the registry.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb469-105">語法</span><span class="sxs-lookup"><span data-stu-id="eb469-105">Syntax</span></span>


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





## <a name="parameters"></a><span data-ttu-id="eb469-106">參數</span><span class="sxs-lookup"><span data-stu-id="eb469-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb469-107">*sGroup* \[在\]</span><span class="sxs-lookup"><span data-stu-id="eb469-107">*sGroup* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb469-108">類型： **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="eb469-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="eb469-109">包含組名的 **字串** 。</span><span class="sxs-lookup"><span data-stu-id="eb469-109">A **String** that contains the group name.</span></span> <span data-ttu-id="eb469-110">此值是用來檢查限制的登錄子機碼名稱。</span><span class="sxs-lookup"><span data-stu-id="eb469-110">This value is the name of a registry subkey under which to check for the restriction.</span></span>

</dd> <dt>

<span data-ttu-id="eb469-111">*sRestriction* \[在\]</span><span class="sxs-lookup"><span data-stu-id="eb469-111">*sRestriction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb469-112">類型： **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="eb469-112">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="eb469-113">**字串**，包含要取出其值的限制。</span><span class="sxs-lookup"><span data-stu-id="eb469-113">A **String** that contains the restriction whose value is to be retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb469-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="eb469-114">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="eb469-115">JScript</span><span class="sxs-lookup"><span data-stu-id="eb469-115">JScript</span></span>

<span data-ttu-id="eb469-116">類型：**整數 \***</span><span class="sxs-lookup"><span data-stu-id="eb469-116">Type: **Integer\***</span></span>

<span data-ttu-id="eb469-117">限制的值。</span><span class="sxs-lookup"><span data-stu-id="eb469-117">The value of the restriction.</span></span> <span data-ttu-id="eb469-118">如果找不到指定的限制，則傳回值為0。</span><span class="sxs-lookup"><span data-stu-id="eb469-118">If the specified restriction is not found, the return value is 0.</span></span>

### <a name="vb"></a><span data-ttu-id="eb469-119">VB</span><span class="sxs-lookup"><span data-stu-id="eb469-119">VB</span></span>

<span data-ttu-id="eb469-120">類型：**整數 \***</span><span class="sxs-lookup"><span data-stu-id="eb469-120">Type: **Integer\***</span></span>

<span data-ttu-id="eb469-121">限制的值。</span><span class="sxs-lookup"><span data-stu-id="eb469-121">The value of the restriction.</span></span> <span data-ttu-id="eb469-122">如果找不到指定的限制，則傳回值為0。</span><span class="sxs-lookup"><span data-stu-id="eb469-122">If the specified restriction is not found, the return value is 0.</span></span>

## <a name="remarks"></a><span data-ttu-id="eb469-123">備註</span><span class="sxs-lookup"><span data-stu-id="eb469-123">Remarks</span></span>

<span data-ttu-id="eb469-124">這個方法是透過 [**IsRestricted**](./shell-isrestricted.md) 方法來執行和存取。</span><span class="sxs-lookup"><span data-stu-id="eb469-124">This method is implemented and accessed through the [**Shell.IsRestricted**](./shell-isrestricted.md) method.</span></span>

<span data-ttu-id="eb469-125">**IsRestricted** 會先尋找符合下列索引鍵之 *sGroup* 的子機碼名稱。</span><span class="sxs-lookup"><span data-stu-id="eb469-125">**IsRestricted** first looks for a subkey name that matches *sGroup* under the following key.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Policies
```

<span data-ttu-id="eb469-126">限制會宣告為個別原則子機碼的值。</span><span class="sxs-lookup"><span data-stu-id="eb469-126">Restrictions are declared as values of the individual policy subkeys.</span></span> <span data-ttu-id="eb469-127">如果在 *sGroup* 中名為的子機碼中找到名為 *sRestriction* 的限制，則 **IsRestricted** 會傳回限制的目前值。</span><span class="sxs-lookup"><span data-stu-id="eb469-127">If the restriction named in *sRestriction* is found in the subkey named in *sGroup*, **IsRestricted** returns the restriction's current value.</span></span> <span data-ttu-id="eb469-128">如果在 **HKEY \_ 本機 \_ 電腦** 下找不到限制，則會在 [ **HKEY 目前的 \_ \_ 使用者**] 底下檢查相同的子機碼。</span><span class="sxs-lookup"><span data-stu-id="eb469-128">If the restriction is not found under **HKEY\_LOCAL\_MACHINE**, the same subkey is checked under **HKEY\_CURRENT\_USER**.</span></span>

<span data-ttu-id="eb469-129">Microsoft Visual Basic 目前無法使用這個方法。</span><span class="sxs-lookup"><span data-stu-id="eb469-129">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="eb469-130">範例</span><span class="sxs-lookup"><span data-stu-id="eb469-130">Examples</span></span>

<span data-ttu-id="eb469-131">下列範例示範如何使用 **IsRestricted** 從 **系統** 子機碼取出 **undockwithoutlogon** 限制的資料值。</span><span class="sxs-lookup"><span data-stu-id="eb469-131">The following examples show the use of **IsRestricted** to retrieve the data value of the **undockwithoutlogon** restriction from the **System** subkey.</span></span> <span data-ttu-id="eb469-132">JScript 和 VBScript 會顯示使用方式。</span><span class="sxs-lookup"><span data-stu-id="eb469-132">Usage is shown for JScript and VBScript.</span></span>

<span data-ttu-id="eb469-133">Jscript：</span><span class="sxs-lookup"><span data-stu-id="eb469-133">JScript:</span></span>


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



<span data-ttu-id="eb469-134">VBScript</span><span class="sxs-lookup"><span data-stu-id="eb469-134">VBScript:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="eb469-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="eb469-135">Requirements</span></span>



| <span data-ttu-id="eb469-136">需求</span><span class="sxs-lookup"><span data-stu-id="eb469-136">Requirement</span></span> | <span data-ttu-id="eb469-137">值</span><span class="sxs-lookup"><span data-stu-id="eb469-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb469-138">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="eb469-138">Minimum supported client</span></span><br/> | <span data-ttu-id="eb469-139">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="eb469-139">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="eb469-140">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="eb469-140">Minimum supported server</span></span><br/> | <span data-ttu-id="eb469-141">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="eb469-141">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="eb469-142">標頭</span><span class="sxs-lookup"><span data-stu-id="eb469-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="eb469-143"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="eb469-143"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="eb469-144">Idl</span><span class="sxs-lookup"><span data-stu-id="eb469-144">IDL</span></span><br/>                      | <dl> <span data-ttu-id="eb469-145"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="eb469-145"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="eb469-146">DLL</span><span class="sxs-lookup"><span data-stu-id="eb469-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eb469-147"><dt>Shell32.dll (5.0 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="eb469-147"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
