---
description: IWiaPropertyStorage 介面會提供方法，以讀取和寫入 Windows 映像取得 (WIA) 專案的屬性。 專案屬性包括裝置命令、專案格式資訊和裝置資訊。
ms.assetid: 268d2298-bc9c-479b-b078-a8180cd38bc3
title: 讀取及設定 WIA 屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51df3e8fdb4b29abb6f64743ab8f7f2dd3776358
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113285"
---
# <a name="reading-and-setting-wia-properties"></a>讀取及設定 WIA 屬性

[**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage)介面會提供方法，以讀取和寫入 Windows 映像取得 (WIA) 專案的屬性。 專案屬性包括裝置命令、專案格式資訊和裝置資訊。

應用程式可以藉由呼叫 [**IWiaItem：： EnumDeviceCapabilities**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumdevicecapabilities)或 [**IWiaItem：： EnumRegisterEventInfo**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumregistereventinfo) ，或藉由查詢專案的 [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem)介面，來取得專案之 [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage)介面的指標。  (在 WIA 2.0 中，藉由呼叫 [**IWiaItem2：： EnumDeviceCapabilities**](-wia-iwiaitem2-enumdevicecapabilities.md) 或 [**IWiaItem2：： EnumRegisterEventInfo**](-wia-iwiaitem2-enumregistereventinfo.md) 或查詢專案的 [**IWiaItem2**](-wia-iwiaitem2.md) 介面來執行此作業。 ) 

[**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) 繼承自 [IPropertyStorage](/windows/win32/api/propidlbase/nn-propidlbase-ipropertystorage) ，且繼承的方法會依照 Windows 軟體開發套件 (SDK) 中結構化儲存體的參考一節所述的方式執行。

> [!Note]
>
> WIA 應用程式應該一律讀取影像資料標頭，以取得正確的影像資訊。 WIA 驅動程式可以在資料傳輸期間改變 WIA 屬性和影像資料標頭。
>
> 如果未提供指定格式的影像資料標頭，則 WIA 應用程式應該使用 WIA 屬性作為資料傳輸的相關資訊來源。 當掃描或抓取完成之後，WIA 應用程式應該重新讀取所需的 WIA 屬性，以取得更新的設定。

 

下列各節說明各種 WIA 屬性：

-   [WIA 屬性驗證](-wia-wia-property-validation.md)
-   [裝置資訊屬性](-wia-device-information-properties-wia-dip-xxxx.md)
-   [裝置內容](-wia-device-properties.md)
-   [項目屬性](-wia-item-properties.md)
-   [其他 WIA 屬性](-wia-additional-wia-properties.md)
-   [定義自訂屬性](-wia-defining-custom-properties.md)
-   [使用自訂屬性](-wia-using-custom-properties.md)
-   [掃描設定檔架構](-wia-scan-profile-schema.md)

 

 
