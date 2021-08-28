---
description: 使用 IKsControl 介面存取音訊屬性
ms.assetid: 72bf9164-96c6-4543-b858-19480b032fdb
title: 使用 IKsControl 介面存取音訊屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b763b874730981907d61ed7d4d2f46f4a9b053705b2747064c2505b9c5e90b14
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088220"
---
# <a name="using-the-ikscontrol-interface-to-access-audio-properties"></a>使用 IKsControl 介面存取音訊屬性

在罕見的情況下，特殊的音訊應用程式可能需要使用 [**IKsControl**](/windows-hardware/drivers/ddi/ksproxy/nn-ksproxy-ikscontrol) 介面，來存取 [DeviceTopology API](devicetopology-api.md) 或 [MMDevice API](mmdevice-api.md)未公開之音訊介面卡的特定硬體功能。 **IKsControl** 介面會讓核心串流 (KS) 裝置的屬性、事件和方法可供使用者模式應用程式使用。 音訊應用程式的主要興趣是 KS 屬性。 **IKsControl** 介面可搭配 DeviceTopology API 和 MMDevice API 使用，以存取音訊介面卡的 KS 屬性。

[**IKsControl**](/windows-hardware/drivers/ddi/ksproxy/nn-ksproxy-ikscontrol)介面主要是供撰寫控制台應用程式來管理其音訊硬體的硬體供應商使用。 針對未系結至特定硬體裝置的一般用途音訊應用程式， **IKsControl** 較不實用。 原因是硬體廠商經常採用專屬機制來存取裝置的音訊內容。 相較于 DeviceTopology API，它會隱藏硬體特定的驅動程式，並提供相當一致的介面來存取音訊屬性，而應用程式會使用 **IKsControl** 直接與驅動程式通訊。 如需 **IKsControl** 的詳細資訊，請參閱 Windows DDK 檔。

如同在 [裝置拓撲](device-topologies.md)中所討論的，介面卡裝置拓撲中的子單位可能會支援下表左邊資料行中所顯示的一或多個函式特定的控制介面。 資料表右邊資料行中的每個專案都是對應至左側控制項介面的 KS 屬性。 控制項介面可方便您存取屬性。 大部分的音訊驅動程式都會使用 KS 屬性來代表次單元連接的函式特定處理功能 (也稱為「KS 節點」（) 在其音訊介面卡的拓撲中）。 如需有關 ks 屬性和 ks 節點的詳細資訊，請參閱 Windows DDK 檔。



| 控制項介面                                          | KS 屬性                        |
|------------------------------------------------------------|------------------------------------|
| [**IAudioAutoGainControl**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioautogaincontrol)     | KSPROPERTY \_ 音訊 \_ AGC             |
| [**IAudioBass**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiobass)                           | KSPROPERTY \_ 音訊 \_ 低音            |
| [**IAudioChannelConfig**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiochannelconfig)         | KSPROPERTY \_ 音訊 \_ 通道 \_ 設定 |
| [**IAudioInputSelector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioinputselector)         | KSPROPERTY \_ 音訊 \_ MUX \_ 來源     |
| [**IAudioLoudness**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioloudness)                   | KSPROPERTY \_ 音訊 \_ 音量        |
| [**IAudioMidrange**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiomidrange)                   | KSPROPERTY \_ 音訊 \_ 中間             |
| [**IAudioMute**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiomute)                           | KSPROPERTY \_ 音訊 \_ 靜音            |
| [**IAudioOutputSelector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiooutputselector)       | KSPROPERTY \_ 音訊 \_ DEMUX \_ 目的地     |
| [**IAudioPeakMeter**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiopeakmeter)                 | KSPROPERTY \_ 音訊 \_ PEAKMETER       |
| [**IAudioTreble**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiotreble)                       | KSPROPERTY \_ 音訊 \_ 高音          |
| [**IAudioVolumeLevel**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiovolumelevel)             | KSPROPERTY \_ 音訊 \_ VOLUMELEVEL     |
| [**IDeviceSpecificProperty**](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicespecificproperty) | KSPROPERTY \_ 音訊 \_ 開發 \_ 專用   |



 

某些音訊介面卡的拓撲可能包含具有上表未列出之 KS 屬性的次單元連接。 例如，假設特定次級的 [**IPart：： GetSubType**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getsubtype) 方法呼叫會抓取 GUID 值 KSNODETYPE \_ 語氣。 此子類型 GUID 表示子單位支援下列其中一個或多個 KS 屬性：

-   KSPROPERTY \_ 音訊 \_ 低音
-   KSPROPERTY \_ 音訊 \_ 中間
-   KSPROPERTY \_ 音訊 \_ 高音
-   KSPROPERTY \_ 音訊 \_ 低音 \_ 提升

這份清單中的前三個屬性可透過上表所顯示的控制項介面存取，但 KSPROPERTY \_ 音訊 \_ 低音 \_ 提升屬性在 DeviceTopology API 中沒有對應的控制介面。 但是，如果子單位支援屬性，則應用程式可以使用 [**IKsControl**](/windows-hardware/drivers/ddi/ksproxy/nn-ksproxy-ikscontrol) 介面來存取這個屬性。

您必須執行下列步驟，才能存取 \_ \_ 子類型 KSNODETYPE 語氣之子單位的 KSPROPERTY 音訊低音 \_ 增強屬性 \_ ：

1.  呼叫 [**IConnector：： GetDeviceIdConnectedTo**](/windows/desktop/api/Devicetopology/nf-devicetopology-iconnector-getdeviceidconnectedto) 或 [**IDeviceTopology：： GetDeviceId**](/windows/desktop/api/Devicetopology/nf-devicetopology-idevicetopology-getdeviceid) 方法，以取得可識別介面卡裝置的裝置識別碼字串。 此字串類似于 [端點識別碼字串](endpoint-id-strings.md)，不同之處在于它會識別介面卡裝置，而不是端點裝置。 如需介面卡裝置與端點裝置之間差異的詳細資訊，請參閱 [音訊端點裝置](audio-endpoint-devices.md)。
2.  以裝置識別碼字串呼叫 [**IMMDeviceEnumerator：： GetDevice**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice)方法，以取得介面卡裝置的 [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice)介面。 這個 **IMMDevice** 介面與 **IMMDevice 介面** 中所述的介面相同，但它代表介面卡裝置，而不是端點裝置。
3.  藉由呼叫 [**IMMDevice：： Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate)方法並將參數 *Iid* 設定為 **REFIID** iid IKsControl，以取得子單位上的 [**IKsControl**](/windows-hardware/drivers/ddi/ksproxy/nn-ksproxy-ikscontrol)介面 \_ 。 請注意，此 **啟動** 方法所支援的介面（適用于介面卡裝置）不同于端點裝置的 **啟動** 方法所支援的介面。 尤其是，介面卡裝置的 **啟動** 方法支援 **IKsControl**。
4.  呼叫 [**IPart：： GetLocalId**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getlocalid) 方法，以取得子領域的本機識別碼。
5.  建立 KS 屬性要求。 要求所需的 KS 節點識別碼包含在上一個步驟中取得之本機識別碼的16個最少有效位。
6.  藉由呼叫 [**IKsControl：： KsProperty**](/windows-hardware/drivers/ddi/ksproxy/nf-ksproxy-ikscontrol-ksproperty) 方法，將 KS 屬性要求傳送到音訊驅動程式。 如需此方法的詳細資訊，請參閱 Windows DDK 檔。

下列程式碼範例會 \_ \_ \_ 從子類型 KSNODETYPE 語氣的子單位，抓取 KSPROPERTY 音訊低音增強屬性的值 \_ ：


```C++
//-----------------------------------------------------------
// This function calls the IKsControl::Property method to get
// the value of the KSPROPERTY_AUDIO_BASS_BOOST property of
// a subunit. Parameter pPart should point to a part that is
// a subunit with a subtype GUID value of KSNODETYPE_TONE.
//-----------------------------------------------------------
#define PARTID_MASK 0x0000ffff
#define EXIT_ON_ERROR(hres)  \
              if (FAILED(hres)) { goto Exit; }
#define SAFE_RELEASE(punk)  \
              if ((punk) != NULL)  \
                { (punk)->Release(); (punk) = NULL; }

const IID IID_IKsControl = __uuidof(IKsControl);

HRESULT GetBassBoost(IMMDeviceEnumerator *pEnumerator,
                     IPart *pPart, BOOL *pbValue)
{
    HRESULT hr;
    IDeviceTopology *pTopology = NULL;
    IMMDevice *pPnpDevice = NULL;
    IKsControl *pKsControl = NULL;
    LPWSTR pwszDeviceId = NULL;

    if (pEnumerator == NULL || pPart == NULL || pbValue == NULL)
    {
        return E_INVALIDARG;
    }

    // Get the topology object for the adapter device that contains
    // the subunit represented by the IPart interface.
    hr = pPart->GetTopologyObject(&pTopology);
    EXIT_ON_ERROR(hr)

    // Get the device ID string that identifies the adapter device.
    hr = pTopology->GetDeviceId(&pwszDeviceId);
    EXIT_ON_ERROR(hr)

    // Get the IMMDevice interface of the adapter device object.
    hr = pEnumerator->GetDevice(pwszDeviceId, &pPnpDevice);
    EXIT_ON_ERROR(hr)

    // Activate an IKsControl interface on the adapter device object.
    hr = pPnpDevice->Activate(IID_IKsControl, CLSCTX_ALL, NULL, (void**)&pKsControl);
    EXIT_ON_ERROR(hr)

    // Get the local ID of the subunit (contains the KS node ID).
    UINT localId = 0;
    hr = pPart->GetLocalId(&localId);
    EXIT_ON_ERROR(hr)

    KSNODEPROPERTY_AUDIO_CHANNEL ksprop;
    ZeroMemory(&ksprop, sizeof(ksprop));
    ksprop.NodeProperty.Property.Set = KSPROPSETID_Audio;
    ksprop.NodeProperty.Property.Id = KSPROPERTY_AUDIO_BASS_BOOST;
    ksprop.NodeProperty.Property.Flags = KSPROPERTY_TYPE_GET | KSPROPERTY_TYPE_TOPOLOGY;
    ksprop.NodeProperty.NodeId = localId & PARTID_MASK;
    ksprop.Channel = 0;

    // Send the property request.to the device driver.
    BOOL bValue = FALSE;
    ULONG valueSize;
    hr = pKsControl->KsProperty(
                         &ksprop.NodeProperty.Property, sizeof(ksprop),
                         &bValue, sizeof(bValue), &valueSize);
    EXIT_ON_ERROR(hr)

    *pbValue = bValue;

Exit:
    SAFE_RELEASE(pTopology)
    SAFE_RELEASE(pPnpDevice)
    SAFE_RELEASE(pKsControl)
    CoTaskMemFree(pwszDeviceId);
    return hr;
}

```



在上述程式碼範例中，GetBassBoost 函數會採用下列三個參數：

-   `pEnumerator` 指向音訊端點列舉值的 [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) 介面。
-   `pPart` 指向具有 KSNODETYPE 語氣子類型之子單位的 [**IPart**](/windows/desktop/api/Devicetopology/nn-devicetopology-ipart) 介面 \_ 。
-   `pbValue` 指向 **BOOL** 變數，函式會將屬性值寫入其中。

程式只會在呼叫 [**IPart：： GetSubType**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getsubtype) 之後呼叫 GetBassBoost，並判斷子單位的子類型為 KSNODETYPE \_ 語氣。 如果啟用了低音提升，則屬性值為 **TRUE** 。 如果已停用低音提升，則為 **FALSE** 。

在 GetBassBoost 函式的開頭， [**IPart：： GetTopologyObject**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-gettopologyobject) 方法的呼叫會取得包含 KSNODETYPE 語氣子單位的介面卡裝置 [**IDeviceTopology**](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicetopology) 介面 \_ 。 [**IDeviceTopology：： GetDeviceId**](/windows/desktop/api/Devicetopology/nf-devicetopology-idevicetopology-getdeviceid)方法呼叫會捕獲識別介面卡裝置的裝置識別碼字串。 [**IMMDeviceEnumerator：： GetDevice**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice)方法呼叫會接受裝置識別碼字串做為輸入參數，並取得介面卡裝置的 [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice)介面。 接下來， [**IMMDevice：： Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) 方法呼叫會抓取子單位的 [**IKsControl**](/windows-hardware/drivers/ddi/ksproxy/nn-ksproxy-ikscontrol) 介面。 如需有關 **IKsControl** 介面的詳細資訊，請參閱 Windows DDK 檔。

接下來，上述程式碼範例會建立 [**KSNODEPROPERTY \_ 音訊 \_ 通道**](/windows-hardware/drivers/ddi/ksmedia/ns-ksmedia-ksnodeproperty_audio_channel) 結構，以描述低音提升屬性。 此程式碼範例會將結構的指標傳遞至 [**IKsControl：： KsProperty**](/windows-hardware/drivers/ddi/ksproxy/nf-ksproxy-ikscontrol-ksproperty) 方法，該方法會使用結構中的資訊來取得屬性值。 如需有關 **KSNODEPROPERTY \_ 音訊 \_ 通道** 結構和 **IKsControl：： KsProperty** 方法的詳細資訊，請參閱 Windows DDK 檔。

音訊硬體通常會為音訊串流中的每個通道指派不同的低音提升狀態。 基本上，您可以針對某些通道啟用低音提升，並為其他通道停用。 [**KSNODEPROPERTY \_ 音訊 \_ 通道**](/windows-hardware/drivers/ddi/ksmedia/ns-ksmedia-ksnodeproperty_audio_channel)結構包含指定頻道號碼的 **通道** 成員。 如果資料流程包含 *N* 個通道，則通道的編號是從0到 *N*-1。 上述程式碼範例只會針對 channel 0 取得低音提升屬性的值。 這項實行隱含地假設所有通道的低音提升屬性都會一致地設定為相同的狀態。 因此，讀取通道0的低音提升屬性就足以判斷資料流程的低音提升屬性值。 為了與此假設一致，設定增強型屬性的對應函式會將所有通道設定為相同的低音提升屬性值。 這些都是合理的慣例，但並非所有硬體廠商都必須遵循它們。 例如，廠商可能會提供一個控制台應用程式，只對驅動全範圍喇叭的通道啟用低音提升。  (全範圍的喇叭可以從低音到高音播放整個範圍的音效。 ) 在這種情況下，上述程式碼範例所抓取的屬性值可能無法正確呈現資料流程的低音提升狀態。

使用上表所列控制項介面的用戶端可以呼叫 [**IPart：： RegisterControlChangeCallback**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-registercontrolchangecallback) 方法，以便在控制項參數的值變更時註冊通知。 請注意， [**IKsControl**](/windows-hardware/drivers/ddi/ksproxy/nn-ksproxy-ikscontrol) 介面未提供類似的方法，讓用戶端在屬性值變更時註冊通知。 如果 **IKsControl** 支援屬性變更通知，則可能會在另一個應用程式變更屬性值時通知應用程式。 不過，相較于透過 [**IPart**](/windows/desktop/api/Devicetopology/nn-devicetopology-ipart) 通知監視的常用控制項， **IKsControl** 所管理的屬性主要是供硬體廠商使用，而且這些屬性可能只會由廠商所撰寫的控制台應用程式來變更。 如果應用程式必須偵測其他應用程式所做的屬性變更，它可以透過 **IKsControl** 定期輪詢屬性值，來偵測變更。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[程式設計指南](programming-guide.md)
</dt> </dl>

 

 
