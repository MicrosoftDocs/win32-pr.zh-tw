---
title: 更新現有的 DSP 外掛程式
description: 更新現有的 DSP 外掛程式
ms.assetid: 0525030e-eb30-41a0-8191-4a5727736857
keywords:
- 'Windows Media Player 外掛程式、數位信號處理 (DSP) '
- '外掛程式，數位信號處理 (DSP) '
- 數位信號處理外掛程式，更新
- DSP 外掛程式，更新
- Windows Media Player、DSP 外掛程式的版本
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 725a7a752206f4d321af9deb106df82c40b677dd719182660c5940cac4788244
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120122728"
---
# <a name="updating-existing-dsp-plug-ins"></a>更新現有的 DSP 外掛程式

在 Windows Media Player 11 SDK 發行之前建立的 DSP 外掛程式，可能無法如預期般運作，因為在 Windows Vista 上執行的 Windows Media Player 11。 為了確保在 Windows Vista 上執行 Windows Media Player 11 的客戶可以使用您的外掛程式，您必須對您的 DSP 外掛程式程式碼進行一些變更、重新編譯您的專案，然後將更新的外掛程式散發給您的客戶。

使用最新版 Windows Media Player 外掛程式 wizard 建立的專案將包含必要的更新。 請參閱[Windows Media Player 11 的 DSP 外掛程式 Wizard 更新](updates-to-the-dsp-plug-in-wizard-for-windows-media-player-11.md)。  (建議您執行 wizard 來建立新的範例專案，然後使用 Visual Studio 所隨附的 Windiff.exe 工具，來檢查範例程式碼與您的實際執行程式碼之間的差異。 ) 

您必須對任何現有的 DSP 外掛程式進行三項主要變更：

-   變更外掛程式註冊的方式。 您現有的外掛程式可能會將執行緒模型註冊為「單元」。 在 Windows Vista 上執行的 Windows Media Player 11 需要 DSP 外掛程式將執行緒模型註冊為「兩者」。 您可以藉由變更 *專案名稱*.rgs 檔中的執行緒模型值來修正此問題，如下所示：

    ```C++
    val ThreadingModel = s 'Both'
    
    ```

    

    > [!Note]  
    > 將執行緒模型指定為「兩者」會移除 COM 針對自訂介面的呼叫所提供的任何序列化。 如果您從多個執行緒呼叫自訂介面，就必須自行提供此序列化。

     

    Windows Media Player 11 可確保 DMO 介面的呼叫已正確序列化。

    1.  使用新的外掛程式類型，將呼叫新增至 [IWMPMediaPluginRegistrar：： WMPRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpregisterplayerplugin) 和 [IWMPMediaPluginRegistrar：： WMPUnRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpunregisterplayerplugin) ，並將 PLUGINTYPE 和 OUTOFPROC 中的 WMP DllRegisterServer DSP DllUnregisterServer 用於 \_ \_ \_ *projectnamedll*.cpp 檔案。 如需詳細資訊，請參閱這些方法的參考頁面。
    2.  建立並散發 proxy/stub DLL，以啟用任何自訂介面的 COM 封送處理，該介面是由外掛程式類別所執行或建立。 自訂介面是您定義和執行的任何專屬介面，可供外掛程式物件使用。 這包括您的屬性頁所使用的自訂介面（如果您有提供的話），但也可能包含連接至 UI 外掛程式的介面（例如）。 外掛程式嚮導所建立的自訂介面範例是 *Iprojectname*。 非自訂介面的介面範例包括 **IMediaObject** 和 **IWMPPluginEnable**。

如果您的 DSP 外掛程式處理音訊，您也必須新增下列新音訊格式的支援：

-   WAVE \_ 格式 \_ IEEE \_ FLOAT
-   WAVE \_ 格式可延伸 \_ 的 subformat KSDATAFORMAT \_ 子類型 \_ IEEE \_ FLOAT。

如果您的 DSP 外掛程式處理影片，您必須新增 NV12 影片格式的支援。

請參閱嚮導所建立的範例音訊或影片 DSP 外掛程式，以取得如何處理這些格式類型的範例。

## <a name="about-the-proxystub-project"></a>關於 Proxy/Stub Project

若要為您的 DSP 外掛程式建立 proxy/存根 DLL 專案，最簡單的方式就是執行 DSP 外掛程式 wizard。 這會建立範例 proxy/stub 專案，讓您可以修改以使用現有的程式碼。 您將需要進行下列變更：

1.  從程式碼中移除自訂介面的任何現有定義。 例如，來自 Windows Media Player 10 SDK 的 DSP 外掛程式 wizard 會使用 **interface** 關鍵字，在 *專案名稱*.h 檔案中建立 *Iprojectname* 介面定義。
2.  在 proxy/stub 專案的 IDL 檔案中定義您的自訂介面。
3.  在您的主要專案之前，建立 proxy/stub 專案。 如果兩個專案都是相同方案的一部分，您可以設定 Visual Studio 自動完成這項作業。
4.  MIDL 編譯器會建立新的標頭檔，其名稱格式為專案名稱 \_ h.h。 您必須將此標頭包含在主要專案 (的專案 *名稱*.h) 中。 它包含自訂介面的定義。

## <a name="distributing-the-updated-plug-in"></a>發佈更新的外掛程式

您可以將更新的外掛程式安裝在使用者電腦上，就像過去一樣。 不過，您現在也必須散發並註冊 proxy/stub DLL。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**DSP 外掛程式開發人員總覽**](dsp-plug-in-developer-overview.md)
</dt> </dl>

 

 




