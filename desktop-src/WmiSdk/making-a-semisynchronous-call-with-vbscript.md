---
description: 提供半同步存取功能，以及進行半同步方法呼叫的程式碼範例。
ms.assetid: 3eae38e8-6a63-45c0-99b0-94e25ddbc5a8
ms.tgt_platform: multiple
title: 使用 VBScript 進行半同步呼叫
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e875a269d2cf1cd4e3b40d5c84d42ffb97dc35a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975196"
---
# <a name="making-a-semisynchronous-call-with-vbscript"></a><span data-ttu-id="95e66-103">使用 VBScript 進行半同步呼叫</span><span class="sxs-lookup"><span data-stu-id="95e66-103">Making a Semisynchronous Call with VBScript</span></span>

<span data-ttu-id="95e66-104">某些 WMI 方法可以傳回大型集合，使腳本停止回應。</span><span class="sxs-lookup"><span data-stu-id="95e66-104">Some WMI methods can return large collections, causing scripts to stop responding.</span></span> <span data-ttu-id="95e66-105">在腳本中，會使用 [半同步存取] 為預設值，而 Windows Management Instrumentation (WMI) 針對可傳回大型物件集合的呼叫（例如下列 [**SWbemServices**](swbemservices.md)方法）設定 **wbemFlagReturnImmediately** ： [**InstancesOf**](swbemservices-instancesof.md)、 [**SubclassesOf**](swbemservices-subclassesof.md)、 [**ExecQuery**](swbemservices-execquery.md)、 [**AssociatorsOf**](swbemservices-associatorsof.md)和 [**ReferencesTo**](swbemservices-referencesto.md)。</span><span class="sxs-lookup"><span data-stu-id="95e66-105">In script, semisynchronous access is the default, and Windows Management Instrumentation (WMI) sets **wbemFlagReturnImmediately** for calls that can return large object collections such as the following [**SWbemServices**](swbemservices.md) methods: [**InstancesOf**](swbemservices-instancesof.md), [**SubclassesOf**](swbemservices-subclassesof.md), [**ExecQuery**](swbemservices-execquery.md), [**AssociatorsOf**](swbemservices-associatorsof.md), and [**ReferencesTo**](swbemservices-referencesto.md).</span></span>

<span data-ttu-id="95e66-106">在 *IFlags* 參數中使用 **wbemFlagReturnImmediately** 集的每半使用者存取，也是呼叫的預設值，可以傳回下列 [**SWbemObject**](swbemobject.md)方法的大型物件集： [**\_ 實例**](swbemobject-instances-.md)、子 [**\_ 類別**](swbemobject-subclasses-.md)、 [**associators of \_**](swbemobject-associators-.md)和 [**參考 \_**](swbemobject-references-.md)。</span><span class="sxs-lookup"><span data-stu-id="95e66-106">Semisynchronous access that uses **wbemFlagReturnImmediately** set in the *IFlags* parameter is also the default for calls that can return large object sets for the following [**SWbemObject**](swbemobject.md) methods: [**Instances\_**](swbemobject-instances-.md), [**Subclasses\_**](swbemobject-subclasses-.md), [**Associators\_**](swbemobject-associators-.md), and [**References\_**](swbemobject-references-.md).</span></span>

<span data-ttu-id="95e66-107">若要在處理大型物件集合時減少 WMI 記憶體資源使用量，請在 *IFlags* 參數中包含 **wbemFlagForwardOnly** 的值。</span><span class="sxs-lookup"><span data-stu-id="95e66-107">To reduce the WMI memory resource usage when processing a large collection of objects, include the value of **wbemFlagForwardOnly** in the *IFlags* parameter.</span></span> <span data-ttu-id="95e66-108">使用 **wbemFlagForwardOnly** 會導致 WMI 建立順向列舉值，而不允許倒轉集合並再次存取專案。</span><span class="sxs-lookup"><span data-stu-id="95e66-108">Using **wbemFlagForwardOnly** causes WMI to create a forward-only enumerator that does not allow rewinding the collection and accessing items again.</span></span>

<span data-ttu-id="95e66-109">WMI 會將每個物件的記憶體排除在 **每個** 語句處理物件時。</span><span class="sxs-lookup"><span data-stu-id="95e66-109">WMI eliminates the memory for each object as the **For Each** statement processes an object.</span></span> <span data-ttu-id="95e66-110">在取得集合的呼叫上設定 **wbemFlagForwardOnly** 旗標時，您無法呼叫集合的 **Count** 方法。</span><span class="sxs-lookup"><span data-stu-id="95e66-110">You cannot call the **Count** method for a collection when the **wbemFlagForwardOnly** flag was set on the call that obtained the collection.</span></span> <span data-ttu-id="95e66-111">請注意， *IFlags* 參數預設會針對 [**SWbemServices.ExeCNotificationQuery**](swbemservices-execnotificationquery.md)方法設定 **wbemFlagReturnImmediately** 和 **wbemFlagForwardOnly** 。</span><span class="sxs-lookup"><span data-stu-id="95e66-111">Note that the *IFlags* parameter has **wbemFlagReturnImmediately** and **wbemFlagForwardOnly** set by default for the [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) method.</span></span>

<span data-ttu-id="95e66-112">下列程式描述如何使用 VBScript 進行半執行呼叫。</span><span class="sxs-lookup"><span data-stu-id="95e66-112">The following procedure describes how to use VBScript to make a semisynchronous call.</span></span>

<span data-ttu-id="95e66-113">**在 VBScript 中進行半同步呼叫**</span><span class="sxs-lookup"><span data-stu-id="95e66-113">**To make a semisynchronous call in VBScript**</span></span>

1.  <span data-ttu-id="95e66-114">將 *IFlags* 參數設定為 [wbemFlagReturnImmediately](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum)的值。</span><span class="sxs-lookup"><span data-stu-id="95e66-114">Set the *IFlags* parameter to the value of [wbemFlagReturnImmediately](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum).</span></span>
2.  <span data-ttu-id="95e66-115">使用 *iFlags* 值，對 [**SWbemServices.ExeCQuery**](swbemservices-execquery.md)或 [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md)進行一般同步呼叫。</span><span class="sxs-lookup"><span data-stu-id="95e66-115">Make the normal synchronous call for [**SWbemServices.ExecQuery**](swbemservices-execquery.md) or [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) with the *iFlags* value.</span></span>
3.  <span data-ttu-id="95e66-116">如果您想要將呼叫所傳回的物件視為集合，請使用 **每個** 列舉語法，例如 VBScript。</span><span class="sxs-lookup"><span data-stu-id="95e66-116">If you want to treat the objects returned by the call as a collection, use an enumeration syntax such as VBScript **For Each**.</span></span> <span data-ttu-id="95e66-117">傳回每個物件時，會將它視為集合中的下一個專案來處理。</span><span class="sxs-lookup"><span data-stu-id="95e66-117">As each object is returned, it is processed as the next item in the collection.</span></span>
4.  <span data-ttu-id="95e66-118">將 **wbemFlagReturnImmediately** 的值與 **wbemFlagForwardOnly** 的值結合，以建立順向列舉值。</span><span class="sxs-lookup"><span data-stu-id="95e66-118">Create a forward-only enumerator by combining the value of **wbemFlagReturnImmediately** with the value of **wbemFlagForwardOnly**.</span></span> <span data-ttu-id="95e66-119">這個 OR 運算的十進位值是48。</span><span class="sxs-lookup"><span data-stu-id="95e66-119">The decimal value of this OR operation is 48.</span></span> <span data-ttu-id="95e66-120">這些常數定義于 Visual Basic 的 >wbemdisp.tlb .tlb 類型程式庫中。</span><span class="sxs-lookup"><span data-stu-id="95e66-120">These constants are defined in the wbemdisp.tlb type library for Visual Basic.</span></span> <span data-ttu-id="95e66-121">大部分的指令碼語言都會使用數值或定義常數。</span><span class="sxs-lookup"><span data-stu-id="95e66-121">Most scripting languages use the numeric value or define a constant.</span></span> <span data-ttu-id="95e66-122">如需詳細資訊，請參閱 [WbemFlagEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum)。</span><span class="sxs-lookup"><span data-stu-id="95e66-122">For more information, see [WbemFlagEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum).</span></span>

<span data-ttu-id="95e66-123">下列程式碼範例示範如何進行半執行方法呼叫。</span><span class="sxs-lookup"><span data-stu-id="95e66-123">The following code example shows how to make a semisynchronous method call.</span></span> <span data-ttu-id="95e66-124">如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。</span><span class="sxs-lookup"><span data-stu-id="95e66-124">For more information, see [Calling a Method](calling-a-method.md).</span></span>


```VB
wbemFlagReturnImmediately = 16
wbemFlagForwardOnly = 32
IFlags = wbemFlagReturnImmediately + wbemFlagForwardOnly
WScript.Echo IFlags
Set objWMIService = GetObject("winmgmts:root\cimv2")
' Query for all the Win32_Process objects on the 
'     local computer and use forward-only enumerator
Set colProcesses = objWMIService.ExecQuery("SELECT Name FROM Win32_Process",,IFlags)
' Receive each object as it arrives
For Each objProcess in colProcesses
    WScript.Echo objProcess.Name
Next
```



## <a name="related-topics"></a><span data-ttu-id="95e66-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="95e66-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="95e66-126">呼叫方法</span><span class="sxs-lookup"><span data-stu-id="95e66-126">Calling a Method</span></span>](calling-a-method.md)
</dt> </dl>

 

 



