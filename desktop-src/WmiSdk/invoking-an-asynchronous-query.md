---
description: 當系統或網路效能將會藉由查詢大型資料群組而受到影響時，非同步查詢（較複雜的寫入）是慣用的查詢類型。
ms.assetid: b382610a-dac9-4d31-b756-aa84d16f0234
ms.tgt_platform: multiple
title: 叫用非同步查詢
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52ae188e3826562b1de68357db34dca6cea60a40e4be07c16946b13ed3eb3007
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118993068"
---
# <a name="invoking-an-asynchronous-query"></a>叫用非同步查詢

當系統或網路效能將會藉由查詢大型資料群組而受到影響時，非同步查詢（較複雜的寫入）是慣用的查詢類型。 在腳本中，建立 [**SWbemSink**](swbemsink.md) 物件和副程式來處理接收接收的事件，是基本查詢以外的唯一額外工作。

> [!Note]  
> 由於接收端的回呼可能不會與用戶端所需的驗證層級傳回，因此建議您使用 [半同步] 而非 [非同步通訊]。 如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。

 

下列縮寫腳本會查詢本機電腦上的所有資料檔案。 如果對網路上的所有機器執行此查詢，則此查詢可能會花費大量的時間。 已設定 [**SWbemSink**](swbemsink.md) 物件，而唯一處理的事件是 OnCompleted 事件。


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



如需有關在腳本中建立異步方法呼叫的詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。

在 c + + 應用程式中，非同步查詢會產生個別的進程來接收查詢資料。 非同步查詢比同步查詢更為複雜，因為您必須撰寫多執行緒應用程式的程式碼。 不過，非同步查詢不會獨佔您應用程式的主執行緒。

下列程式描述如何在 c + + 中執行非同步查詢。

**若要在 c + + 中執行非同步查詢**

1.  執行 **IWbemSink** 物件。

    **IWbemSink** 物件會接收非同步作業的相關資訊。

2.  在對 [**IWbemServices：： ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync)的呼叫中描述您的查詢。

    WMI 會立即將查詢 CIM 的程式移至另一個執行緒，並釋出針對另一項工作執行查詢的執行緒。

3.  等候 WMI 呼叫 [**IWbemObjectSink：：指示**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) 方法。

    完成時，WMI 呼叫會 [**指出**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) 您的應用程式已完成查詢。 WMI 也會將查詢的結果以指標的形式傳回給 [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) 介面指標。 如同同步查詢，請使用指標來存取組成查詢結果的物件。

下列程式碼範例不會進行編譯而不會發生錯誤，因為尚未定義類別 QuerySink。 如需 QuerySink 類別的定義，請參閱 [**IWbemObjectSink**](iwbemobjectsink.md)。 程式碼範例也需要下列參考和 \# 包含語句。


```C++
#include <iostream>
using namespace std;
#include <wbemidl.h>
```



下列程式碼範例示範如何發出非同步呼叫來發出查詢。


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



如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。

 

 



