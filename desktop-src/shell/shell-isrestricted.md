---
description: IsRestricted 方法-從登錄中抓取群組的限制設定。
ms.assetid: C4B3B5C0-7445-483a-885F-5283BD4D4B39
title: 'IsRestricted 方法 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.IsRestricted
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 3e428c914cf95d282fd721071009efc70fcb3a4d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104256"
---
# <a name="shellisrestricted-method"></a><span data-ttu-id="1c8e2-103">IsRestricted 方法</span><span class="sxs-lookup"><span data-stu-id="1c8e2-103">Shell.IsRestricted method</span></span>

<span data-ttu-id="1c8e2-104">從登錄抓取群組的限制設定。</span><span class="sxs-lookup"><span data-stu-id="1c8e2-104">Retrieves a group's restriction setting from the registry.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c8e2-105">語法</span><span class="sxs-lookup"><span data-stu-id="1c8e2-105">Syntax</span></span>


```JScript
iRetVal = Shell.IsRestricted(
  sGroup,
  sRestriction
)
```


```VB

Shell.IsRestricted( _
  ByVal sGroup As BSTR, _
  ByVal sRestriction As BSTR _
) As Integer
```





## <a name="parameters"></a><span data-ttu-id="1c8e2-106">參數</span><span class="sxs-lookup"><span data-stu-id="1c8e2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c8e2-107">*sGroup* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1c8e2-107">*sGroup* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c8e2-108">類型： **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="1c8e2-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="1c8e2-109">包含組名的 **字串** 。</span><span class="sxs-lookup"><span data-stu-id="1c8e2-109">A **String** that contains the group name.</span></span> <span data-ttu-id="1c8e2-110">此值是用來檢查限制的登錄子機碼名稱。</span><span class="sxs-lookup"><span data-stu-id="1c8e2-110">This value is the name of a registry subkey under which to check for the restriction.</span></span>

</dd> <dt>

<span data-ttu-id="1c8e2-111">*sRestriction* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1c8e2-111">*sRestriction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c8e2-112">類型： **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="1c8e2-112">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="1c8e2-113">**字串**，包含要取出其值的限制。</span><span class="sxs-lookup"><span data-stu-id="1c8e2-113">A **String** that contains the restriction whose value is to be retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c8e2-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="1c8e2-114">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="1c8e2-115">JScript</span><span class="sxs-lookup"><span data-stu-id="1c8e2-115">JScript</span></span>

<span data-ttu-id="1c8e2-116">類型：**整數 \***</span><span class="sxs-lookup"><span data-stu-id="1c8e2-116">Type: **Integer\***</span></span>

<span data-ttu-id="1c8e2-117">限制的值。</span><span class="sxs-lookup"><span data-stu-id="1c8e2-117">The value of the restriction.</span></span> <span data-ttu-id="1c8e2-118">如果找不到指定的限制，則傳回值為0。</span><span class="sxs-lookup"><span data-stu-id="1c8e2-118">If the specified restriction is not found, the return value is 0.</span></span>

### <a name="vb"></a><span data-ttu-id="1c8e2-119">VB</span><span class="sxs-lookup"><span data-stu-id="1c8e2-119">VB</span></span>

<span data-ttu-id="1c8e2-120">類型：**整數 \***</span><span class="sxs-lookup"><span data-stu-id="1c8e2-120">Type: **Integer\***</span></span>

<span data-ttu-id="1c8e2-121">限制的值。</span><span class="sxs-lookup"><span data-stu-id="1c8e2-121">The value of the restriction.</span></span> <span data-ttu-id="1c8e2-122">如果找不到指定的限制，則傳回值為0。</span><span class="sxs-lookup"><span data-stu-id="1c8e2-122">If the specified restriction is not found, the return value is 0.</span></span>

## <a name="remarks"></a><span data-ttu-id="1c8e2-123">備註</span><span class="sxs-lookup"><span data-stu-id="1c8e2-123">Remarks</span></span>

<span data-ttu-id="1c8e2-124">**IsRestricted** 會先尋找符合下列索引鍵之 *sGroup* 的子機碼名稱。</span><span class="sxs-lookup"><span data-stu-id="1c8e2-124">**IsRestricted** first looks for a subkey name that matches *sGroup* under the following key.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Policies
```

<span data-ttu-id="1c8e2-125">限制會宣告為個別原則子機碼的值。</span><span class="sxs-lookup"><span data-stu-id="1c8e2-125">Restrictions are declared as values of the individual policy subkeys.</span></span> <span data-ttu-id="1c8e2-126">如果在 *sGroup* 中名為的子機碼中找到名為 *sRestriction* 的限制，則 **IsRestricted** 會傳回限制的目前值。</span><span class="sxs-lookup"><span data-stu-id="1c8e2-126">If the restriction named in *sRestriction* is found in the subkey named in *sGroup*, **IsRestricted** returns the restriction's current value.</span></span> <span data-ttu-id="1c8e2-127">如果在 **HKEY \_ 本機 \_ 電腦** 下找不到限制，則會在 [ **HKEY 目前的 \_ \_ 使用者**] 底下檢查相同的子機碼。</span><span class="sxs-lookup"><span data-stu-id="1c8e2-127">If the restriction is not found under **HKEY\_LOCAL\_MACHINE**, the same subkey is checked under **HKEY\_CURRENT\_USER**.</span></span>

<span data-ttu-id="1c8e2-128">Microsoft Visual Basic 目前無法使用這個方法。</span><span class="sxs-lookup"><span data-stu-id="1c8e2-128">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="1c8e2-129">範例</span><span class="sxs-lookup"><span data-stu-id="1c8e2-129">Examples</span></span>

<span data-ttu-id="1c8e2-130">下列範例示範如何使用 **IsRestricted** 從 **系統** 子機碼取出 **undockwithoutlogon** 限制的資料值。</span><span class="sxs-lookup"><span data-stu-id="1c8e2-130">The following examples show the use of **IsRestricted** to retrieve the data value of the **undockwithoutlogon** restriction from the **System** subkey.</span></span> <span data-ttu-id="1c8e2-131">JScript 和 VBScript 會顯示使用方式。</span><span class="sxs-lookup"><span data-stu-id="1c8e2-131">Usage is shown for JScript and VBScript.</span></span>

<span data-ttu-id="1c8e2-132">Jscript：</span><span class="sxs-lookup"><span data-stu-id="1c8e2-132">JScript:</span></span>


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



<span data-ttu-id="1c8e2-133">VBScript</span><span class="sxs-lookup"><span data-stu-id="1c8e2-133">VBScript:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="1c8e2-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="1c8e2-134">Requirements</span></span>



| <span data-ttu-id="1c8e2-135">需求</span><span class="sxs-lookup"><span data-stu-id="1c8e2-135">Requirement</span></span> | <span data-ttu-id="1c8e2-136">值</span><span class="sxs-lookup"><span data-stu-id="1c8e2-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c8e2-137">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1c8e2-137">Minimum supported client</span></span><br/> | <span data-ttu-id="1c8e2-138">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1c8e2-138">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1c8e2-139">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1c8e2-139">Minimum supported server</span></span><br/> | <span data-ttu-id="1c8e2-140">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1c8e2-140">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="1c8e2-141">標頭</span><span class="sxs-lookup"><span data-stu-id="1c8e2-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="1c8e2-142"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="1c8e2-142"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="1c8e2-143">Idl</span><span class="sxs-lookup"><span data-stu-id="1c8e2-143">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1c8e2-144"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="1c8e2-144"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="1c8e2-145">DLL</span><span class="sxs-lookup"><span data-stu-id="1c8e2-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1c8e2-146"><dt>Shell32.dll (5.0 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="1c8e2-146"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
