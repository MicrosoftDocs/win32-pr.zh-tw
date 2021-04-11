---
description: 當系統或網路效能將會藉由查詢大型資料群組而受到影響時，非同步查詢（較複雜的寫入）是慣用的查詢類型。
ms.assetid: b382610a-dac9-4d31-b756-aa84d16f0234
ms.tgt_platform: multiple
title: 叫用非同步查詢
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14a0e297c6a1955d0006d888fc95f5e827f5cb75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852631"
---
# <a name="invoking-an-asynchronous-query"></a><span data-ttu-id="2df60-103">叫用非同步查詢</span><span class="sxs-lookup"><span data-stu-id="2df60-103">Invoking an Asynchronous Query</span></span>

<span data-ttu-id="2df60-104">當系統或網路效能將會藉由查詢大型資料群組而受到影響時，非同步查詢（較複雜的寫入）是慣用的查詢類型。</span><span class="sxs-lookup"><span data-stu-id="2df60-104">An asynchronous query, while somewhat more complex to write, is the preferred type of query when system or network performance will be affected by querying a large group of data.</span></span> <span data-ttu-id="2df60-105">在腳本中，建立 [**SWbemSink**](swbemsink.md) 物件和副程式來處理接收接收的事件，是基本查詢以外的唯一額外工作。</span><span class="sxs-lookup"><span data-stu-id="2df60-105">In script, creating an [**SWbemSink**](swbemsink.md) object and subroutines to handle the events that the sink could receive are the only additional tasks beyond the basic query.</span></span>

> [!Note]  
> <span data-ttu-id="2df60-106">由於接收端的回呼可能不會與用戶端所需的驗證層級傳回，因此建議您使用 [半同步] 而非 [非同步通訊]。</span><span class="sxs-lookup"><span data-stu-id="2df60-106">Because the callback to the sink might not be returned at the same authentication level as the client requires, it is recommended that you use semisynchronous instead of asynchronous communication.</span></span> <span data-ttu-id="2df60-107">如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。</span><span class="sxs-lookup"><span data-stu-id="2df60-107">For more information, see [Calling a Method](calling-a-method.md).</span></span>

 

<span data-ttu-id="2df60-108">下列縮寫腳本會查詢本機電腦上的所有資料檔案。</span><span class="sxs-lookup"><span data-stu-id="2df60-108">The following abbreviated script queries for all of the data files on the local machine.</span></span> <span data-ttu-id="2df60-109">如果對網路上的所有機器執行此查詢，則此查詢可能會花費大量的時間。</span><span class="sxs-lookup"><span data-stu-id="2df60-109">This query could take an excessive amount of time if it were executed for all of the machines on a network.</span></span> <span data-ttu-id="2df60-110">已設定 [**SWbemSink**](swbemsink.md) 物件，而唯一處理的事件是 OnCompleted 事件。</span><span class="sxs-lookup"><span data-stu-id="2df60-110">An [**SWbemSink**](swbemsink.md) object is set up and the only event that is handled is the OnCompleted event.</span></span>


```VB
Sub SINK_OnCompleted(iHResult, objErrorObject, objAsyncContext)
    WScript.Echo "Asynchronous operation is done."
End Sub

Set service = GetObject("winmgmts:")
Set sink = WScript.CreateObject("WbemScripting.SWbemSink","SINK_")
service.ExecQueryAsync sink, "SELECT * FROM Win32_DataFile"
WScript.Echo "Waiting for instances."
sink.Cancel()
set sink= Nothing
```



<span data-ttu-id="2df60-111">如需有關在腳本中建立異步方法呼叫的詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。</span><span class="sxs-lookup"><span data-stu-id="2df60-111">For detailed information about constructing asynchronous method calls in script, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="2df60-112">在 c + + 應用程式中，非同步查詢會產生個別的進程來接收查詢資料。</span><span class="sxs-lookup"><span data-stu-id="2df60-112">In C++ applications, an asynchronous query spawns a separate process to receive query data.</span></span> <span data-ttu-id="2df60-113">非同步查詢比同步查詢更為複雜，因為您必須撰寫多執行緒應用程式的程式碼。</span><span class="sxs-lookup"><span data-stu-id="2df60-113">An asynchronous query is more complex than a synchronous query, as you must code a multithreaded application.</span></span> <span data-ttu-id="2df60-114">不過，非同步查詢不會獨佔您應用程式的主執行緒。</span><span class="sxs-lookup"><span data-stu-id="2df60-114">However, an asynchronous query does not monopolize the main thread of your application.</span></span>

<span data-ttu-id="2df60-115">下列程式描述如何在 c + + 中執行非同步查詢。</span><span class="sxs-lookup"><span data-stu-id="2df60-115">The following procedure describes how to perform an asynchronous query in C++.</span></span>

<span data-ttu-id="2df60-116">**若要在 c + + 中執行非同步查詢**</span><span class="sxs-lookup"><span data-stu-id="2df60-116">**To perform an asynchronous query in C++**</span></span>

1.  <span data-ttu-id="2df60-117">執行 **IWbemSink** 物件。</span><span class="sxs-lookup"><span data-stu-id="2df60-117">Implement an **IWbemSink** object.</span></span>

    <span data-ttu-id="2df60-118">**IWbemSink** 物件會接收非同步作業的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="2df60-118">An **IWbemSink** object receives information about an asynchronous operation.</span></span>

2.  <span data-ttu-id="2df60-119">在對 [**IWbemServices：： ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync)的呼叫中描述您的查詢。</span><span class="sxs-lookup"><span data-stu-id="2df60-119">Describe your query in a call to [**IWbemServices::ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync).</span></span>

    <span data-ttu-id="2df60-120">WMI 會立即將查詢 CIM 的程式移至另一個執行緒，並釋出針對另一項工作執行查詢的執行緒。</span><span class="sxs-lookup"><span data-stu-id="2df60-120">WMI immediately moves the process that queries the CIM to another thread and frees up the thread that executed the query for another task.</span></span>

3.  <span data-ttu-id="2df60-121">等候 WMI 呼叫 [**IWbemObjectSink：：指示**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) 方法。</span><span class="sxs-lookup"><span data-stu-id="2df60-121">Wait for WMI to call the [**IWbemObjectSink::Indicate**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) method.</span></span>

    <span data-ttu-id="2df60-122">完成時，WMI 呼叫會 [**指出**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) 您的應用程式已完成查詢。</span><span class="sxs-lookup"><span data-stu-id="2df60-122">When finished, WMI calls [**Indicate**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) to signal your application that the query is complete.</span></span> <span data-ttu-id="2df60-123">WMI 也會將查詢的結果以指標的形式傳回給 [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) 介面指標。</span><span class="sxs-lookup"><span data-stu-id="2df60-123">WMI also returns results of the query to the sink as a pointer to an [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) interface pointer.</span></span> <span data-ttu-id="2df60-124">如同同步查詢，請使用指標來存取組成查詢結果的物件。</span><span class="sxs-lookup"><span data-stu-id="2df60-124">As with a synchronous query, use the pointer to access the objects that make up the result of your query.</span></span>

<span data-ttu-id="2df60-125">下列程式碼範例不會進行編譯而不會發生錯誤，因為尚未定義類別 QuerySink。</span><span class="sxs-lookup"><span data-stu-id="2df60-125">The following code example does not compile without an error because the class QuerySink has not been defined.</span></span> <span data-ttu-id="2df60-126">如需 QuerySink 類別的定義，請參閱 [**IWbemObjectSink**](iwbemobjectsink.md)。</span><span class="sxs-lookup"><span data-stu-id="2df60-126">For the definition of the QuerySink class, see [**IWbemObjectSink**](iwbemobjectsink.md).</span></span> <span data-ttu-id="2df60-127">程式碼範例也需要下列參考和 \# 包含語句。</span><span class="sxs-lookup"><span data-stu-id="2df60-127">The code example also requires the following reference and \#include statements.</span></span>


```C++
#include <iostream>
using namespace std;
#include <wbemidl.h>
```



<span data-ttu-id="2df60-128">下列程式碼範例示範如何發出非同步呼叫來發出查詢。</span><span class="sxs-lookup"><span data-stu-id="2df60-128">The following code example shows how to make an asynchronous call to issue a query.</span></span>


```C++
void ExecQuery(IWbemServices *pSvc)
{
    // Create a new sink object.
    QuerySink *pSink = new QuerySink;

    // Initialize the query and query language.
    BSTR strQuery = SysAllocString(L"SELECT * FROM ClassName");
    BSTR strQueryLang = SysAllocString(L"WQL");
    
    // Issue the query.
    HRESULT hRes = pSvc->ExecQueryAsync(strQueryLang, strQuery, 0,
        NULL, pSink);

    // Clean up.
    SysFreeString(strQuery);
    SysFreeString(strQueryLang);
    
    if (hRes)
    {
        printf("ExecQueryAsync failed with = 0x%X\n", hRes);
        return;
    }
    
    printf("Completed.\n");
}
```



<span data-ttu-id="2df60-129">如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。</span><span class="sxs-lookup"><span data-stu-id="2df60-129">For more information, see [Calling a Method](calling-a-method.md).</span></span>

 

 



