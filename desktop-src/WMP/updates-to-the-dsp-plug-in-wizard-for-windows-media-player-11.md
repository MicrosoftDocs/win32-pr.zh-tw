---
title: Windows Media Player 11 的 DSP 外掛程式嚮導更新
description: Windows Media Player 11 的 DSP 外掛程式嚮導更新
ms.assetid: 975c18d5-06d7-4db2-a558-bc6557963425
keywords:
- Windows Media Player 外掛程式，外掛程式嚮導
- 外掛程式、外掛程式嚮導
- 數位信號處理外掛程式，外掛程式嚮導
- DSP 外掛程式，外掛程式嚮導
- 外掛程式嚮導
- Visual Studio，DSP 外掛程式 wizard
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a8efe798a3c324f9ecfac0a5b6021db4ea5abdf
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104374459"
---
# <a name="updates-to-the-dsp-plug-in-wizard-for-windows-media-player-11"></a>Windows Media Player 11 的 DSP 外掛程式嚮導更新

Windows Media Player 11 SDK 引進了下列對 DSP 外掛程式 wizard 的變更：

-   外掛程式會將執行緒模型註冊為「兩者」。 這可讓外掛程式在 Windows Vista 上的媒體基礎管線中執行。 請參閱 *專案名稱*.rgs 檔。

    -   音訊 DSP 外掛程式支援下列兩種額外的格式：

    <!-- -->

    -   WAVE \_ 格式 \_ IEEE \_ FLOAT
    -   WAVE \_ 格式可延伸 \_ 的 subformat KSDATAFORMAT \_ 子類型 \_ IEEE \_ FLOAT。

    請參閱 *專案名稱*.cpp 檔案。

    1.  影片 DSP 外掛程式支援 NV12 影片格式。
    2.  外掛程式會使用新的外掛程式類型，對 [IWMPMediaPluginRegistrar：： WMPRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpregisterplayerplugin) 和 [IWMPMediaPluginRegistrar：： WMPUnRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpunregisterplayerplugin) 進行額外的呼叫： WMP \_ PLUGINTYPE \_ DSP \_ OUTOFPROC。 請參閱專案的 *projectnamedll*.cpp 檔案。
    3.  每個方案中的其他專案會為屬性頁面設定自訂介面建立 proxy/存根 DLL。 請參閱 *projectnamePS* 專案。
    4.  對已被取代之方法的呼叫已變更為使用最新版本。
    5.  您可以藉由執行 **IMFTransform** 來藉由執行 **IMediaObject** 和 MFT，來產生雙重模式外掛程式，以做為一。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**DSP 外掛程式嚮導**](dsp-plug-in-wizard.md)
</dt> </dl>

 

 




