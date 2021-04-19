---
description: '\_SWbemObject 物件的衍生屬性包含字串陣列，這些字串會描述所參考之實例的類別衍生階層架構。'
ms.assetid: 8a4daab0-7d10-4a37-aacd-1f3f499b859a
ms.tgt_platform: multiple
title: 'SWbemObject.Derivation_ 屬性 (>wbemdisp.tlb) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Derivation_
- ISWbemObject.Derivation_
- ISWbemObject.get_Derivation_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 84e7b4e53a1a5544c92bb5116f3f83189789487f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106995852"
---
# <a name="swbemobjectderivation_-property"></a><span data-ttu-id="208b3-103">SWbemObject。衍生 \_ 屬性</span><span class="sxs-lookup"><span data-stu-id="208b3-103">SWbemObject.Derivation\_ property</span></span>

<span data-ttu-id="208b3-104">[**SWbemObject**](swbemobject.md)物件的 **衍生 \_** 屬性包含字串陣列，這些字串會描述所參考之實例的類別衍生階層架構。</span><span class="sxs-lookup"><span data-stu-id="208b3-104">The **Derivation\_** property of the [**SWbemObject**](swbemobject.md) object contains an array of strings that describe the class derivation hierarchy for the instance being referenced.</span></span> <span data-ttu-id="208b3-105">陣列中的第一個元素會定義父類別，而最後一個元素會定義時代類別。</span><span class="sxs-lookup"><span data-stu-id="208b3-105">The first element in the array defines the parent class and the last element defines the dynasty class.</span></span> <span data-ttu-id="208b3-106">這是唯讀的屬性。</span><span class="sxs-lookup"><span data-stu-id="208b3-106">This property is read-only.</span></span>

<span data-ttu-id="208b3-107">如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="208b3-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="208b3-108">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="208b3-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="208b3-109">語法</span><span class="sxs-lookup"><span data-stu-id="208b3-109">Syntax</span></span>


```VB
SWbemObject.Derivation_ As String
```



## <a name="property-value"></a><span data-ttu-id="208b3-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="208b3-110">Property value</span></span>

## <a name="examples"></a><span data-ttu-id="208b3-111">範例</span><span class="sxs-lookup"><span data-stu-id="208b3-111">Examples</span></span>

<span data-ttu-id="208b3-112">下列 VBScript 範例說明如何取出 win32 logicaldisk 的類別階層架構 \_ 。</span><span class="sxs-lookup"><span data-stu-id="208b3-112">The following VBScript sample describes how to retrieve the class hierarchy for win32\_logicaldisk.</span></span>


```VB
on Error resume next

Set c = GetObject("winmgmts://./root/cimv2:win32_logicaldisk")
d = c.Derivation_

for x = LBound(d) to UBound(d)
 WScript.Echo d(x)
Next

if err <> 0 then
 WScript.Echo Err.Description
end if
```



<span data-ttu-id="208b3-113">他的下列 Perl 範例說明如何取出 win32 logicaldisk 的類別階層架構 \_ 。</span><span class="sxs-lookup"><span data-stu-id="208b3-113">he following Perl sample describes how to retrieve the class hierarchy for win32\_logicaldisk.</span></span>


```
use strict;
use Win32::OLE;

my ($C, $D, @collection);

eval {$C = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\cimv2")->
  InstancesOf ("win32_logicaldisk") };
unless ($@) 
{
 @collection = in $C;
 eval {$D = $collection[0]->Derivation_();};
 print "\n";
 unless ($@) 
 {
  print map{"$_\n"} @{$D};
 }
 else
 {
  print STDERR Win32::OLE->LastError, "\n";
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a><span data-ttu-id="208b3-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="208b3-114">Requirements</span></span>



| <span data-ttu-id="208b3-115">需求</span><span class="sxs-lookup"><span data-stu-id="208b3-115">Requirement</span></span> | <span data-ttu-id="208b3-116">值</span><span class="sxs-lookup"><span data-stu-id="208b3-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="208b3-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="208b3-117">Minimum supported client</span></span><br/> | <span data-ttu-id="208b3-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="208b3-118">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="208b3-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="208b3-119">Minimum supported server</span></span><br/> | <span data-ttu-id="208b3-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="208b3-120">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="208b3-121">標頭</span><span class="sxs-lookup"><span data-stu-id="208b3-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="208b3-122"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="208b3-122"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="208b3-123">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="208b3-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="208b3-124"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="208b3-124"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="208b3-125">DLL</span><span class="sxs-lookup"><span data-stu-id="208b3-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="208b3-126"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="208b3-126"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="208b3-127">CLSID</span><span class="sxs-lookup"><span data-stu-id="208b3-127">CLSID</span></span><br/>                    | <span data-ttu-id="208b3-128">CLSID \_ SWbemObject</span><span class="sxs-lookup"><span data-stu-id="208b3-128">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="208b3-129">IID</span><span class="sxs-lookup"><span data-stu-id="208b3-129">IID</span></span><br/>                      | <span data-ttu-id="208b3-130">IID \_ ISWbemObject</span><span class="sxs-lookup"><span data-stu-id="208b3-130">IID\_ISWbemObject</span></span><br/>                                                            |



 

 




