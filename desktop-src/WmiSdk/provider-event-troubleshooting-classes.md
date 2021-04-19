---
description: 下表列出 WMI 提供者事件疑難排解的類別。 每個類別都與其結合的 WMI 提供者事件相關聯。
ms.assetid: 5acfc8f4-9b3b-4ff4-a8ed-7378334a8ddb
ms.tgt_platform: multiple
title: 提供者事件疑難排解類別
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62ed8c02cf70078ae3b6f42d1c45e2d40efeabe2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975309"
---
# <a name="provider-event-troubleshooting-classes"></a>提供者事件疑難排解類別

下表列出 WMI 提供者事件疑難排解的類別。 每個類別都與其結合的 WMI 提供者事件相關聯。



| 類別                                                                                                                            | 描述                                                                                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MSFT \_ 的 wmiprovider \_ AccessCheck \_ 文章**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-accesscheck-post)                                      | 緊接在完成提供者的 [**IWbemEventProviderSecurity：： AccessCheck**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventprovidersecurity-accesscheck)完成後產生的事件類別實例。   |
| [**MSFT \_ 的 wmiprovider \_ AccessCheck \_ 預先**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-accesscheck-pre)                                        | 在呼叫提供者的 [**IWbemEventProviderSecurity：： AccessCheck**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventprovidersecurity-accesscheck)執行之前立即產生的事件類別實例。          |
| [**MSFT \_ 的 wmiprovider \_ CancelQuery \_ 文章**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-cancelquery-post)                                      | 緊接在完成提供者的 [**IWbemEventProviderQuerySink：： CancelQuery**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventproviderquerysink-cancelquery)完成後產生的事件類別實例。 |
| [**MSFT \_ 的 wmiprovider \_ CancelQuery \_ 預先**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-cancelquery-pre)                                        | 在呼叫提供者的 [**IWbemEventProviderQuerySink：： CancelQuery**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventproviderquerysink-cancelquery)執行之前立即產生的事件類別實例。        |
| [**MSFT \_ 的 wmiprovider \_ ComServerLoadOperationEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-comserverloadoperationevent)                 | 針對 COM 伺服器實例啟用所產生的事件類別實例。                                                                                                                               |
| [**MSFT \_ 的 wmiprovider \_ ComServerLoadOperationFailureEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-comserverloadoperationfailureevent)   | 針對 COM 伺服器實例啟用失敗所產生的事件類別實例。                                                                                                                       |
| [**MSFT \_ 的 wmiprovider \_ CreateClassEnumAsyncEvent \_ 文章**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-createclassenumasyncevent-post)          | 緊接在完成提供者的 [**IWbemServices：： CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync)完成後產生的事件類別實例。           |
| [**MSFT \_ 的 wmiprovider \_ CreateClassEnumAsyncEvent \_ 預先**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-createclassenumasyncevent-pre)            | 在呼叫提供者的 [**IWbemServices：： CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync)執行之前立即產生的事件類別實例。                  |
| [**MSFT \_ 的 wmiprovider \_ CreateInstanceEnumAsyncEvent \_ 文章**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-createinstanceenumasyncevent-post)    | 緊接在完成提供者的 [**IWbemServices：： CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync)完成後產生的事件類別實例。     |
| [**MSFT \_ 的 wmiprovider \_ CreateInstanceEnumAsyncEvent \_ 預先**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-createinstanceenumasyncevent-pre)      | 在呼叫提供者的 [**IWbemServices：： CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync)執行之前立即產生的事件類別實例。            |
| [**MSFT \_ 的 wmiprovider \_ DeleteClassAsyncEvent \_ 文章**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-deleteclassasyncevent-post)                  | 緊接在完成提供者的 [**IWbemServices：:D eleteclassasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync)完成後產生的事件類別實例。                   |
| [**MSFT \_ 的 wmiprovider \_ DeleteClassAsyncEvent \_ 預先**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-deleteclassasyncevent-pre)                    | 在呼叫 provider 的 [**IWbemServices：:D eleteclassasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync)之前，立即產生的事件類別實例。                          |
| [**MSFT \_ 的 wmiprovider \_ DeleteInstanceAsyncEvent \_ 文章**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-deleteinstanceasyncevent-post)            | 緊接在完成提供者的 [**IWbemServices：:D eleteinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync)完成後產生的事件類別實例。             |
| [**MSFT \_ 的 wmiprovider \_ DeleteInstanceAsyncEvent \_ 預先**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-deleteinstanceasyncevent-pre)              | 在呼叫 provider 的 [**IWbemServices：:D eleteinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync)之前，立即產生的事件類別實例。                    |
| [**MSFT \_ 的 wmiprovider \_ ExecMethodAsyncEvent \_ 文章**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-execmethodasyncevent-post)                    | 緊接在完成提供者的 [**IWbemServices：： ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync)完成後產生的事件類別實例。                     |
| [**MSFT \_ 的 wmiprovider \_ ExecMethodAsyncEvent \_ 預先**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-execmethodasyncevent-pre)                      | 在呼叫提供者的 [**IWbemServices：： ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync)執行之前立即產生的事件類別實例。                            |
| [**MSFT \_ 的 wmiprovider \_ ExecQueryAsyncEvent \_ 文章**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-execqueryasyncevent-post)                      | 緊接在完成提供者的 [**IWbemServices：： ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync)完成後產生的事件類別實例。                       |
| [**MSFT \_ 的 wmiprovider \_ ExecQueryAsyncEvent \_ 預先**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-execqueryasyncevent-pre)                        | 在呼叫提供者的 [**IWbemServices：： ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync)執行之前立即產生的事件類別實例。                              |
| [**MSFT \_ 的 wmiprovider \_ GetObjectAsyncEvent \_ 文章**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-getobjectasyncevent-post)                      | 緊接在完成提供者的 [**IWbemServices：： GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)完成後產生的事件類別實例。                       |
| [**MSFT \_ 的 wmiprovider \_ GetObjectAsyncEvent \_ 預先**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-getobjectasyncevent-pre)                        | 在呼叫提供者的 [**IWbemServices：： GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)執行之前立即產生的事件類別實例。                              |
| [**MSFT \_ 的 wmiprovider \_ InitializationOperationEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-initializationoperationevent)               | 為成功初始化提供者伺服器實例所產生的事件類別實例。                                                                                                    |
| [**MSFT \_ 的 wmiprovider \_ InitializationOperationFailureEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-initializationoperationfailureevent) | 為提供者伺服器實例的初始化失敗所產生的事件類別實例。                                                                                                        |
| [**MSFT \_ 的 wmiprovider \_ LoadOperationEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-loadoperationevent)                                   | 事件類別實例產生或成功啟用和初始化提供者快取專案。                                                                                          |
| [**MSFT \_ 的 wmiprovider \_ LoadOperationFailureEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-loadoperationfailureevent)                     | 針對啟用和初始化提供者快取專案所產生的事件類別實例。                                                                                             |
| [**MSFT \_ 的 wmiprovider \_ NewQuery \_ 文章**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-newquery-post)                                            | 緊接在完成提供者的 [**IWbemEventProviderQuerySink：： NewQuery**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventproviderquerysink-newquery)完成後產生的事件類別實例。       |
| [**MSFT \_ 的 wmiprovider \_ NewQuery \_ 預先**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-newquery-pre)                                              | 在呼叫提供者的 [**IWbemEventProviderQuerySink：： NewQuery**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventproviderquerysink-newquery)執行之前立即產生的事件類別實例。              |
| [**MSFT \_ 的 wmiprovider \_ OperationEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-operationevent)                                           | WMI 提供者疑難排解事件類別的基類。                                                                                                                                       |
| [**MSFT \_ 的 wmiprovider \_ OperationEvent \_ 文章**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-operationevent-post)                                | 完成提供者執行之後，針對事件進行疑難排解的基類。                                                                                                           |
| [**MSFT \_ 的 wmiprovider \_ OperationEvent \_ 預先**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-operationevent-pre)                                  | 在呼叫提供者執行之前，針對事件進行疑難排解的基類。                                                                                                                  |
| [**MSFT \_ 的 wmiprovider \_ ProvideEvents \_ 文章**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-provideevents-post)                                  | 緊接在完成提供者的 [**IWbemEventProvider：:P rovideevents**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventprovider-provideevents)完成後產生的事件類別實例。               |
| [**MSFT \_ 的 wmiprovider \_ ProvideEvents \_ 預先**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-provideevents-pre)                                    | 在呼叫提供者的 [**IWbemEventProvider：:P rovideevents**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventprovider-provideevents)之前立即產生的事件類別實例。                      |
| [**MSFT \_ 的 wmiprovider \_ PutClassAsyncEvent \_ 文章**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-putclassasyncevent-post)                        | 緊接在完成提供者的 [**IWbemServices：:P utclassasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync)完成後產生的事件類別實例。                         |
| [**MSFT \_ 的 wmiprovider \_ PutClassAsyncEvent \_ 預先**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-putclassasyncevent-pre)                          | 在呼叫 provider 的 [**IWbemServices：:P utclassasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync)之前，立即產生的事件類別實例。                                |
| [**MSFT \_ 的 wmiprovider \_ PutInstanceAsyncEvent \_ 文章**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-putinstanceasyncevent-post)                  | 緊接在完成提供者的 [**IWbemServices：:P utinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync)完成後產生的事件類別實例。                   |
| [**MSFT \_ 的 wmiprovider \_ PutInstanceAsyncEvent \_ 預先**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-putinstanceasyncevent-pre)                    | 在呼叫 provider 的 [**IWbemServices：:P utinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync)之前，立即產生的事件類別實例。                          |
| [**MSFT \_ 的 wmiprovider \_ UnloadOperationEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-unloadoperationevent)                               | 為了移除提供者快取專案所產生的事件類別實例。                                                                                                                          |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[WMI 疑難排解](wmi-troubleshooting.md) \(英文\)
</dt> <dt>

WMI 疑難排解
</dt> <dt>

[接收 WMI 事件](receiving-a-wmi-event.md)
</dt> </dl>

 

 
