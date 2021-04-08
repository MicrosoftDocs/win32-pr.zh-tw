---
title: 當地語系化的系統設定檔
description: 當地語系化的系統設定檔
ms.assetid: 2c218ab4-ecdb-414c-aa42-b71a42e340e5
keywords:
- Windows Media Format SDK，系統設定檔
- Advanced Systems Format (ASF) 、系統設定檔
- ASF (Advanced 系統格式) 、系統設定檔
- Windows Media Format SDK，當地語系化的系統設定檔
- Advanced Systems Format (ASF) ，當地語系化的系統設定檔
- ASF (Advanced Systems Format) ，當地語系化的系統設定檔
- 系統設定檔，當地語系化
- 當地語系化的系統設定檔，清單
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8aaeecdf1d1d62d78df18e0ac1c5bffbf39f9778
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104022998"
---
# <a name="localized-system-profiles"></a>當地語系化的系統設定檔

下表列出 Windows Media Format SDK 隨附的當地語系化系統設定檔，以及與每個檔案相關聯的語言。 這些檔案會安裝到 \[ SDKRoot \] \\ WMSDK \\ WMFSDK9 \\ LocalizedProfiles 資料夾中。 若要使用 **IWMProfileManagerLanguage** 方法來存取特定檔案，您必須將它移至系統根目錄以及預設的系統設定檔。



| 語言              | 檔案名稱    |
|-----------------------|--------------|
| 阿拉伯文                | WMPrfAra.prx |
| 中文-簡體  | WMPrfCHS.prx |
| 中文-繁體 | WMPrfCHT.prx |
| 捷克文                 | WMPrfCsy.prx |
| 丹麥文                | WMPrfDan.prx |
| 荷蘭文                 | WMPrfNld.prx |
| 芬蘭文               | WMPrfFin.prx |
| 法文                | WMPrfFra.prx |
| 德文                | WMPrfDeu.prx |
| 希臘文                 | WMPrfEll.prx |
| Hebrew                | WMPrfHeb.prx |
| 匈牙利文             | WMPrfHun.prx |
| 義大利文               | WMPrfIta.prx |
| 日文              | WMPrfJpn.prx |
| 韓文                | WMPrfKor.prx |
| 挪威文             | WMPrfNor.prx |
| 波蘭文                | WMPrfPlk.prx |
| 葡萄牙文 – 巴西   | WMPrfPtb.prx |
| 葡萄牙文 (葡萄牙) | WMPrfPtg.prx |
| 俄文               | WMPrfRus.prx |
| 斯洛伐克文                | WMPrfSky.prx |
| 斯洛維尼亞文             | WMPrfSlv.prx |
| 西班牙文               | WMPrfEsp.prx |
| 瑞典文               | WMPrfSve.prx |
| 土耳其文               | WMPrfTrk.prx |



 

您可以藉由呼叫 [**IWMProfileManagerLanguage：： SetUserLanguageID**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanagerlanguage-setuserlanguageid) 方法，設定配置檔案管理員物件的語言。 針對大部分的語言，只會檢查 LANGID 中的主要語言識別項。 例外狀況適用于中文和葡萄牙文語言，其中也會使用次要語言識別項。 下表說明如何建立要在 **SetUserLanguageID** 方法中指定的 LANGID。



| 主要-次要語言 | MAKELANGID 宏                                             |
|----------------------------|--------------------------------------------------------------|
| 中文 (簡體)       | MAKELANGID ( LANG \_ 中文，SUBLANG \_ 簡體中文 \_)      |
| 中文 (繁體)      | MAKELANGID ( LANG \_ 中文，SUBLANG \_ 中文 \_ 新加坡)       |
| 葡萄牙文 (巴西)        | MAKELANGID (LANG \_ 葡萄牙文，SUBLANG \_ 葡萄牙文 \_ 巴西)  |
| 葡萄牙文 (葡萄牙)      | MAKELANGID (LANG \_ 葡萄牙文，SUBLANG \_ 葡萄牙文)             |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**程式設計參考**](programming-reference.md)
</dt> <dt>

[**系統設定檔**](system-profiles.md)
</dt> </dl>

 

 




