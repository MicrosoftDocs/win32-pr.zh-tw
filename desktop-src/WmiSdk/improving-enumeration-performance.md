---
description: 列舉通常會使用大量的系統資源。
ms.assetid: 4163e6c2-4ee3-4906-b297-618509666c90
ms.tgt_platform: multiple
title: 改善列舉效能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df2554e9e1df2f2ece58f5703d6099d84acbe01c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193867"
---
# <a name="improving-enumeration-performance"></a><span data-ttu-id="fdb17-103">改善列舉效能</span><span class="sxs-lookup"><span data-stu-id="fdb17-103">Improving Enumeration Performance</span></span>

<span data-ttu-id="fdb17-104">列舉通常會使用大量的系統資源。</span><span class="sxs-lookup"><span data-stu-id="fdb17-104">Enumerations tend to use a significant amount of system resources.</span></span> <span data-ttu-id="fdb17-105">因此，如果您打算在大型群組上執行列舉，您應該嘗試將 WMI 列舉程式優化。</span><span class="sxs-lookup"><span data-stu-id="fdb17-105">Therefore, you should try to optimize the WMI enumeration process if you plan on performing enumerations on a large group.</span></span> <span data-ttu-id="fdb17-106">腳本也可以使用查詢，以避免「針對每個 ...」作業使用大型集合的效能降低。</span><span class="sxs-lookup"><span data-stu-id="fdb17-106">Scripts can also use a query to avoid performance degradation in "For each….Next" operations with a large set.</span></span> <span data-ttu-id="fdb17-107">如需詳細資訊，請參閱 [查詢 WMI](querying-wmi.md)。</span><span class="sxs-lookup"><span data-stu-id="fdb17-107">For more information, see [Querying WMI](querying-wmi.md).</span></span>

<span data-ttu-id="fdb17-108">下列程式描述如何改善列舉效能。</span><span class="sxs-lookup"><span data-stu-id="fdb17-108">The following procedure describes how to improve enumeration performance.</span></span>

<span data-ttu-id="fdb17-109">**改善列舉效能**</span><span class="sxs-lookup"><span data-stu-id="fdb17-109">**To improve enumeration performance**</span></span>

1.  <span data-ttu-id="fdb17-110">將 *lFlags* 參數設定為允許在每次傳遞時從 WMI 中捨棄每個專案的列舉值，以允許最半傳回資料。</span><span class="sxs-lookup"><span data-stu-id="fdb17-110">Set the *lFlags* parameter to allow semisynchronous return of the data with an enumerator that discards each item from WMI as it is delivered.</span></span> <span data-ttu-id="fdb17-111">如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。</span><span class="sxs-lookup"><span data-stu-id="fdb17-111">For more information, see [Calling a Method](calling-a-method.md).</span></span>

    <span data-ttu-id="fdb17-112">下列 c + + 程式碼範例示範如何使用 **WBEM \_ 旗 \_ \_** 標，傳回立即和 **WBEM 旗標順 \_ \_ 向 \_** 旗標。</span><span class="sxs-lookup"><span data-stu-id="fdb17-112">The following C++ code example shows how to use the **WBEM\_FLAG\_RETURN\_IMMEDIATE** and **WBEM\_FLAG\_FORWARD\_ONLY** flags.</span></span>

    `WBEM_FLAG_RETURN_IMMEDIATE | WBEM_FLAG_FORWARD_ONLY`

    <span data-ttu-id="fdb17-113">在 VBScript 或 Visual Basic 中，請使用 [WbemFlagEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum)中的腳本旗標 **WbemFlagReturnImmediately** 和 **WbemFlagForwardOnly** 。</span><span class="sxs-lookup"><span data-stu-id="fdb17-113">In VBScript or Visual Basic, use the scripting flags **WbemFlagReturnImmediately** and **WbemFlagForwardOnly** from [WbemFlagEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum).</span></span> <span data-ttu-id="fdb17-114">這些旗標的合併值是十進位48。</span><span class="sxs-lookup"><span data-stu-id="fdb17-114">The combined value of these flags is decimal 48.</span></span>

    <span data-ttu-id="fdb17-115">腳本和參數旗標會導致下列行為：</span><span class="sxs-lookup"><span data-stu-id="fdb17-115">The scripting and parameter flags cause the following behavior:</span></span>

    -   <span data-ttu-id="fdb17-116">WBEM 旗標會傳回 **\_ \_ \_ 立即** 或 **wbemFlagReturnImmediately** 旗標要求的最半行為。</span><span class="sxs-lookup"><span data-stu-id="fdb17-116">The **WBEM\_FLAG\_RETURN\_IMMEDIATE** or **wbemFlagReturnImmediately** flag requests semisynchronous behavior.</span></span> <span data-ttu-id="fdb17-117">建立列舉值的呼叫會立即傳回。</span><span class="sxs-lookup"><span data-stu-id="fdb17-117">The call to create the enumerator returns immediately.</span></span> <span data-ttu-id="fdb17-118">然後，您可以開始遍歷您收到的物件集。</span><span class="sxs-lookup"><span data-stu-id="fdb17-118">You can then begin to traverse the object set that you receive.</span></span>
    -   <span data-ttu-id="fdb17-119">**WBEM \_ 旗標 \_ \_ 僅向前** 旗標或 **wbemFlagForwardOnly** 旗標會要求您無法倒轉的列舉值。</span><span class="sxs-lookup"><span data-stu-id="fdb17-119">The **WBEM\_FLAG\_FORWARD\_ONLY** flag or **wbemFlagForwardOnly** flag requests an enumerator that you cannot rewind.</span></span> <span data-ttu-id="fdb17-120">也就是說，在您查看物件之後，WMI 可以釋放物件。</span><span class="sxs-lookup"><span data-stu-id="fdb17-120">That is, WMI can release an object after you view the object.</span></span>

    <span data-ttu-id="fdb17-121">在列舉很大且應用程式非常快速的情況下，使用順向列舉值搭配半同步處理可讓 WMI 保持較少的物件，進而大幅增加回應時間和記憶體效能。</span><span class="sxs-lookup"><span data-stu-id="fdb17-121">In situations where the enumeration is large and the application is very fast, using forward-only enumerators with semisynchronous processing allows WMI to hold on to far fewer objects, thereby increasing response time and memory performance significantly.</span></span>

    <span data-ttu-id="fdb17-122">下列 VBScript 程式碼範例示範如何使用合併的 **wbemFlagReturnImmediately** 和 **wbemFlagForwardOnly** 旗標來進行呼叫，以從事件記錄檔取得事件的集合。</span><span class="sxs-lookup"><span data-stu-id="fdb17-122">The following VBScript code example shows how to make a call using the combined **wbemFlagReturnImmediately** and **wbemFlagForwardOnly** flags to obtain a collection of events from an event log.</span></span>

    ```VB
    Set Events = GetObject("winmgmts:").ExecQuery _
         ("SELECT * FROM Win32_NTLogEvent " _
          & "WHERE Logfile = 'System'",,48)
    ```

    

2.  <span data-ttu-id="fdb17-123">可能的話，請避免在 c + + 或 [**SWbemServices InstancesOf**](swbemservices-instancesof.md)中使用 [**CreateInstanceEnum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum) ，而改為使用 **ExecQuery**。</span><span class="sxs-lookup"><span data-stu-id="fdb17-123">Whenever possible, avoid using [**CreateInstanceEnum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum) in C++ or [**SWbemServices.InstancesOf**](swbemservices-instancesof.md), and instead use **ExecQuery**.</span></span>

    <span data-ttu-id="fdb17-124">**ExecQuery** 方法會使用資料庫技術來查詢 wmi，而 [**CreateInstanceEnum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum)或 [**SWbemServices**](swbemservices-instancesof.md)則會列舉 wmi 物件。</span><span class="sxs-lookup"><span data-stu-id="fdb17-124">The **ExecQuery** method queries WMI using database technologies, while [**CreateInstanceEnum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum) or [**SWbemServices.InstancesOf**](swbemservices-instancesof.md) enumerates WMI objects.</span></span> <span data-ttu-id="fdb17-125">具體而言， **ExecQuery** 可以要求列舉方法無法進行的特定資料子集。</span><span class="sxs-lookup"><span data-stu-id="fdb17-125">Specifically, **ExecQuery** can request specific subsets of data that the enumerating methods cannot.</span></span>

    <span data-ttu-id="fdb17-126">由於某些提供者沒有查詢功能，因此 WMI 提供「後篩選」功能，可讓 WMI 捨棄未滿足查詢規格的實例。</span><span class="sxs-lookup"><span data-stu-id="fdb17-126">Because some providers do not have querying capabilities, WMI provides a "post filter" feature that allows WMI to discard instances that do not fulfill a query's specifications.</span></span> <span data-ttu-id="fdb17-127">特定提供者是否可利用這項功能，是由提供者的作者所決定。</span><span class="sxs-lookup"><span data-stu-id="fdb17-127">Whether a particular provider takes advantage of this feature is up to the provider author.</span></span>

3.  <span data-ttu-id="fdb17-128">使用不同的查詢進行實驗，以判斷可提供最佳效能的方式。</span><span class="sxs-lookup"><span data-stu-id="fdb17-128">Experiment with different queries to determine what gives you the best performance.</span></span>

    <span data-ttu-id="fdb17-129">例如，WMI 很少會有效率地使用 Prop1 格式的 **WHERE** 子句來處理查詢 < "x"。</span><span class="sxs-lookup"><span data-stu-id="fdb17-129">For example, WMI seldom efficiently processes queries with **WHERE** clauses of the form Prop1 < "x".</span></span> <span data-ttu-id="fdb17-130">相反地，WMI 通常會有效率地處理 KeyProp1 = "x" 形式的查詢。</span><span class="sxs-lookup"><span data-stu-id="fdb17-130">In contrast, WMI normally processes queries of the form KeyProp1 = "x" efficiently.</span></span>

<span data-ttu-id="fdb17-131">如需詳細資訊，請參閱 [列舉 WMI](enumerating-wmi.md)。</span><span class="sxs-lookup"><span data-stu-id="fdb17-131">For more information, see [Enumerating WMI](enumerating-wmi.md).</span></span>

 

 



