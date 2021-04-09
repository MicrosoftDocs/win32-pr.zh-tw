---
title: 設定檔物件
description: 設定檔物件
ms.assetid: ec42889e-580e-4a65-9fe6-4a5f15c97eb0
keywords:
- Windows Media 格式 SDK，設定檔物件
- Advanced Systems Format (ASF) 、profile 物件
- ASF (Advanced 系統格式) ，設定檔物件
- 物件，設定檔物件
- 設定檔，物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d6763d098819bde7d5db404aeffef3cd333d9b1
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/25/2020
ms.locfileid: "103841967"
---
# <a name="profile-object"></a>設定檔物件

設定檔物件會管理設定檔的設定。 您可以為現有的設定檔資料建立設定檔物件，也可以建立空的，以便接收新資料。 在載入檔案以進行讀取時，讀取器物件也會建立設定檔物件 (和同步讀取器物件) 。 在此情況下，物件會填入儲存在檔案標頭中的設定檔資訊。

若要儲存設定檔物件的內容，您必須呼叫 [**IWMProfileManager：： SaveProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-saveprofile)。

設定檔包含多個物件，可控制設定檔 (的各個層面，例如資料流程) 。 所有這些物件都是設定檔物件的從屬物件。 您不會像使用此 SDK 的主要物件一樣，建立具有建立功能的這些物件。 但是，設定檔物件的介面會包含建立從屬物件的方法。

若要建立設定檔物件，請呼叫下列其中一種方法。



| 方法                                                                                | 描述                                                                                                                                                     |
|---------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMProfileManager::CreateEmptyProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-createemptyprofile) | 建立沒有任何設定檔資料的設定檔物件。                                                                                                              |
| [**IWMProfileManager::LoadProfileByData**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-loadprofilebydata)   | 建立設定檔物件，其填入儲存為字串之設定檔中的資料。 這是使用自訂設定檔中的資料建立設定檔物件的唯一方法。 |
| [**IWMProfileManager::LoadProfileByID**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-loadprofilebyid)       | 建立以系統設定檔中的資料填入的設定檔物件。 使用 GUID 來識別所需的系統設定檔。                                       |
| [**IWMProfileManager::LoadSystemProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-loadsystemprofile)   | 建立以系統設定檔中的資料填入的設定檔物件。 使用設定檔索引來識別所需的系統設定檔。                              |



 

上表中的所有方法都會設定 **IWMProfile** 介面的指標。 您可以藉由呼叫 **QueryInterface** 方法來取得設定檔物件的其他介面。

每個設定檔物件都支援下列介面。



| 介面                                  | 描述                                                                                                                                       |
|--------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMLanguageList**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlanguagelist) | 管理 ASF 檔案所支援的語言清單。                                                                                             |
| [**IWMPacketSize**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize)     | 控制檔案中封包的大小上限。                                                                                                   |
| [**IWMPacketSize2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize2)   | 控制檔案中封包的大小下限。 繼承 **IWMPacketSize** 的所有方法。                                                 |
| [**IWMProfile**](iwmprofile.md)           | 控制設定檔中包含的基本設定和物件。                                                                                    |
| [**IWMProfile2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile2)         | 抓取與設定檔相關聯 (GUID) 的全域唯一識別碼。 繼承 **IWMProfile** 的所有方法。                       |
| [**IWMProfile3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3)         | 控制設定檔中的頻寬共用和串流優先順序資訊。 繼承 **IWMProfile** 和 **IWMProfile2** 的所有方法。 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**物件**](objects.md)
</dt> <dt>

[**設定檔管理員物件**](profile-manager-object.md)
</dt> <dt>

[**配置 檔**](profiles.md)
</dt> </dl>

 

 




