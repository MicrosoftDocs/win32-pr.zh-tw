---
description: 裝置可能會產生許多事件，每個事件都可以選擇由許多不同處理常式的其中一個來處理。
ms.assetid: C203B5AB-917C-4543-98D6-EDE02E0B5E49
title: 如何註冊事件處理常式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f96aedc8b6b7944238938539a8fafa5d80c6dc7f1afd4dc5f818ecc91abd08c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120090558"
---
# <a name="how-to-register-an-event-handler"></a>如何註冊事件處理常式

裝置可能會產生許多事件，每個事件都可以選擇由許多不同處理常式的其中一個來處理。 在 Windows XP 中，會定義下列事件：

-   DeviceArrival
-   DeviceRemoval
-   MediaArrival
-   MediaRemoval

## <a name="instructions"></a>指示


事件處理常式是在 **EventHandlers** 索引鍵下定義。 事件處理常式索引鍵的值是使用者在偵測到事件時，必須從中選擇的每個處理常式的名稱。 沒有與這些專案相關聯的資料值。 以下是自訂事件處理常式（稱為 **MyNewRemovalEventHandler**）的範例定義，其提供這些處理常式的可能性給使用者：

-   當名為 Contoso，Inc. 的公司所建立的裝置上偵測到事件時，所要使用的處理常式。
-   如果在名稱為 Fabrikam，Inc. 的公司所建立的裝置上偵測到事件，要使用的處理常式。
-   要在所有其他情況下使用的處理常式。

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  AutoplayHandlers
                     EventHandlers
                        MyNewRemovalEventHandler
                           CompanyContosoHandler [REG_SZ]
                           CompanyFabrikamHandler [REG_SZ]
                           MyRemovalHandler [REG_SZ]
```

定義事件處理常式之後，它必須針對其中一個事件可能的裝置處理常式註冊： DeviceArrival、DeviceRemoval、MediaArrival 或 MediaRemoval。 稍早定義的 MyNewRemovalEventHandler 會用來在名為 MyDeviceHandler 的自訂裝置處理常式下進行 DeviceRemoval，並在下列範例中針對該目的定義。 同樣地，登錄值沒有資料元件。

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  AutoplayHandlers
                     DeviceHandlers
                        EventHandlers
                           DeviceRemoval
                              MyNewRemovalEventHandler
```

WindowsXP 預先定義下列一組 EventHandlers。 

| EventHandlers 索引鍵        | 媒體或檔案類型                             |
|--------------------------|------------------------------------------------|
| HandleCDBurningOnArrival | 空白 CD-R/cd-rw                               |
| ShowPicturesOnArrival    | 圖片檔案                                  |
| PlayMusicFilesOnArrival  | 音樂檔案                                    |
| PlayVideoFilesOnArrival  | 影片檔案                                    |
| PlayCDAudioOnArrival     | 音訊 CD (REDBOOK 格式 CD 與音訊曲目)  |
| PlayDVDMovieOnArrival    | DVD 電影                                     |



 

Windows除了上述的 EventHandlers 以外，Vista 還預先定義了下列一組。 

| EventHandlers 索引鍵              | 媒體或檔案類型   |
|--------------------------------|----------------------|
| PlaySuperVideoCDMovieOnArrival | 超級 VideoCD 電影 |
| PlayVideoCDMovieOnArrival      | VideoCD 電影       |



 

 

 



