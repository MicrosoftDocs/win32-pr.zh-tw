---
description: FindPrinter 方法-顯示 [尋找印表機] 對話方塊。
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
ms.openlocfilehash: 17d04b60de2b52ca3d2f17fbdccf7de93ac095b3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104306"
---
# <a name="shellfindprinter-method"></a><span data-ttu-id="a42f5-103">FindPrinter 方法</span><span class="sxs-lookup"><span data-stu-id="a42f5-103">Shell.FindPrinter method</span></span>

<span data-ttu-id="a42f5-104">顯示 [ **尋找印表機** ] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="a42f5-104">Displays the **Find Printer** dialog box.</span></span>

## <a name="syntax"></a><span data-ttu-id="a42f5-105">語法</span><span class="sxs-lookup"><span data-stu-id="a42f5-105">Syntax</span></span>


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





## <a name="parameters"></a><span data-ttu-id="a42f5-106">參數</span><span class="sxs-lookup"><span data-stu-id="a42f5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a42f5-107">*sName* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="a42f5-107">*sName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a42f5-108">類型： **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="a42f5-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="a42f5-109">包含印表機名稱的 **字串** 。</span><span class="sxs-lookup"><span data-stu-id="a42f5-109">A **String** that contains the printer name.</span></span>

</dd> <dt>

<span data-ttu-id="a42f5-110">*sLocation* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="a42f5-110">*sLocation* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a42f5-111">類型： **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="a42f5-111">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="a42f5-112">包含印表機位置的 **字串** 。</span><span class="sxs-lookup"><span data-stu-id="a42f5-112">A **String** that contains the printer location.</span></span>

</dd> <dt>

<span data-ttu-id="a42f5-113">*sModel* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="a42f5-113">*sModel* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a42f5-114">類型： **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="a42f5-114">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="a42f5-115">包含印表機型號的 **字串** 。</span><span class="sxs-lookup"><span data-stu-id="a42f5-115">A **String** that contains the printer model.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a42f5-116">備註</span><span class="sxs-lookup"><span data-stu-id="a42f5-116">Remarks</span></span>

<span data-ttu-id="a42f5-117">如果您將字串指派給一或多個選擇性參數，當顯示 [ **尋找印表機** ] 對話方塊時，它們會在相關聯的編輯控制項中顯示為預設值。</span><span class="sxs-lookup"><span data-stu-id="a42f5-117">If you assign strings to one or more of the optional parameters, they are displayed as default values in the associated edit control when the **Find Printer** dialog box is displayed.</span></span> <span data-ttu-id="a42f5-118">使用者可以接受或覆寫這些值。</span><span class="sxs-lookup"><span data-stu-id="a42f5-118">The user can either accept or override these values.</span></span> <span data-ttu-id="a42f5-119">如果未指派任何值給參數，則相關聯的編輯方塊是空的，而且使用者必須輸入值。</span><span class="sxs-lookup"><span data-stu-id="a42f5-119">If no value is assigned to a parameter, the associated edit box is empty and the user must enter a value.</span></span>

<span data-ttu-id="a42f5-120">Microsoft Visual Basic 目前無法使用這個方法。</span><span class="sxs-lookup"><span data-stu-id="a42f5-120">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="a42f5-121">範例</span><span class="sxs-lookup"><span data-stu-id="a42f5-121">Examples</span></span>

<span data-ttu-id="a42f5-122">下列範例示範如何使用 **FindPrinter** 來顯示特定應用程式的 [ **尋找印表機** ] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="a42f5-122">The following examples show the use of **FindPrinter** to display the **Find Printer** dialog box for a particular application.</span></span> <span data-ttu-id="a42f5-123">JScript、VBScript 和 Visual Basic 會顯示使用方式。</span><span class="sxs-lookup"><span data-stu-id="a42f5-123">Usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="a42f5-124">Jscript：</span><span class="sxs-lookup"><span data-stu-id="a42f5-124">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFindPrinterJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.FindPrinter();
    }
</script>
```



<span data-ttu-id="a42f5-125">VBScript</span><span class="sxs-lookup"><span data-stu-id="a42f5-125">VBScript:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="a42f5-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="a42f5-126">Requirements</span></span>



| <span data-ttu-id="a42f5-127">需求</span><span class="sxs-lookup"><span data-stu-id="a42f5-127">Requirement</span></span> | <span data-ttu-id="a42f5-128">值</span><span class="sxs-lookup"><span data-stu-id="a42f5-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a42f5-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a42f5-129">Minimum supported client</span></span><br/> | <span data-ttu-id="a42f5-130">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a42f5-130">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a42f5-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a42f5-131">Minimum supported server</span></span><br/> | <span data-ttu-id="a42f5-132">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a42f5-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="a42f5-133">標頭</span><span class="sxs-lookup"><span data-stu-id="a42f5-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="a42f5-134"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="a42f5-134"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="a42f5-135">Idl</span><span class="sxs-lookup"><span data-stu-id="a42f5-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a42f5-136"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="a42f5-136"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="a42f5-137">DLL</span><span class="sxs-lookup"><span data-stu-id="a42f5-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a42f5-138"><dt>Shell32.dll (5.0 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="a42f5-138"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
