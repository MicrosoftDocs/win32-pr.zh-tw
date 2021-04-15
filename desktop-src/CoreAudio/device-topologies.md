---
description: 裝置拓撲
ms.assetid: 5ac421e5-74a4-40e8-af6f-a99a05ebc3e0
title: 裝置拓撲
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31e0af267bb4a0fa924ee23d36a2a615ac5ae7fa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510725"
---
# <a name="device-topologies"></a>裝置拓撲

[DEVICETOPOLOGY api](devicetopology-api.md)可讓用戶端控制無法透過[MMDevice api](mmdevice-api.md)、 [WASAPI](wasapi.md)或[EndpointVolume api](endpointvolume-api.md)存取的各種音訊配接器內部功能。

如先前所述， [MMDEVICE api](mmdevice-api.md)、 [WASAPI](wasapi.md)和 [EndpointVolume api](endpointvolume-api.md) 會將麥克風、喇叭、耳機和其他音訊輸入和輸出裝置呈現給用戶端作為 [音訊端點裝置](audio-endpoint-devices.md)。 端點裝置模型可讓用戶端方便存取音訊裝置中的音量和靜音控制項。 只需要這些簡單控制項的用戶端可以避免將硬體裝置的內部拓撲用於音訊介面卡。

在 Windows Vista 中，音訊引擎會自動設定音訊裝置的拓撲，以供音訊應用程式使用。 因此，應用程式很少需要使用 DeviceTopology API 來達到此目的。 例如，假設音訊介面卡包含可從線路輸入或麥克風捕捉串流的輸入多工器，但無法同時從兩個端點裝置捕獲資料流程。 假設使用者已啟用獨佔模式應用程式，以依照共用模式應用程式來搶先使用音訊端點裝置，如 [獨佔模式串流](exclusive-mode-streams.md)中所述。 如果共用模式應用程式在獨佔模式應用程式開始從麥克風錄製串流時，從行輸入記錄資料流程，則音訊引擎會自動將多工器從線路輸入切換至麥克風。 相反地，在舊版 Windows （包括 Windows XP）中，此範例中的獨佔模式應用程式會使用 Windows 多媒體應用程式開發介面中的 **mixerXxx** 函式來跨越介面卡裝置的拓撲、探索多工器，並設定多工器以選取麥克風輸入。 在 Windows Vista 中，不再需要這些步驟。

不過，某些用戶端可能需要明確控制無法透過 MMDevice API、WASAPI 或 EndpointVolume API 存取的音訊硬體控制項類型。 針對這些用戶端，DeviceTopology API 可讓您遍歷介面卡裝置的拓撲，以探索及管理裝置中的音訊控制項。 使用 DeviceTopology API 的應用程式必須謹慎設計，以避免干擾 Windows 音訊原則，並干擾與其他應用程式共用之音訊裝置的內部設定。 如需 Windows 音訊原則的詳細資訊，請參閱 [使用者模式音訊元件](user-mode-audio-components.md)。

DeviceTopology API 提供介面來探索和管理裝置拓撲中的下列音訊控制項類型：

-   自動增益控制
-   低音控制
-   輸入選取器 (多工器) 
-   音量控制項
-   中型控制項
-   靜音控制
-   輸出選取器 (信號信號) 
-   尖峰計量
-   高音控制項
-   音量控制

此外，DeviceTopology API 可讓用戶端查詢介面卡裝置，以取得其所支援之串流格式的相關資訊。 標頭檔 Devicetopology 會定義 DeviceTopology API 中的介面。

下圖顯示 PCI 介面卡部分的數個連線裝置拓撲範例，可從麥克風、線路輸入和 CD 播放機捕獲音訊。

![四個連線裝置拓撲的範例](images/fig2.jpg)

上圖顯示從類比輸入到系統匯流排的資料路徑。 下列每個裝置都會以具有 [**IDeviceTopology**](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicetopology) 介面的裝置拓撲物件表示：

-   Wave capture 裝置
-   輸入多工器裝置
-   端點裝置 A
-   端點裝置 B

請注意，拓撲圖結合了介面卡裝置 (wave 捕捉和輸入多工器裝置) 與端點裝置。 透過裝置之間的連線，音訊資料會從一部裝置傳遞到下一個裝置。 在連線的每一端都是連接器 (在圖表中標示為 Con，) 資料進入或離開裝置的位置。

在圖表的左邊緣，線路輸入和麥克風插孔的信號會進入端點裝置。

在 wave capture 裝置和輸入多工器裝置中，是串流處理函式，在 DeviceTopology API 的術語中，稱為次單元連接。 上圖顯示下列類型的次單元連接：

-   磁片區控制 (標示的音量) 
-   將控制項靜音 (標示為靜音) 
-   多工器 (或輸入選取器;標記的 MUX) 
-   類比轉數位轉換器 (標示的 ADC) 

[磁片區]、[靜音] 和 [多工器] 次單元連接中的設定可由用戶端控制，而 DeviceTopology API 則提供控制介面給用戶端來控制這些設定。 在此範例中，ADC 子單位沒有任何控制設定。 因此，DeviceTopology API 不會提供任何 ADC 的控制介面。

在 DeviceTopology API 的術語中，連接器和次單元連接屬於相同的一般類別（部分）。 無論是連接器或次單元連接，所有零件都能提供一組通用的函式。 DeviceTopology API 會執行 [**IPart**](/windows/desktop/api/Devicetopology/nn-devicetopology-ipart) 介面，以代表連接器和次單元連接通用的一般函數。 API 會執行 [**IConnector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iconnector) 和 [**ISubunit**](/windows/win32/api/devicetopology/nn-devicetopology-isubunit) 介面，以代表連接器和次單元連接的特定層面。

DeviceTopology API 會從核心串流處理 wave capture 裝置和輸入多工器裝置的拓朴 (KS) 篩選器，音訊驅動程式會將這些篩選器公開給作業系統來代表這些裝置。  (音訊介面卡驅動程式會執行 **IMiniportWaveXxx** 和 **IMiniportTopology** 介面，以代表這些篩選器的硬體相依部分;如需這些介面和有關 KS 篩選器的詳細資訊，請參閱 Windows DDK 檔。 ) 

DeviceTopology API 會在上圖中，建立代表端點裝置 A 和 B 的簡單拓撲。 端點裝置的裝置拓撲是由單一連接器所組成。 此拓撲只是端點裝置的預留位置，不包含處理音訊資料的次單元連接。 事實上，介面卡裝置包含用戶端應用程式用來控制音訊處理的所有次單元連接。 端點裝置的裝置拓撲主要做為探索介面卡裝置之裝置拓撲的起點。

裝置拓撲中兩個元件之間的內部連接稱為連結。 DeviceTopology API 提供的方法，可讓您將連結從某個元件的連結到裝置拓撲中的下一個部分。 此 API 也會提供方法來進行裝置拓撲之間的連接。

為了開始探索一組已連線的裝置拓撲，用戶端應用程式會啟用音訊端點裝置的 **IDeviceTopology** 介面。 端點裝置中的連接器會連接到音訊介面卡或網路中的連接器。 如果端點連線到音訊介面卡上的裝置，則 DeviceTopology API 中的方法會在連線的另一端取得介面卡裝置的 **IDeviceTopology** 介面參考，讓應用程式能夠從端點到介面卡的連線逐步進行。 另一方面，網路沒有裝置拓撲。 網路連接會使用管線將音訊串流輸送至遠端存取系統的用戶端。

DeviceTopology API 只會提供音訊介面卡中硬體裝置拓撲的存取權。 圖表左邊緣的外部裝置和右邊邊緣的軟體元件超出 API 的範圍。 圖表任一側的虛線表示 DeviceTopology API 的限制。 用戶端可以使用 API 來探索從輸入插孔延伸至系統匯流排的資料路徑，但是 API 無法滲透于這些界限之外。

上圖中的每個連接器都有相關聯的連線類型，指出連接器所進行的連線類型。 因此，連接兩端的連接器一律具有相同的連線類型。 連線類型是由 [**ConnectorType**](/windows/win32/api/devicetopology/ne-devicetopology-connectortype) 列舉值（實體 \_ 外部、實體 \_ 內部、軟體 \_ 固定、軟體 \_ IO 或網路）所表示。 輸入多工器裝置與端點裝置 A 和 B 之間的連線是實體 \_ 外部類型，也就是說，連線代表外部裝置的實體連線 (換句話說，就是使用者可存取的音訊插孔) 。 從內部 CD 播放機到類比信號的連接是實體 \_ 內部類型，表示安裝在系統底座內的輔助裝置實體連接。 Wave capture 裝置和輸入多工器裝置之間的連線類型為「軟體 \_ 固定」，這表示永久連線是固定的，且無法在軟體控制下設定。 最後，連接到圖表右側的系統匯流排類型為「軟體 \_ IO」，這表示連線的資料 i/o 是由軟體控制下的 DMA 引擎所執行。  (圖表不包含網路連接類型的範例。 ) 

用戶端會開始遍歷端點裝置上的資料路徑。 首先，用戶端會取得代表端點裝置的 [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) 介面，如 [列舉音訊裝置](enumerating-audio-devices.md)所述。 為了取得端點裝置的 **IDeviceTopology** 介面，用戶端會呼叫 [**IMMDevice：： Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) 方法，並將參數 *iid* 設定為 REFIID iid \_ IDeviceTopology。

在上圖的範例中，輸入多工器裝置包含的所有硬體控制項都 (磁片區、靜音和多工器，) 適用于來自線路輸入和麥克風插孔的捕獲資料流程。 下列程式碼範例示範如何從線路輸入或麥克風的端點裝置的 **IMMDevice** 介面取得輸入多工器裝置的 **IDeviceTopology** 介面：


```C++
//-----------------------------------------------------------
// The input argument to this function is a pointer to the
// IMMDevice interface of an endpoint device. The function
// outputs a pointer (counted reference) to the
// IDeviceTopology interface of the adapter device that
// connects to the endpoint device.
//-----------------------------------------------------------
#define EXIT_ON_ERROR(hres)  \
              if (FAILED(hres)) { goto Exit; }
#define SAFE_RELEASE(punk)  \
              if ((punk) != NULL)  \
                { (punk)->Release(); (punk) = NULL; }

const IID IID_IDeviceTopology = __uuidof(IDeviceTopology);
const IID IID_IPart = __uuidof(IPart);

HRESULT GetHardwareDeviceTopology(
            IMMDevice *pEndptDev,
            IDeviceTopology **ppDevTopo)
{
    HRESULT hr = S_OK;
    IDeviceTopology *pDevTopoEndpt = NULL;
    IConnector *pConnEndpt = NULL;
    IConnector *pConnHWDev = NULL;
    IPart *pPartConn = NULL;

    // Get the endpoint device's IDeviceTopology interface.

    hr = pEndptDev->Activate(
                      IID_IDeviceTopology, CLSCTX_ALL,
                      NULL, (void**)&pDevTopoEndpt);
    EXIT_ON_ERROR(hr)

    // The device topology for an endpoint device always
    // contains just one connector (connector number 0).

    hr = pDevTopoEndpt->GetConnector(0, &pConnEndpt);
    EXIT_ON_ERROR(hr)

    // Use the connector in the endpoint device to get the
    // connector in the adapter device.

    hr = pConnEndpt->GetConnectedTo(&pConnHWDev);
    EXIT_ON_ERROR(hr)

    // Query the connector in the adapter device for
    // its IPart interface.

    hr = pConnHWDev->QueryInterface(
                         IID_IPart, (void**)&pPartConn);
    EXIT_ON_ERROR(hr)

    // Use the connector's IPart interface to get the
    // IDeviceTopology interface for the adapter device.

    hr = pPartConn->GetTopologyObject(ppDevTopo);

Exit:
    SAFE_RELEASE(pDevTopoEndpt)
    SAFE_RELEASE(pConnEndpt)
    SAFE_RELEASE(pConnHWDev)
    SAFE_RELEASE(pPartConn)

    return hr;
}
```



上述程式碼範例中的 GetHardwareDeviceTopology 函式會執行下列步驟，以取得輸入多工器裝置的 **IDeviceTopology** 介面：

1.  呼叫 **IMMDevice：： Activate** 方法以取得端點裝置的 **IDeviceTopology** 介面。
2.  使用上一個步驟取得的 **IDeviceTopology** 介面，呼叫 [**IDeviceTopology：： GetConnector**](/windows/desktop/api/Devicetopology/nf-devicetopology-idevicetopology-getconnector) 方法，以取得端點裝置中單一連接器 (連接器編號 0) 的 **IConnector** 介面。
3.  使用上一個步驟取得的 **IConnector** 介面，呼叫 [**IConnector：： GetConnectedTo**](/windows/desktop/api/Devicetopology/nf-devicetopology-iconnector-getconnectedto) 方法，以取得輸入多工器裝置中連接器的 **IConnector** 介面。
4.  查詢在上一個步驟中取得的 **IConnector** 介面，以取得其 **IPart** 介面。
5.  使用上一個步驟中取得的 **IPart** 介面，呼叫 [**IPart：： GetTopologyObject**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-gettopologyobject) 方法以取得輸入多工器裝置的 **IDeviceTopology** 介面。

在使用者可以從上圖中的麥克風錄製之前，用戶端應用程式必須確定多工器選取麥克風輸入。 下列程式碼範例會示範用戶端如何從麥克風中找出資料路徑，直到找到多工器為止，然後程式會選取麥克風輸入：


```C++
//-----------------------------------------------------------
// The input argument to this function is a pointer to the
// IMMDevice interface for a capture endpoint device. The
// function traverses the data path that extends from the
// endpoint device to the system bus (for example, PCI)
// or external bus (USB). If the function discovers a MUX
// (input selector) in the path, it selects the MUX input
// that connects to the stream from the endpoint device.
//-----------------------------------------------------------
#define EXIT_ON_ERROR(hres)  \
              if (FAILED(hres)) { goto Exit; }
#define SAFE_RELEASE(punk)  \
              if ((punk) != NULL)  \
                { (punk)->Release(); (punk) = NULL; }

const IID IID_IDeviceTopology = __uuidof(IDeviceTopology);
const IID IID_IPart = __uuidof(IPart);
const IID IID_IConnector = __uuidof(IConnector);
const IID IID_IAudioInputSelector = __uuidof(IAudioInputSelector);

HRESULT SelectCaptureDevice(IMMDevice *pEndptDev)
{
    HRESULT hr = S_OK;
    DataFlow flow;
    IDeviceTopology *pDeviceTopology = NULL;
    IConnector *pConnFrom = NULL;
    IConnector *pConnTo = NULL;
    IPart *pPartPrev = NULL;
    IPart *pPartNext = NULL;
    IAudioInputSelector *pSelector = NULL;

    if (pEndptDev == NULL)
    {
        EXIT_ON_ERROR(hr = E_POINTER)
    }

    // Get the endpoint device's IDeviceTopology interface.
    hr = pEndptDev->Activate(
                      IID_IDeviceTopology, CLSCTX_ALL, NULL,
                      (void**)&pDeviceTopology);
    EXIT_ON_ERROR(hr)

    // The device topology for an endpoint device always
    // contains just one connector (connector number 0).
    hr = pDeviceTopology->GetConnector(0, &pConnFrom);
    SAFE_RELEASE(pDeviceTopology)
    EXIT_ON_ERROR(hr)

    // Make sure that this is a capture device.
    hr = pConnFrom->GetDataFlow(&flow);
    EXIT_ON_ERROR(hr)

    if (flow != Out)
    {
        // Error -- this is a rendering device.
        EXIT_ON_ERROR(hr = AUDCLNT_E_WRONG_ENDPOINT_TYPE)
    }

    // Outer loop: Each iteration traverses the data path
    // through a device topology starting at the input
    // connector and ending at the output connector.
    while (TRUE)
    {
        BOOL bConnected;
        hr = pConnFrom->IsConnected(&bConnected);
        EXIT_ON_ERROR(hr)

        // Does this connector connect to another device?
        if (bConnected == FALSE)
        {
            // This is the end of the data path that
            // stretches from the endpoint device to the
            // system bus or external bus. Verify that
            // the connection type is Software_IO.
            ConnectorType  connType;
            hr = pConnFrom->GetType(&connType);
            EXIT_ON_ERROR(hr)

            if (connType == Software_IO)
            {
                break;  // finished
            }
            EXIT_ON_ERROR(hr = E_FAIL)
        }

        // Get the connector in the next device topology,
        // which lies on the other side of the connection.
        hr = pConnFrom->GetConnectedTo(&pConnTo);
        EXIT_ON_ERROR(hr)
        SAFE_RELEASE(pConnFrom)

        // Get the connector's IPart interface.
        hr = pConnTo->QueryInterface(
                        IID_IPart, (void**)&pPartPrev);
        EXIT_ON_ERROR(hr)
        SAFE_RELEASE(pConnTo)

        // Inner loop: Each iteration traverses one link in a
        // device topology and looks for input multiplexers.
        while (TRUE)
        {
            PartType parttype;
            UINT localId;
            IPartsList *pParts;

            // Follow downstream link to next part.
            hr = pPartPrev->EnumPartsOutgoing(&pParts);
            EXIT_ON_ERROR(hr)

            hr = pParts->GetPart(0, &pPartNext);
            pParts->Release();
            EXIT_ON_ERROR(hr)

            hr = pPartNext->GetPartType(&parttype);
            EXIT_ON_ERROR(hr)

            if (parttype == Connector)
            {
                // We've reached the output connector that
                // lies at the end of this device topology.
                hr = pPartNext->QueryInterface(
                                  IID_IConnector,
                                  (void**)&pConnFrom);
                EXIT_ON_ERROR(hr)

                SAFE_RELEASE(pPartPrev)
                SAFE_RELEASE(pPartNext)
                break;
            }

            // Failure of the following call means only that
            // the part is not a MUX (input selector).
            hr = pPartNext->Activate(
                              CLSCTX_ALL,
                              IID_IAudioInputSelector,
                              (void**)&pSelector);
            if (hr == S_OK)
            {
                // We found a MUX (input selector), so select
                // the input from our endpoint device.
                hr = pPartPrev->GetLocalId(&localId);
                EXIT_ON_ERROR(hr)

                hr = pSelector->SetSelection(localId, NULL);
                EXIT_ON_ERROR(hr)

                SAFE_RELEASE(pSelector)
            }

            SAFE_RELEASE(pPartPrev)
            pPartPrev = pPartNext;
            pPartNext = NULL;
        }
    }

Exit:
    SAFE_RELEASE(pConnFrom)
    SAFE_RELEASE(pConnTo)
    SAFE_RELEASE(pPartPrev)
    SAFE_RELEASE(pPartNext)
    SAFE_RELEASE(pSelector)
    return hr;
}
```



DeviceTopology API 會實 [**IAudioInputSelector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioinputselector) 介面來封裝多工器，例如上圖中的多工器。  ([**IAudioOutputSelector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiooutputselector) 介面會封裝一個信號。 ) 在上述程式碼範例中，SelectCaptureDevice 函式的內部迴圈會查詢它找到的每個子單位，以探索子單位是否為多工器。 如果子單位為多工器，則函式會呼叫 [**IAudioInputSelector：： SetSelection**](/windows/desktop/api/Devicetopology/nf-devicetopology-iaudioinputselector-setselection) 方法，以選取從端點裝置連接到資料流程的輸入。

在上述程式碼範例中，外部迴圈的每個反復專案都會流經一個裝置拓撲。 當您在上圖中遍歷裝置拓撲時，第一次反覆運算會流經輸入多工器裝置，而第二個反復專案則會流經 wave capture 裝置。 函式會在到達圖表右邊緣的接點時終止。 當函數偵測到具有軟體 IO 連線類型的連接器時，就會發生終止 \_ 。 此連線類型會識別介面卡裝置連接到系統匯流排的點。

在上述程式碼範例中，呼叫 [**IPart：： GetPartType**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getparttype) 方法會取得 **IPartType** 列舉值，這個值表示目前的元件是連接器或音訊處理子單位。

上述程式碼範例中的內部迴圈會透過呼叫 [**IPart：： EnumPartsOutgoing**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-enumpartsoutgoing) 方法，從某個部分到下一個部分的連結逐步執行。  (也會有 [**IPart：： EnumPartsIncoming**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-enumpartsincoming) 方法，以相反的方向逐步執行。 ) 這個方法會抓取 [**IPartsList**](/windows/desktop/api/Devicetopology/nn-devicetopology-ipartslist) 物件，其中包含所有傳出部分的清單。 不過，SelectCaptureDevice 函式預期在捕獲裝置中遇到的任何部分，一律會有一個外寄部分。 因此，後續對 [**IPartsList：： GetPart**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipartslist-getpart) 的呼叫一律會要求清單中的第一個部分（元件編號0），因為此函式會假設這是清單中的唯一部分。

如果 SelectCaptureDevice 函式遇到該假設不正確拓撲，此函式可能無法正確設定裝置。 若要避免這類失敗，更一般用途的函式版本可能會執行下列動作：

-   呼叫 [**IPartsList：： GetCount**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipartslist-getcount) 方法，以判斷外寄部分的數目。
-   針對每個外寄部分，呼叫 **IPartsList：： GetPart** 來開始遍歷元件的資料路徑。

部分（但不一定全部）部分都有用戶端可以設定或取得的相關硬體控制項。 特定元件可能會有零個、一個或多個硬體控制項。 硬體控制項是由下列成對的介面所代表：

-   泛型控制項介面 [**IControlInterface**](/windows/desktop/api/Devicetopology/nn-devicetopology-icontrolinterface)，其具有所有硬體控制項通用的方法。
-    (的函式特定介面，例如，會公開特定硬體控制項類型之控制項參數的 [**IAudioVolumeLevel**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiovolumelevel))  (例如，磁片區控制項) 。

為了列舉元件的硬體控制項，用戶端會先呼叫 [**IPart：： GetControlInterfaceCount**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getcontrolinterfacecount) 方法，以判斷與元件相關聯的硬體控制項數目。 接下來，用戶端會對 [**IPart：： GetControlInterface**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getcontrolinterface) 方法進行一連串的呼叫，以取得每個硬體控制項的 **IControlInterface** 介面。 最後，用戶端會呼叫 [**IControlInterface：： GetIID**](/windows/desktop/api/Devicetopology/nf-devicetopology-icontrolinterface-getiid) 方法取得介面識別碼，以取得每個硬體控制項的函式特定介面。 用戶端會使用這個識別碼呼叫 [**IPart：： Activate**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-activate) 方法來取得函式特定的介面。

屬於連接器的元件可能會支援下列其中一個函式特定的控制項介面：

-   [**IKsFormatSupport**](/windows/desktop/api/Devicetopology/nn-devicetopology-iksformatsupport)
-   [**IKsJackDescription**](/windows/desktop/api/Devicetopology/nn-devicetopology-iksjackdescription)

屬於子單位的部分可能會支援下列一或多個特定的函式控制項介面：

-   [**IAudioAutoGainControl**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioautogaincontrol)
-   [**IAudioBass**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiobass)
-   [**IAudioChannelConfig**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiochannelconfig)
-   [**IAudioInputSelector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioinputselector)
-   [**IAudioLoudness**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioloudness)
-   [**IAudioMidrange**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiomidrange)
-   [**IAudioMute**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiomute)
-   [**IAudioOutputSelector**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiooutputselector)
-   [**IAudioPeakMeter**](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiopeakmeter)
-   [**IAudioTreble**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiotreble)
-   [**IAudioVolumeLevel**](/windows/win32/api/devicetopology/nn-devicetopology-iaudiovolumelevel)
-   [**IDeviceSpecificProperty**](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicespecificproperty)

只有當基礎硬體控制項有裝置特定的控制值，且控制項無法由上述清單中的任何其他函式特定介面明確表示時，元件才支援 **IDeviceSpecificProperty** 介面。 通常，裝置專屬屬性只適用于可從元件類型、元件子類型和部分名稱等資訊推斷屬性值意義的用戶端。 用戶端可以藉由呼叫 [**IPart：： GetPartType**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getparttype)、 [**IPart：： GetSubType**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getsubtype)和 [**IPart：： GetName**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getname) 方法來取得此資訊。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[程式設計指南](programming-guide.md)
</dt> </dl>

 

 
