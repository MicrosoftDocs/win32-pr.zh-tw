---
description: MSDVDAdm 物件
ms.assetid: 753d2820-4d47-4e07-9f54-9b996e55f0b6
title: MSDVDAdm 物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa4001def80bff94920996dc627869ffecfd6dda3fbc679be79f2b321ac33a1b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072972"
---
# <a name="msdvdadm-object"></a>MSDVDAdm 物件

> [!Note]  
> 此元件可在 Microsoft Windows 2000、Windows XP 和 Windows Server 2003 作業系統中使用。 它在後續版本中可能會變更或無法使用。

 

> [!Note]  
> 此 API 即將淘汰。 如需 DirectShow dvd 播放和流覽的相關資訊，請參閱[dvd 應用程式](dvd-applications.md)。

 

`MSDVDAdm`"administration" 物件的方法和屬性可讓腳本應用程式在 Microsoft® Windows® registry 中修改其預設設定。 登錄是所有 Windows 系統上的資料庫，應用程式可以在其上儲存本身的相關資訊，以便在初始化時或在執行時間時使用。

大部分的方法和屬性都不會設定或抓取 [MSWebDVD](mswebdvd-object.md) 物件本身中的目前值。 例如，這表示當您呼叫 **GetParentalLevel** 時，傳回的值不是目前儲存在物件中的父層級。 相反地，它是儲存在登錄中的預設家長儲存層級。 若要取得目前的父層級，請呼叫 **MSWebDVD** 方法 [**GetPlayerParentalLevel**](getplayerparentallevel-method.md)。 呼叫 [**SaveParentalLevel**](saveparentallevel-method.md) 只會將新的預設家長存取層級寫入登錄;您仍然需要呼叫 **MSWebDVD** 方法 [**SelectParentalLevel**](selectparentallevel-method.md) ，讓變更立即生效于 **MSWebDVD** 物件中。 預設的地區設定識別碼 (LCID) 方法的運作方式類似。

另一方面， [**BookmarkOnStop**](bookmarkonstop-property.md) 和 [**BookmarkOnClose**](bookmarkonclose-property.md) 方法會立即生效，因為 **MSWebDVD** 物件會在使用者停止播放或關閉應用程式時，而不是在初始化期間檢查這些設定。

您可以 `MSDVDAdm` 透過 **MSWebDVD** 的 **DVDAdm** 屬性存取物件。 比方說，如果 **MSWebDVD** 物件名為 "DVD"，請呼叫 **ChangePassword** ，如下列程式碼範例所示。


```C++
DVD.DVDAdm.ChangePassword(sUserName, sOld, sNew)
```



**方法和屬性**

下表列出 MSDVDAdm 物件方法和屬性所公開的方法和屬性。



| 方法                                                          | 描述                                                                                                                                                                      |
|-----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ChangePassword**](changepassword-method.md)                 | 在登錄中儲存新的應用程式密碼。                                                                                                                                |
| [**SaveParentalLevel**](saveparentallevel-method.md)           | 將新的預設家長監護儲存至登錄。                                                                                                                              |
| [**SaveParentalCountry**](saveparentalcountry-method.md)       | 將應用程式的新家長/區域儲存至登錄。                                                                                                             |
| [**ConfirmPassword**](confirmpassword-method.md)               | 測試指定的密碼是否符合先前儲存的密碼。                                                                                                      |
| [**GetParentalLevel**](getparentallevel-method.md)             | 抓取上次儲存至登錄的父層級。                                                                                                                |
| [**GetParentalCountry**](getparentalcountry-method.md)         | 抓取上次儲存至登錄的家長監護/區域。                                                                                                       |
| [**RestoreScreenSaver**](restorescreensaver-method.md)         | 還原系統螢幕保護裝置設定。                                                                                                                                       |
| 屬性                                                        | 描述                                                                                                                                                                      |
| [**DisableScreenSaver**](disablescreensaver-property.md)       | 開啟或關閉系統螢幕保護裝置。                                                                                                                                         |
| [**DefaultAudioLCID**](defaultaudiolcid-property.md)           | 為音訊資料流程設定或抓取使用者指定之預設 LCID 的登錄設定。                                                                                 |
| [**DefaultSubpictureLCID**](defaultsubpicturelcid-property.md) | 針對使用者指定的子圖片資料流程預設 LCID 設定或抓取登錄設定。                                                                            |
| [**DefaultMenuLCID**](defaultmenulcid-property.md)             | 設定或抓取使用者為功能表指定之預設 LCID 的登錄設定。                                                                                            |
| [**BookmarkOnStop**](bookmarkonstop-property.md)               | 設定或抓取值，告知 MSDVDAdm 物件是否要在使用者按一下 [ **停止** ] 按鈕時，自動儲存目前位置和設定的書簽。 |
| [**BookmarkOnClose**](bookmarkonclose-property.md)             | 設定或抓取值，告知 MSDVDAdm 物件是否要在使用者關閉應用程式時，自動儲存目前位置和設定的書簽。     |



 

 

 



