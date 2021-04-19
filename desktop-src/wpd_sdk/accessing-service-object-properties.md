---
description: 存取服務物件屬性
ms.assetid: 66d9802b-ad28-47a4-8151-9df7aff07d61
title: 存取服務物件屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 028ffc178f29f21aa60295b137b48c0fa2357a28
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973049"
---
# <a name="accessing-service-object-properties"></a>存取服務物件屬性

應用程式可以針對服務、物件識別碼所識別的多個物件，或相同類型的多個物件，讀取和寫入單一物件的屬性。 「 [正在取得物件屬性](retrieving-content-object-properties.md) 」主題描述如何讀取服務上單一物件的屬性。 [撰寫物件屬性](writing-content-object-properties.md)主題描述如何在服務上撰寫單一物件的屬性。

如需多個物件的屬性抓取說明，請參閱「 [Advanced Tasks](advanced-tasks.md) 」一節。

## <a name="when-to-use-service-property-definitions"></a>使用服務屬性定義的時機

用來抓取和設定服務物件屬性的 WPD API 呼叫，與用來抓取裝置之物件屬性的呼叫相同 (比較「抓取單一物件的屬性」以取得範例) 。 主要差異在於使用不同的 PROPERTYKEYs 集合來查詢物件屬性。 針對 WpdServiceApiSample，會使用裝置服務 PROPERTYKEYs (例如 **PKEY \_ GenericObj \_ 名稱**) ; 針對 WPDAPISAMPLE，會使用 WPD PROPERTYKEYs (例如 **WPD \_ 物件 \_ 名稱**) 。

裝置服務 PROPERTYKEYs 定義于每個服務標頭檔) 所包含的 BridgeDeviceServices (中，並代表裝置服務應用程式和裝置上的固件執行所採用的一組通用 PROPERTYKEYS。 如此一來，就能以最少量的轉譯、以服務為基礎的 PROPERTYKEYs 群組，在整個裝置堆疊中提供一組一致的定義，並可讓您更輕鬆地定義新的服務，而不需要更新 WPD 架構。

使用的 PROPERTYKEYs 集將視您的應用程式需求而定：

-   如果您的應用程式是藉由呼叫 [**IPortableDevice：： Open**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open)來與裝置通訊，請使用 PortableDevice 中所定義的 PROPERTYKEYs。 這類應用程式的其中一個範例是 WpdApiSample。
-   如果您的應用程式是藉由呼叫 [**IPortableDeviceService：： Open**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-open)來與裝置服務通訊，請使用 BridgeDeviceServices 中所定義的 PROPERTYKEYS。 這類應用程式的其中一個範例是 WpdServicesApiSample。
-   如果您撰寫的複雜應用程式需要同時支援裝置服務和裝置的混合 (這表示您的應用程式會同時呼叫 **IPortableDevice：： Open** 和 **IPortableDeviceService：： Open**) ，您必須在使用 IPortableDevice 及其衍生介面時使用 WPD PROPERTYKEYs，並在使用 [PROPERTYKEYs](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice) 及其衍生介面時使用裝置服務 IPortableDeviceService。

大部分的 WPD 應用程式都應該落在第一個或第二個類別中。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IPortableDeviceContent2**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2)
</dt> <dt>

[**IPortableDeviceProperties**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)
</dt> <dt>

[正在抓取物件屬性](retrieving-content-object-properties.md)
</dt> <dt>

[撰寫物件屬性](writing-content-object-properties.md)
</dt> <dt>

[WpdServicesApiSample](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 



