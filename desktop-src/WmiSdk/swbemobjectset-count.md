---
description: 使用 Swbemobjectset 搭配使用物件的 Count 屬性，判斷 Swbemobjectset 搭配使用集合中有多少個專案。 這是唯讀的屬性。
ms.assetid: ad3d1265-a11e-4962-b1f3-60092d2f79ef
ms.tgt_platform: multiple
title: 'Swbemobjectset 搭配使用： Count 屬性 (>wbemdisp.tlb .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectSet.Count
- ISWbemObjectSet.Count
- ISWbemObjectSet.get_Count
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 3154e22bbdbc75080ceebdf8b1eef602cf5c3be3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988440"
---
# <a name="swbemobjectsetcount-property"></a><span data-ttu-id="32779-104">Swbemobjectset 搭配使用 Count 屬性</span><span class="sxs-lookup"><span data-stu-id="32779-104">SWbemObjectSet.Count property</span></span>

<span data-ttu-id="32779-105">使用 [**swbemobjectset 搭配使用**](swbemobjectset.md)物件的 **Count** 屬性，判斷 **swbemobjectset 搭配使用** 集合中有多少個專案。</span><span class="sxs-lookup"><span data-stu-id="32779-105">Use the **Count** property of the [**SWbemObjectSet**](swbemobjectset.md) object to determine how many items are in an **SWbemObjectSet** collection.</span></span> <span data-ttu-id="32779-106">這是唯讀的屬性。</span><span class="sxs-lookup"><span data-stu-id="32779-106">This property is read-only.</span></span>

<span data-ttu-id="32779-107">如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="32779-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="32779-108">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="32779-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="32779-109">語法</span><span class="sxs-lookup"><span data-stu-id="32779-109">Syntax</span></span>


```VB
SWbemObjectSet.Count As Integer
```



## <a name="property-value"></a><span data-ttu-id="32779-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="32779-110">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="32779-111">備註</span><span class="sxs-lookup"><span data-stu-id="32779-111">Remarks</span></span>

<span data-ttu-id="32779-112">使用 Count 時要特別注意的一點是，WMI 不會將集合中的專案數目維持在執行中的計數。</span><span class="sxs-lookup"><span data-stu-id="32779-112">One thing to be careful of when using Count is that WMI does not keep a running tally of the number of items in a collection.</span></span> <span data-ttu-id="32779-113">如果您要求集合的計數，WMI 無法立即以數位回應;相反地，它必須對專案進行計算，以列舉整個集合。</span><span class="sxs-lookup"><span data-stu-id="32779-113">If you request Count for a collection, WMI cannot instantly respond with a number; instead, it must literally count the items, enumerating the entire collection.</span></span> <span data-ttu-id="32779-114">對於具有相當少專案的集合（例如服務），此列舉可能需要不到一秒。</span><span class="sxs-lookup"><span data-stu-id="32779-114">For a collection that has relatively few items, such as services, this enumeration likely takes less than a second.</span></span> <span data-ttu-id="32779-115">不過，在事件記錄檔集合中計算事件數目可能需要更長的時間。</span><span class="sxs-lookup"><span data-stu-id="32779-115">Counting the number of events in an event log collection, however, can take considerably longer.</span></span>

<span data-ttu-id="32779-116">然後，假設您想要顯示集合中每個事件的屬性值。</span><span class="sxs-lookup"><span data-stu-id="32779-116">And then suppose you want to display the property values for every event in the collection.</span></span> <span data-ttu-id="32779-117">若是如此，WMI 就必須第二次列舉整個集合。</span><span class="sxs-lookup"><span data-stu-id="32779-117">If so, WMI will have to enumerate the entire collection a second time.</span></span>

> [!Note]  
> <span data-ttu-id="32779-118">如果您嘗試從方法傳回的 [**swbemobjectset 搭配使用**](swbemobjectset.md) 物件取得這個屬性，而該方法的指定旗標包含在 wbemFlagForwardOnly 旗標中，則您會收到 wbemErrFailed 錯誤。</span><span class="sxs-lookup"><span data-stu-id="32779-118">If you attempt to get this property from an [**SWbemObjectSet**](swbemobjectset.md) object that is returned from a method where the specified flags are included the wbemFlagForwardOnly flag, you will get an wbemErrFailed error.</span></span>

 

## <a name="examples"></a><span data-ttu-id="32779-119">範例</span><span class="sxs-lookup"><span data-stu-id="32779-119">Examples</span></span>

<span data-ttu-id="32779-120">在大部分的情況下，您只會對 Swbemobjectset 搭配使用列舉集合本身所包含的所有物件。</span><span class="sxs-lookup"><span data-stu-id="32779-120">For the most part, the only thing you will ever do with an SWbemObjectSet is enumerate all the objects contained within the collection itself.</span></span> <span data-ttu-id="32779-121">不過，計數計數在系統管理腳本中很有用。</span><span class="sxs-lookup"><span data-stu-id="32779-121">However, the Count Count that can be useful in system administration scripting.</span></span> <span data-ttu-id="32779-122">顧名思義，Count 會告訴您集合中的專案數。</span><span class="sxs-lookup"><span data-stu-id="32779-122">As the name implies, Count tells you the number of items in the collection.</span></span> <span data-ttu-id="32779-123">例如，此腳本會取得電腦上安裝的所有服務的集合，然後回顯找到的服務總數：</span><span class="sxs-lookup"><span data-stu-id="32779-123">For example, this script retrieves a collection of all the services installed on a computer and then echoes the total number of services found:</span></span>


```VB
strComputer = "."
Set objSWbemServices = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")
Set colSWbemObjectSet = objSWbemServices.InstancesOf("Win32_Service")
Wscript.Echo "Services installed on target computer: " & colSWbemObjectSet.Count

```



<span data-ttu-id="32779-124">計數會很有用，因為它可以告訴您電腦上是否有特定的實例可供使用。</span><span class="sxs-lookup"><span data-stu-id="32779-124">What makes Count useful is that it can tell you whether a specific instance is available on a computer.</span></span> <span data-ttu-id="32779-125">例如，此腳本會在名稱為 W3SVC 的電腦上，取得所有服務的集合。</span><span class="sxs-lookup"><span data-stu-id="32779-125">For example, this script retrieves a collection of all the services on a computer that have the Name W3SVC.</span></span> <span data-ttu-id="32779-126">如果計數為 0 (且有效的集合沒有任何實例) ，這表示電腦上未安裝 W3SVC 服務。</span><span class="sxs-lookup"><span data-stu-id="32779-126">If the Count is 0 (and it is valid for collections to have no instances), that means the W3SVC service is not installed on the computer.</span></span>


```VB
strComputer = "."
Set objSWbemServices = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")
Set colSWbemObjectSet = objSWbemServices.ExecQuery _
    ("SELECT * FROM Win32_Service WHERE Name='w3svc'")
If colSWbemObjectSet.Count = 0 Then
    Wscript.Echo "W3SVC service is not installed on target computer."
Else
    For Each objSWbemObject In colSWbemObjectSet
        ' Perform task on World Wide Web Publishing service.
    Next
End If
```



## <a name="requirements"></a><span data-ttu-id="32779-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="32779-127">Requirements</span></span>



| <span data-ttu-id="32779-128">需求</span><span class="sxs-lookup"><span data-stu-id="32779-128">Requirement</span></span> | <span data-ttu-id="32779-129">值</span><span class="sxs-lookup"><span data-stu-id="32779-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="32779-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="32779-130">Minimum supported client</span></span><br/> | <span data-ttu-id="32779-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="32779-131">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="32779-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="32779-132">Minimum supported server</span></span><br/> | <span data-ttu-id="32779-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="32779-133">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="32779-134">標頭</span><span class="sxs-lookup"><span data-stu-id="32779-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="32779-135"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="32779-135"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="32779-136">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="32779-136">Type library</span></span><br/>             | <dl> <span data-ttu-id="32779-137"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="32779-137"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="32779-138">DLL</span><span class="sxs-lookup"><span data-stu-id="32779-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="32779-139"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="32779-139"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="32779-140">CLSID</span><span class="sxs-lookup"><span data-stu-id="32779-140">CLSID</span></span><br/>                    | <span data-ttu-id="32779-141">CLSID \_ swbemobjectset 搭配使用</span><span class="sxs-lookup"><span data-stu-id="32779-141">CLSID\_SWbemObjectSet</span></span><br/>                                                        |
| <span data-ttu-id="32779-142">IID</span><span class="sxs-lookup"><span data-stu-id="32779-142">IID</span></span><br/>                      | <span data-ttu-id="32779-143">IID \_ ISWbemObjectSet</span><span class="sxs-lookup"><span data-stu-id="32779-143">IID\_ISWbemObjectSet</span></span><br/>                                                         |



 

 




