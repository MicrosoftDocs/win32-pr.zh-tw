---
title: 設定檔管理員物件
description: 設定檔管理員物件
ms.assetid: 8d174243-334e-418e-a1c8-77486b940de7
keywords:
- Windows Media 格式 SDK，配置檔案管理員物件
- Advanced Systems Format (ASF) 、profile manager 物件
- ASF (Advanced Systems Format) ，profile manager 物件
- 物件，配置檔案管理員物件
- 設定檔，物件
- 設定檔，配置檔案管理員物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ce3d77598f52e43a840c1b6b3ef58baa47f77bd
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/25/2020
ms.locfileid: "106969095"
---
# <a name="profile-manager-object"></a>設定檔管理員物件

設定檔是一組用來建立 ASF 檔案的媒體參數。 配置檔案管理員物件會建立設定檔物件來進行編輯。 您可以建立不含任何資料的設定檔物件，或是從現有的設定檔資料建立。 配置檔案管理員物件也提供列舉支援的編解碼器，以及查詢這些編解碼器以取得相關資訊的方法。

配置檔案管理員物件是由 [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) 函式所建立，它會將指標設定為 [**IWMProfileManager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) 介面。 您可以藉由呼叫 **QueryInterface** 方法來取得配置檔案管理員物件的其他介面。

配置檔案管理員物件支援下列介面。



| 介面                                                      | 描述                                                                                                                                  |
|----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMCodecInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo)                           | 抓取支援的編解碼器及其格式的相關資訊。                                                                              |
| [**IWMCodecInfo2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo2)                         | 抓取支援的編解碼器名稱和其格式的描述。 繼承 **IWMCodecInfo** 的所有方法。          |
| [**IWMCodecInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo3)                         | 抓取編解碼器屬性和查詢編解碼器以取得支援的功能。 繼承 **IWMCodecInfo** 和 **IWMCodecInfo2** 的所有方法。 |
| [**IWMProfileManager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager)                 | 建立新的設定檔、載入現有的設定檔，並儲存自訂設定檔。                                                                    |
| [**IWMProfileManager2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager2)               | 控制配置檔案管理員列舉的系統設定檔版本。 繼承 **IWMProfileManager** 的所有方法。             |
| [**IWMProfileManagerLanguage**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanagerlanguage) | 控制配置檔案管理員所剖析之系統設定檔的語言。                                                                  |



 

## <a name="remarks"></a>備註

當配置檔案管理員物件建立時，它會剖析所有系統設定檔，這可能需要幾秒鐘的時間。 每次需要使用時建立和發行配置檔案管理員，將會對效能造成不良的影響。 您應該在應用程式中建立配置檔案管理員一次，而且只有在不再需要使用它時，才將它釋放。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**物件**](objects.md)
</dt> <dt>

[**設定檔物件**](profile-object.md)
</dt> <dt>

[**配置 檔**](profiles.md)
</dt> </dl>

 

 




