---
title: 執行自訂音訊端點列舉值
description: 從 Windows Server 2008 R2 開始，您可以在遠端桌面通訊協定提供者中執行自訂的遠端音訊端點枚舉器。
ms.assetid: 684bd62e-1e28-4330-a3c5-6bce684d652d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ae135d19e13e3b78fddbdd58bccd476b7e5ee7a
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122478854"
---
# <a name="implementing-a-custom-audio-endpoint-enumerator"></a>執行自訂音訊端點列舉值

從 Windows Server 2008 R2 開始，您可以在遠端桌面通訊協定提供者中執行自訂的遠端音訊端點枚舉器。 遠端桌面通訊協定提供者可以使用自訂音訊端點列舉值，來抓取具有一組特定功能的音訊端點集合。

**若要執行自訂遠端音訊端點列舉值**

1.  您的自訂端點列舉值解決方案應採用四種主要類型的物件：裝置列舉值物件、裝置集合物件、裝置物件和屬性存放區物件。

    

    
| 物件型別 | 說明 | 
|-------------|-------------|
| 裝置列舉值物件<br /> | 裝置列舉值物件提供端點列舉值功能。 它會公開傳回預設端點和指定端點集合的方法。 例如，根據指定的準則，列舉值可以傳回通訊端點、播放端點或捕捉端點。 裝置列舉值物件必須執行 <a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator"><strong>IMMDeviceEnumerator</strong></a> 介面。<br /> | 
| 裝置集合物件<br /> | 裝置集合物件代表音訊裝置的集合。 它必須執行 <a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdevicecollection"><strong>IMMDeviceCollection</strong></a> 介面。<br /> | 
| 裝置物件<br /> | 裝置物件代表特定音訊裝置。 它可讓您存取音訊裝置的屬性存放區，並公開裝置上可用的音訊播放和捕捉介面。 裝置物件必須執行 <a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdevice"><strong>IMMDevice</strong></a> 和 <a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immendpoint"><strong>IMMEndpoint</strong></a> 介面。<br /> | 
| 屬性存放區物件<br /> | 屬性存放區物件會公開與音訊裝置相關聯的屬性。 系統會使用其中一些屬性，但應用程式也可以使用音訊端點儲存任意屬性。<br /> 所有音訊裝置都有下列三個屬性：<br /><ul><li><a href="/windows/desktop/CoreAudio/pkey-deviceinterface-friendlyname"><strong>PKEY_DeviceInterface_FriendlyName</strong></a></li><li><a href="/windows/desktop/CoreAudio/pkey-device-devicedesc"><strong>PKEY_Device_DeviceDesc</strong></a></li><li><a href="/windows/desktop/CoreAudio/pkey-device-friendlyname"><strong>PKEY_Device_FriendlyName</strong></a></li></ul>    屬性存放區物件必須執行 <a href="/windows/win32/api/propsys/nn-propsys-ipropertystore">IPropertyStore</a> 介面。<br /> | 


    

     

2.  自訂端點列舉值必須在可以載入音訊系統和其他應用程式的 DLL 中實作為。 DLL 必須經過簽署，才能讓安全的進程載入它。 DLL 必須執行並匯出 [**GetTSAudioEndpointEnumeratorForSession**](gettsaudioendpointenumeratorforsession.md) 函式，作為自訂端點列舉值的進入點。

遠端桌面服務服務會呼叫 [**QueryProperty**](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-queryproperty)方法，並將 *QueryType* 參數設定為 **WTS \_ QUERY \_ AUDIOENUM \_ DLL** 來取得列舉值物件的名稱。

自訂列舉值物件使用類似 COM 的介面和類似 COM 的參考計數機制，但它們不是真正的 COM 物件。 自訂端點列舉值必須能夠使用不支援 COM 之應用程式所使用的舊版音訊介面。 基於這個理由，自訂端點列舉值不能依賴 COM 的生命週期管理機制。 音訊端點列舉值的取用者（例如 MMDevAPI.dll）會在使用者應用程式需要時載入自訂端點列舉值 DLL，而且當列舉值持有裝置列舉值物件、裝置集合物件、裝置物件或屬性存放區物件的參考時，就不會卸載列舉值。 但是，這些取用者不可能追蹤自訂端點列舉值所擁有之其他類型物件的參考。 因此，我們建議您的自訂端點列舉值不會建立任何可能存留時間這四種物件類型的物件。

## <a name="to-implement-a-custom-audio-endpoint"></a>若要執行自訂音訊端點

若要執行自訂音訊裝置列舉值，您必須執行自訂音訊端點。 自訂音訊裝置的連結方式是使用下列兩個語句：

-   `IMMDevice::Activate(IAudioOutputEndpointRT)`
-   `IMMDevice::Activate(IAudioInputEndpointRT)`

我們不希望您在自訂音訊裝置列舉值中執行 [**IMMDevice：： Activate**](/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-immdevice-activate) 介面的完整清單。 相反地，您應該執行 [**IAudioOutputEndpointRT**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudiooutputendpointrt) 和 [**IAudioInputEndpointRT**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioinputendpointrt)。 您可以選擇性地執行一些其他工作，例如 [**IAudioEndpointVolume**](/windows/desktop/api/endpointvolume/nn-endpointvolume-iaudioendpointvolume)。 針對您未執行的任何介面，您應該傳回 **E \_ NOINTERFACE** (您必須使用這個特定的失敗代碼) 。 Windows 接著會切換回介面的庫存實 (例如， [**IAudioClient2**](/windows/desktop/api/audioclient/nn-audioclient-iaudioclient2)) 。

如需如何執行和註冊音訊端點的其他參考檔，請參閱 [**IAudioInputEndpointRT**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioinputendpointrt)。 如需顯示 WASAPI 運作方式的圖表，請參閱 [使用者模式音訊元件](/windows/desktop/CoreAudio/user-mode-audio-components)。 請注意，所有使用者模式音訊都是從 Windows Server 2008 開始新增的。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[建立遠端桌面通訊協定提供者](creating-a-custom-remote-protocol.md)
</dt> <dt>

[**GetTSAudioEndpointEnumeratorForSession**](gettsaudioendpointenumeratorforsession.md)
</dt> <dt>

[**IMMDevice**](/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdevice)
</dt> <dt>

[**IMMDeviceCollection**](/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdevicecollection)
</dt> <dt>

[**IMMDeviceEnumerator**](/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator)
</dt> <dt>

[**IMMEndpoint**](/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immendpoint)
</dt> <dt>

[IPropertyStore](/windows/win32/api/propsys/nn-propsys-ipropertystore)
</dt> </dl>
