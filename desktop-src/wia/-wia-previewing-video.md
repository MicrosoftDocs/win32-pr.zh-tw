---
description: IWiaVideo 介面可讓應用程式觀看影片，並從它中捕捉影像。
ms.assetid: 59eddbdc-4957-44be-a602-0763f3385e89
title: '預覽影片 (WIA) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ca270adf4e6461beac409315c782101744e8afeb72c33f07aa7bbc999e24751
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119813718"
---
# <a name="previewing-video-wia"></a>預覽影片 (WIA) 

[**IWiaVideo**](/windows/desktop/api/Wiavideo/nn-wiavideo-iwiavideo)介面可讓應用程式觀看影片，並從它中捕捉影像。 請執行下列步驟來選取串流影片裝置，並在視窗中顯示影片串流。

-   呼叫 [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) 以取得 [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) 介面的指標。
-   使用 [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr)介面的 [**IWiaDevMgr：： EnumDeviceInfo**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-enumdeviceinfo)方法，取得 [**IEnumWIA \_ 開發人員 \_ 資訊**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info)介面的指標。 如需有關如何列舉裝置的指示，請參閱列舉系統裝置。
-   使用 [**IEnumWIA \_ DEV \_ INFO**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info)介面可取得找到的每個 Windows 映像取得 (WIA) 裝置的 [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage)介面指標。
-   使用 [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) 介面取得所需裝置的 DeviceID 屬性。 串流影片裝置具有 [WIA \_ DIP \_ 開發 \_ 類型] 屬性集的 StiDeviceTypeStreamingVideo 旗標。
-   使用 [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) 介面取得 [WIA \_ DPV IMAGES] \_ \_ 目錄屬性值。
-   呼叫 [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) 以取得 [**IWiaVideo**](/windows/desktop/api/Wiavideo/nn-wiavideo-iwiavideo) 介面的指標。
-   將 [**IWiaVideo**](/windows/desktop/api/Wiavideo/nn-wiavideo-iwiavideo)介面的 [**IWiaVideo：： ImagesDirectory**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-get_imagesdirectory)屬性設定為從 WIA \_ DPV \_ IMAGES \_ 目錄屬性值收到的值。
-   在 [**IWiaVideo**](/windows/desktop/api/Wiavideo/nn-wiavideo-iwiavideo)介面上呼叫 [**IWiaVideo：： CreateVideoByWiaDevID**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-createvideobywiadevid) ，並傳遞串流映射裝置的裝置識別碼，以及要顯示影片的視窗控制碼。

> [!Note]  
> WIA 不支援 Windows Server 2003、Windows Vista 或更新版本中的影片裝置。 針對這些版本的 Windows，使用[DirectShow](/previous-versions//ms783323(v=vs.85))從影片取得影像。

 

 

 
