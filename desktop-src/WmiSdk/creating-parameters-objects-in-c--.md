---
description: 如果執行的方法具有任何輸入引數，則 IWbemServices：： ExecMethod 或 ExecMethodAsync 方法需要 \_ \_ 參數系統類別做為 pInParams 中的容器。
ms.assetid: 17b72ceb-e730-4176-aa4d-189d0b6acc8b
ms.tgt_platform: multiple
title: 在 c + + 中建立參數物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c200958f4ad00ced5455462e7a2909ac6a58cfd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192203"
---
# <a name="creating-parameters-objects-in-c"></a>在 c + + 中建立參數物件

如果執行的方法具有任何輸入引數，則 [**IWbemServices：： ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod)或 [**ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync)方法需要 [**\_ \_ 參數**](--parameters.md)系統類別做為 *pInParams* 中的容器。

下列程式描述如何建立 [**\_ \_ 參數**](--parameters.md)系統類別的實例來保存參數資訊。

**若要建立參數的實例 \_ \_**

1.  判斷包含方法定義之類別的類別路徑。
2.  使用從 [**IWbemProviderInit：： Initialize**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize)傳入的類別路徑和 [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices)指標，呼叫 [**IWbemClassObject：： GetMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod)以取得輸入和輸出參數類別。

    [**GetMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod)方法會傳回用來存取每個類別的 [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject)指標。

3.  使用輸出類別的 [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) 指標，呼叫 [**IWbemClassObject：： SpawnInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawninstance) 來建立類別的實例。
4.  藉由設定對應至輸出值的屬性來填入類別實例，如果有方法的傳回值，則為 [ReturnValue](creating-a-method.md) 屬性。
5.  透過 [**IWbemObjectSink：：指示**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate)方法，將 [**\_ \_ 參數**](--parameters.md)實例傳回給呼叫端。

當方法提供者判斷輸入參數正確之後， *strMethodName* 所指向的方法可能仍會通過或失敗。 某些方法提供者會產生第二個執行緒來執行方法，讓方法的實際成功或失敗最後會透過 [**IWbemObjectSink：： SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus)回報給呼叫者。 請注意， **IWbemObjectSink：： SetStatus** 不會收到提供者方法的傳回碼。 但是，它會接收實際呼叫傳回機制的傳回碼，而且只適用于驗證呼叫是否發生，或是基於機械原因而失敗。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[呼叫方法](calling-a-method.md)
</dt> <dt>

[**IWbemCallResult::GetResultObject**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemcallresult-getresultobject)
</dt> <dt>

[**IWbemServices：： ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync)
</dt> <dt>

[**IWbemServices：： ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod)
</dt> </dl>

 

 



