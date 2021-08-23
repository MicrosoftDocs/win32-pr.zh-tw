---
description: wdm (Windows Driver Model) 提供者會授與符合 WDM 模型的硬體驅動程式之類別、實例、方法和事件的存取權。
ms.assetid: 2f9749ff-b318-4228-80fd-e3846dde21d2
title: WDM 提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54ba187680ec371f331aa6394c5a2408c23080259e6b275e74cee496dd5125cb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119794618"
---
# <a name="wdm-provider"></a>WDM 提供者

wdm (Windows Driver Model) 提供者會授與符合 WDM 模型的硬體驅動程式之類別、實例、方法和事件的存取權。 硬體驅動程式的類別位於「根 \\ wmi 命名空間」中。

WDM 類別主要是在 Wmi 中定義。

WDM 是一種作業系統介面，可用來提供資訊和事件通知。 WDM 提供者是一種類別、實例、事件和方法提供者，可讓管理應用程式從啟用 WMI 的裝置驅動程式存取資料和事件。 WDM 提供者所建立用來代表設備磁碟機資料的類別，只位於「根 \\ WMI」命名空間中。 在 WDM 提供者將處理已安裝的 WDM 驅動程式之前，這個命名空間必須已經存在。

WDM 提供者會在 WmiProv 檔案中記錄 WDM 作業的相關資訊。 如需詳細資訊，請參閱 [WMI 記錄](/windows/desktop/WmiSdk/wmi-log-files)檔。

針對類別、實例、方法和事件提供者，WDM 提供者會實作為標準 [**IWbemProviderInit**](/windows/desktop/api/wbemprov/nn-wbemprov-iwbemproviderinit) 介面，以及下列 [**IWbemServices**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices) 方法：

-   [**CreateClassEnumAsync**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-createclassenumasync)
-   [**CreateInstanceEnumAsync**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-createinstanceenumasync)
-   [**GetObjectAsync**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-getobjectasync)
-   [**ExecMethodAsync**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-execmethodasync)
-   [**ExecNotificationQueryAsync**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-execnotificationqueryasync)
-   [**ExecQueryAsync**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-execqueryasync)
-   [**PutInstanceAsync**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-putinstanceasync)

WDM 提供者支援 [**>register-wmievent**](/windows/desktop/WmiCoreProv/wmievent) 外建事件，此事件會通知 WMI 有關來自以 WDM 為基礎之驅動程式的事件。 您可以註冊事件取用者來 **>register-wmievent** 事件，就像任何其他事件一樣。 如需詳細資訊，請參閱 [接收 WMI 事件](/windows/desktop/WmiSdk/receiving-a-wmi-event)。 啟動驅動程式時，不會引發任何類別建立事件。

WDM 提供者支援下列類別：

-   [**WMIBinaryMofResource**](wmibinarymofresource.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[WMI 提供者](/windows/desktop/WmiSdk/wmi-providers)
</dt> <dt>

[從設備磁碟機存取資料](/windows/desktop/WmiSdk/accessing-data-from-device-drivers)
</dt> </dl>

 

 
