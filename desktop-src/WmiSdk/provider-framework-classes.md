---
description: 瞭解屬於 WMI 提供者架構的 WMI c + + 類別，現在會被視為最終狀態。
ms.assetid: 062a7724-0589-4e9d-af7a-39fd9c08e40b
ms.tgt_platform: multiple
title: 提供者架構類別
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ba5f8ec85eca2ea2413e176b104865c84ddc5de39aa9fd137b015d07c3e0592
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119130990"
---
# <a name="provider-framework-classes"></a>提供者架構類別

\[屬於 WMI 提供者架構一部分的 WMI c + + 類別現在會被視為最終狀態，而且不會有任何進一步的開發、增強功能或更新可用於影響這些程式庫的非安全性相關問題。 [MI api](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure)應該用於所有新的開發。\]

提供者架構會實作為下列類別。



| Framework 類別                                | 描述                                                                                                                                                                                                         |
|------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CFrameworkQuery**](/windows/desktop/api/FrQuery/nl-frquery-cframeworkquery)     | 包含查詢處理的方法。                                                                                                                                                                              |
| [**CInstance**](/windows/desktop/api/Instance/nl-instance-cinstance)                 | 包含用來設定和取出屬性的方法，而且是 [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) 介面的封裝。 實施者應該不需要直接存取 **IWbemClassObject** 方法。 |
| [**CThreadBase**](/windows/desktop/api/ThrdBase/nl-thrdbase-cthreadbase)             | 提供 WMI 提供者架構內部執行緒安全機制的基類。                                                                                                                    |
| [**CWbemGlueFactory**](/windows/desktop/api/WbemGlue/nl-wbemglue-cwbemgluefactory)   | WMI 提供者架構的一部分。 提供者架構會在內部實作為此介面的方法，為提供者建立新的類別實例。                                                     |
| [**CWbemProviderGlue**](/windows/desktop/api/WbemGlue/nl-wbemglue-cwbemproviderglue) | 會實 [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) 和方法，以控制架構提供者的載入和卸載。                                                                             |
| [**提供者**](/windows/desktop/api/Provider/nl-provider-provider)                   | 包含 helper 函式，並提供 [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices)方法的預設實作為。                                                                                            |



 

請注意，許多 framework 方法都使用 [**CHString**](chstring.md) 參數。 **CHString** 支援許多與 Microsoft Foundation 類別 (mfc) 相同的方法和屬性，但是不會有 mfc 的額外負荷。 如需 **CHString** 的詳細資訊，請參閱 **CHString 類別參考**。

 

 
