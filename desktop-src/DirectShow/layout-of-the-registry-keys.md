---
description: 登錄機碼的版面配置
ms.assetid: c041d094-8165-446f-bf77-0d53b728fe7a
title: 登錄機碼的版面配置
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4473027b2612d16b3c6daee4f8e708d90b993397b133db111aa55c58e9c4ceb0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119502288"
---
# <a name="layout-of-the-registry-keys"></a>登錄機碼的版面配置

DirectShow 篩選準則會在兩個地方註冊：

-   包含篩選的 DLL 會註冊為篩選的 COM 伺服器。 當應用程式呼叫 **CoCreateInstance** 來建立篩選器時，Microsoft Windows COM 程式庫會使用這個登錄專案來尋找 DLL。
-   篩選準則的其他資訊可以在篩選準則類別目錄中註冊。 此資訊可讓 [系統裝置列舉](system-device-enumerator.md) 值和 [篩選器](filter-mapper.md) 對應程式找出篩選。

不需要篩選以註冊額外的篩選資訊。 只要 DLL 註冊為 COM 伺服器，應用程式就可以建立篩選器，並將它新增至篩選圖形。 但是，如果您想要讓篩選器可透過系統裝置列舉值或篩選器對應程式來搜尋，則必須註冊其他資訊。

DLL 的登錄專案具有下列索引鍵：


```
HKEY_CLASSES_ROOT
    CLSID
        Filter CLSID 
            REG_SZ: (Default) = Friendly name

            InprocServer32
                REG_SZ: (Default) = File name of the DLL
                REG_SZ: ThreadingModel = Both
```



篩選資訊的登錄專案具有下列索引鍵：


```
HKEY_CLASSES_ROOT
    CLSID
        Category
            Instance
                Filter CLSID
                    REG_SZ: CLSID = Filter CLSID
                    REG_BINARY: FilterData = Filter information
                    REG_SZ: FriendlyName = Friendly name
```




```
Category
```



這是篩選類別目錄的 GUID。  (參閱 [篩選類別目錄](filter-categories.md)。 ) 篩選資訊會封裝成二進位格式。 [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2)介面會在搜尋登錄中的篩選器時解壓縮此資料。

所有篩選類別目錄 Guid 都會列在登錄的下列機碼底下：


```C++
HKEY_CLASSES_ROOT\CLSID\{DA4E3DA0-D07D-11d0-BD50-00A0C911CE86}\Instance
```



 

 



