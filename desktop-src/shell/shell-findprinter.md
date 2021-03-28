---
description: 顯示 [尋找印表機] 對話方塊。
ms.assetid: 61C700CF-623B-4c99-A211-AC26A1E4AE85
title: 'FindPrinter 方法 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.FindPrinter
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 1286bb7247359ea91d29a53f8f0eaa13b55be5e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973689"
---
# <a name="shellfindprinter-method"></a><span data-ttu-id="d42d8-103">FindPrinter 方法</span><span class="sxs-lookup"><span data-stu-id="d42d8-103">Shell.FindPrinter method</span></span>

<span data-ttu-id="d42d8-104">顯示 [ **尋找印表機** ] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="d42d8-104">Displays the **Find Printer** dialog box.</span></span>

## <a name="syntax"></a><span data-ttu-id="d42d8-105">語法</span><span class="sxs-lookup"><span data-stu-id="d42d8-105">Syntax</span></span>


```JScript
iRetVal = Shell.FindPrinter(
  [ sName ],
  [ sLocation ],
  [ sModel ]
)
```


```VB

Shell.FindPrinter( _
  [ ByVal sName As BSTR ], _
  [ ByVal sLocation As BSTR ], _
  [ ByVal sModel As BSTR ] _
) As Integer
```





## <a name="parameters"></a><span data-ttu-id="d42d8-106">參數</span><span class="sxs-lookup"><span data-stu-id="d42d8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d42d8-107">*sName* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="d42d8-107">*sName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d42d8-108">類型： **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="d42d8-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="d42d8-109">包含印表機名稱的 **字串** 。</span><span class="sxs-lookup"><span data-stu-id="d42d8-109">A **String** that contains the printer name.</span></span>

</dd> <dt>

<span data-ttu-id="d42d8-110">*sLocation* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="d42d8-110">*sLocation* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d42d8-111">類型： **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="d42d8-111">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="d42d8-112">包含印表機位置的 **字串** 。</span><span class="sxs-lookup"><span data-stu-id="d42d8-112">A **String** that contains the printer location.</span></span>

</dd> <dt>

<span data-ttu-id="d42d8-113">*sModel* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="d42d8-113">*sModel* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d42d8-114">類型： **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="d42d8-114">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="d42d8-115">包含印表機型號的 **字串** 。</span><span class="sxs-lookup"><span data-stu-id="d42d8-115">A **String** that contains the printer model.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d42d8-116">備註</span><span class="sxs-lookup"><span data-stu-id="d42d8-116">Remarks</span></span>

<span data-ttu-id="d42d8-117">如果您將字串指派給一或多個選擇性參數，當顯示 [ **尋找印表機** ] 對話方塊時，它們會在相關聯的編輯控制項中顯示為預設值。</span><span class="sxs-lookup"><span data-stu-id="d42d8-117">If you assign strings to one or more of the optional parameters, they are displayed as default values in the associated edit control when the **Find Printer** dialog box is displayed.</span></span> <span data-ttu-id="d42d8-118">使用者可以接受或覆寫這些值。</span><span class="sxs-lookup"><span data-stu-id="d42d8-118">The user can either accept or override these values.</span></span> <span data-ttu-id="d42d8-119">如果未指派任何值給參數，則相關聯的編輯方塊是空的，而且使用者必須輸入值。</span><span class="sxs-lookup"><span data-stu-id="d42d8-119">If no value is assigned to a parameter, the associated edit box is empty and the user must enter a value.</span></span>

<span data-ttu-id="d42d8-120">Microsoft Visual Basic 目前無法使用這個方法。</span><span class="sxs-lookup"><span data-stu-id="d42d8-120">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="d42d8-121">範例</span><span class="sxs-lookup"><span data-stu-id="d42d8-121">Examples</span></span>

<span data-ttu-id="d42d8-122">下列範例示範如何使用 **FindPrinter** 來顯示特定應用程式的 [ **尋找印表機** ] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="d42d8-122">The following examples show the use of **FindPrinter** to display the **Find Printer** dialog box for a particular application.</span></span> <span data-ttu-id="d42d8-123">JScript、VBScript 和 Visual Basic 會顯示使用方式。</span><span class="sxs-lookup"><span data-stu-id="d42d8-123">Usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="d42d8-124">Jscript：</span><span class="sxs-lookup"><span data-stu-id="d42d8-124">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFindPrinterJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.FindPrinter();
    }
</script>
```



<span data-ttu-id="d42d8-125">VBScript</span><span class="sxs-lookup"><span data-stu-id="d42d8-125">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnFindPrinterVB()
        dim objShell
        dim bReturn

        set objShell = CreateObject("shell.application")
        objShell.FindPrinter()

        set objShell = nothing
    end function
</script>
```



## <a name="requirements"></a><span data-ttu-id="d42d8-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="d42d8-126">Requirements</span></span>



| <span data-ttu-id="d42d8-127">需求</span><span class="sxs-lookup"><span data-stu-id="d42d8-127">Requirement</span></span> | <span data-ttu-id="d42d8-128">值</span><span class="sxs-lookup"><span data-stu-id="d42d8-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d42d8-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d42d8-129">Minimum supported client</span></span><br/> | <span data-ttu-id="d42d8-130">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d42d8-130">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d42d8-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d42d8-131">Minimum supported server</span></span><br/> | <span data-ttu-id="d42d8-132">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d42d8-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="d42d8-133">標頭</span><span class="sxs-lookup"><span data-stu-id="d42d8-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="d42d8-134"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="d42d8-134"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="d42d8-135">Idl</span><span class="sxs-lookup"><span data-stu-id="d42d8-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d42d8-136"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="d42d8-136"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="d42d8-137">DLL</span><span class="sxs-lookup"><span data-stu-id="d42d8-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d42d8-138"><dt>Shell32.dll (5.0 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="d42d8-138"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
