---
description: 裝置類別允許指定該類別之任何裝置的圖示、標籤和 DeviceHandlers 屬性。
ms.assetid: E32C1BA6-B520-4809-A9E9-48813C7EBAA4
title: 如何使用裝置類別指定裝置的圖示、標籤或裝置處理常式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46f81ee6fa469a6bec13abbc1d8a088f5fb334ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991550"
---
# <a name="how-to-specify-an-icon-label-or-device-handler-for-a-device-using-a-device-class"></a>如何使用裝置類別指定裝置的圖示、標籤或裝置處理常式

裝置類別允許指定該類別之任何裝置的圖示、標籤和 DeviceHandlers 屬性。 這類似于使用裝置群組，但是裝置類別和其成員資格是由硬體所決定，而不是建立或指派。 每個類別機碼名稱（也就是隨插即用裝置介面 GUID）都是在 **DeviceClasses** 索引鍵下找到。 在個別類別機碼下，指派圖示、標籤和 DeviceHandlers 的值。

## <a name="instructions"></a>指示

### <a name="step-1"></a>步驟 1:

下列範例會顯示磁片區介面的類別索引鍵和 DeviceHandlers 值。

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  AutoplayHandlers
                     DeviceClasses
                        {53f5630d-b6bf-11d0-94f2-00a0c91efb8b}
                           DeviceHandlers [REG_SZ] = GenericVolumeHandler
```

您也可以在裝置類別機碼底下新增自訂裝置屬性。 自訂裝置屬性接著會套用至該類別中的所有裝置。 裝置和裝置處理常式應該一律有相關聯的圖示和標籤，以符合最小的可用性需求。

> [!Note]  
> 在裝置實例層級定義的屬性優先于在裝置群組層級定義的屬性，而這些屬性會優先于在裝置類別層級定義的屬性。

 

 

 



