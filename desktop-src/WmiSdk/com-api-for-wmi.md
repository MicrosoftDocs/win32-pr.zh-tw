---
description: 您可以使用 WMI 元件物件模型 (COM) API 來寫入管理用戶端應用程式，或建立新的 WMI 提供者。
ms.assetid: 5fa8f1b5-fd19-4d45-9b53-bc7089eecdb1
ms.tgt_platform: multiple
title: 適用于 WMI 的 COM API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfb585badeeeaae947906bbfc783baf355863e05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984993"
---
# <a name="com-api-for-wmi"></a>適用于 WMI 的 COM API

您可以使用 WMI 元件物件模型 (COM) API 來寫入管理用戶端應用程式，或建立新的 WMI [*提供者*](gloss-p.md)。 COM API 參考提供 advanced system 系統管理員的資訊，以及撰寫用戶端和提供者應用程式的開發人員。

如需撰寫 WMI enterprise management 應用程式的詳細資訊，請參閱 [使用 c + + 建立 Wmi 應用程式](creating-a-wmi-application-using-c-.md)。 如需有關如何撰寫 WMI 提供者的詳細資訊，請參閱 [將資料提供給 wmi](providing-data-to-wmi.md)。

> [!Note]  
> WMI 僅支援使用 Microsoft Visual C++ 6.0 版和更新版本的開發系統進行 c + + 開發。 不過，您也可以使用其他編譯器，例如來自 Borland 和 Watcom 的編譯器。

 

每個不同的 WMI 物件都會繼承自介面，最後繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) 介面。 COM 會指定物件實施者（或介面）如何處理工作，例如記憶體管理、參數管理和多執行緒處理。 藉由符合 COM，適用于 WMI 的 COM API 可確保它支援每個 WMI 物件介面所提供的功能。

WMI 可透過下列 WMI 特定的 COM 介面進行存取。



| 介面                                                                    | 描述                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject)                         | 適用于 [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject)類型之物件的列舉值。 它類似于標準 COM 列舉值，例如 [**IEnumVariant**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant)。                                                                                                      |
| [**IMofCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler)                                         | 由 Mofd.dll 所執行，此介面會提供 MOF 編譯器所使用的 COM 介面，以及任何其他編譯 MOF 檔案的應用程式。                                                                                                                                                       |
| [**IUnsecuredApartment**](/windows/desktop/api/Wbemcli/nn-wbemcli-iunsecuredapartment)                           | 用來簡化從用戶端進程進行非同步呼叫的程式。                                                                                                                                                                                                                           |
| [**IWbemBackupRestore**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbembackuprestore)                             | 備份和還原 WMI 存放庫的內容。                                                                                                                                                                                                                                                  |
| [**IWbemCallResult**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemcallresult)                                   | 用於 [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices)介面的 [半同步](making-a-semisynchronous-call-with-c--.md)呼叫。 進行這類呼叫時，被呼叫的 **IWbemServices** 方法會立即傳回，以及 [**IWbemCallResult**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemcallresult) 物件。                    |
| [**IWbemCausalityAnalysis**](iwbemcausalityaccess.md)                       | 追蹤從父要求產生的子要求。                                                                                                                                                                                                                                            |
| [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject)                                 | 包含和操作類別定義和類別物件實例。 開發人員不需要執行這個介面;WMI 提供其實作為。                                                                                                                                                 |
| [**IWbemConfigureRefresher**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemconfigurerefresher)                   | 由用戶端程式代碼用來將列舉值、物件和嵌套的重新整理器新增或移除到複習中。                                                                                                                                                                                                         |
| [**IWbemCoNtext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext)                                         | 選擇性地在將 [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) 呼叫提交給 Windows 管理時，用來將其他內容資訊傳達給提供者。                                                                                                                                             |
| [**IWbemDecoupledBasicEventProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemdecoupledbasiceventprovider) | 向 WMI 註冊低耦合提供者。                                                                                                                                                                                                                                                                    |
| [**IWbemDecoupledRegistrar**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemdecoupledregistrar)                   | 讓低耦合提供者與 WMI 產生關聯。 這個介面可讓進程裝載的提供者定義介面的互通性存留期，並與其他提供者並存。                                                                                                                        |
| [**IWbemEventConsumerProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventconsumerprovider)             | 提供事件取用者提供者的主要介面。 透過這個介面和 [**FindConsumer**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventconsumerprovider-findconsumer) 方法，事件取用者提供者可以指出哪些事件取用者應該接收指定事件。                                          |
| [**IWbemEventProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventprovider)                             | 用來起始與事件提供者的通訊。                                                                                                                                                                                                                                                     |
| [**IWbemEventProviderQuerySink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventproviderquerysink)           | （選擇性）由想要知道目前作用中的事件查詢篩選準則類型的事件提供者所執行，以優化效能。                                                                                                                                                                 |
| [**IWbemEventProviderSecurity**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventprovidersecurity)             | （選擇性）由想要限制取用者存取其事件的事件提供者來執行。                                                                                                                                                                                                             |
| [**IWbemEventSink**](iwbemeventsink.md)                                     | 使用一組受限制的查詢來起始與事件提供者的通訊。 這個介面會擴充 [**IWbemObjectSink**](iwbemobjectsink.md)，提供處理安全性和效能的新方法。                                                                                          |
| [**IWbemHiPerfProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemhiperfprovider)                           | 可讓提供者提供可重新整理的物件和枚舉器。                                                                                                                                                                                                                                           |
| [**IWbemHiPerfEnum**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemhiperfenum)                                   | 用於重新整理程式作業，以提供實例物件列舉的快速存取。                                                                                                                                                                                                                  |
| [**IWbemLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator)                                         | 取得特定主機電腦上 WMI 的 [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) 介面初始命名空間指標。                                                                                                                                                                         |
| [**IWbemObjectAccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess)                               | 提供物件之方法和屬性的存取權。 [**IWbemObjectAccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess)物件是重新整理程式所更新之實例的容器 [*。*](gloss-r.md)                                                                                           |
| [**IWbemObjectSink**](iwbemobjectsink.md)                                   | 用來接收 [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) 的結果和特定類型的事件通知。                                                                                                                                                                                       |
| [**IWbemObjectTextSrc**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjecttextsrc)                             | 用來將 [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) 實例與不同的文字格式轉譯。                                                                                                                                                                                               |
| [**IWbemPropertyProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbempropertyprovider)                       | 支援在 WMI 類別的實例中，抓取和更新個別屬性。                                                                                                                                                                                                                      |
| [**IWbemProviderIdentity**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemprovideridentity)                       | 如果提供者使用一個以上的 **名稱** 來註冊本身， (多個 [**\_ \_ Win32Provider**](--win32provider.md)) 的實例（具有相同的 [CLSID](../com/clsid.md)值），則由事件提供者所執行。 類別提供一種機制，用來區別應該使用的命名提供者。 |
| [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit)                               | 用來初始化提供者。                                                                                                                                                                                                                                                                              |
| [**IWbemProviderInitSink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinitsink)                       | 由 WMI 執行，並由提供者呼叫以報告初始化狀態。                                                                                                                                                                                                                                |
| [**IWbemQualifierSet**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemqualifierset)                               | 作為單一屬性或整個物件的整組命名限定詞的容器，)  (類別或實例。                                                                                                                                                                                   |
| [**IWbemQuery**](/windows/desktop/api/Wmiutils/nn-wmiutils-iwbemquery)                                             | 提供可剖析 [*WMI 查詢語言*](gloss-w.md) (WQL) 查詢的進入點。                                                                                                                                                                        |
| [**IWbemRefresher**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemrefresher)                                     | 提供一個進入點，可讓您重新整理可重新整理的物件（例如枚舉器或重新整理程式物件）。                                                                                                                                                                                      |
| [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices)                                       | 供用戶端和提供者用來存取 WMI 服務。 介面只能由 WMI 執行，而且是主要 WMI 介面。                                                                                                                                                                           |
| [**IWbemStatusCodeText**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemstatuscodetext)                           | 解壓縮錯誤碼的文字字串描述，或發生錯誤之子系統的名稱。                                                                                                                                                                                                    |
| [**IWbemUnboundObjectSink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemunboundobjectsink)                     | 由所有邏輯事件取用者所執行。 它是接受事件物件傳遞的簡單接收介面。                                                                                                                                                                                          |



 

> [!Note]  
> 許多 WMI COM 函數都會傳回以命名常數記載的數值錯誤碼。 這些常數定義于 PSDK WMI Include 資料夾的 Wbemcli 中。 \\ 如需詳細資訊，請參閱 [WMI 傳回碼](wmi-return-codes.md)。

 

如需有關 COM 程式設計的下列主題的詳細資訊，請參閱 [元件開發]( /previous-versions//ee663263(v=vs.85))：

-   介面和物件設計。
-   執行 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)。
-   記憶體管理
-   正在處理參考計數。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[WMI 參考](wmi-reference.md)
</dt> </dl>

 

 
