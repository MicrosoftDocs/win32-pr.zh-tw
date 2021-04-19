---
title: 執行自訂音訊端點列舉值
description: 從 Windows Server 2008 R2 開始，您可以在遠端桌面通訊協定提供者中執行自訂的遠端音訊端點枚舉器。
ms.assetid: 684bd62e-1e28-4330-a3c5-6bce684d652d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 435ab2a572169f20a7f8f9db194449be5361e409
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/08/2020
ms.locfileid: "106969544"
---
# <a name="implementing-a-custom-audio-endpoint-enumerator"></a><span data-ttu-id="575aa-103">執行自訂音訊端點列舉值</span><span class="sxs-lookup"><span data-stu-id="575aa-103">Implementing a Custom Audio Endpoint Enumerator</span></span>

<span data-ttu-id="575aa-104">從 Windows Server 2008 R2 開始，您可以在遠端桌面通訊協定提供者中執行自訂的遠端音訊端點枚舉器。</span><span class="sxs-lookup"><span data-stu-id="575aa-104">Beginning with Windows Server 2008 R2, you can implement a custom remote audio endpoint enumerator as part of a Remote Desktop protocol provider.</span></span> <span data-ttu-id="575aa-105">遠端桌面通訊協定提供者可以使用自訂音訊端點列舉值，來抓取具有一組特定功能的音訊端點集合。</span><span class="sxs-lookup"><span data-stu-id="575aa-105">A Remote Desktop protocol provider can use a custom audio endpoint enumerator to retrieve a collection of audio endpoints that have a specific set of capabilities.</span></span>

<span data-ttu-id="575aa-106">**若要執行自訂遠端音訊端點列舉值**</span><span class="sxs-lookup"><span data-stu-id="575aa-106">**To implement a custom remote audio endpoint enumerator**</span></span>

1.  <span data-ttu-id="575aa-107">您的自訂端點列舉值解決方案應採用四種主要類型的物件：裝置列舉值物件、裝置集合物件、裝置物件和屬性存放區物件。</span><span class="sxs-lookup"><span data-stu-id="575aa-107">Your custom endpoint enumerator solution should implement four main types of objects: device enumerator objects, device collection objects, device objects, and property store objects.</span></span>

    

    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="575aa-108">物件型別</span><span class="sxs-lookup"><span data-stu-id="575aa-108">Object type</span></span></th>
    <th><span data-ttu-id="575aa-109">說明</span><span class="sxs-lookup"><span data-stu-id="575aa-109">Description</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="575aa-110">裝置列舉值物件</span><span class="sxs-lookup"><span data-stu-id="575aa-110">Device enumerator object</span></span><br/></td>
    <td><span data-ttu-id="575aa-111">裝置列舉值物件提供端點列舉值功能。</span><span class="sxs-lookup"><span data-stu-id="575aa-111">A device enumerator object provides the endpoint enumerator functionality.</span></span> <span data-ttu-id="575aa-112">它會公開傳回預設端點和指定端點集合的方法。</span><span class="sxs-lookup"><span data-stu-id="575aa-112">It exposes methods that return a default endpoint and specified collections of endpoints.</span></span> <span data-ttu-id="575aa-113">例如，根據指定的準則，列舉值可以傳回通訊端點、播放端點或捕捉端點。</span><span class="sxs-lookup"><span data-stu-id="575aa-113">For example, depending on the criteria specified, the enumerator can return communication endpoints, playback endpoints, or capture endpoints.</span></span> <span data-ttu-id="575aa-114">裝置列舉值物件必須執行 <a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator"><strong>IMMDeviceEnumerator</strong></a> 介面。</span><span class="sxs-lookup"><span data-stu-id="575aa-114">The device enumerator object must implement the <a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator"><strong>IMMDeviceEnumerator</strong></a> interface.</span></span><br/></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="575aa-115">裝置集合物件</span><span class="sxs-lookup"><span data-stu-id="575aa-115">Device collection object</span></span><br/></td>
    <td><span data-ttu-id="575aa-116">裝置集合物件代表音訊裝置的集合。</span><span class="sxs-lookup"><span data-stu-id="575aa-116">A device collection object represents a collection of audio devices.</span></span> <span data-ttu-id="575aa-117">它必須執行 <a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdevicecollection"><strong>IMMDeviceCollection</strong></a> 介面。</span><span class="sxs-lookup"><span data-stu-id="575aa-117">It must implement the <a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdevicecollection"><strong>IMMDeviceCollection</strong></a> interface.</span></span><br/></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="575aa-118">裝置物件</span><span class="sxs-lookup"><span data-stu-id="575aa-118">Device object</span></span><br/></td>
    <td><span data-ttu-id="575aa-119">裝置物件代表特定音訊裝置。</span><span class="sxs-lookup"><span data-stu-id="575aa-119">A device object represents a particular audio device.</span></span> <span data-ttu-id="575aa-120">它可讓您存取音訊裝置的屬性存放區，並公開裝置上可用的音訊播放和捕捉介面。</span><span class="sxs-lookup"><span data-stu-id="575aa-120">It provides access to the audio device's property store and exposes the audio playback and capture interfaces available on the device.</span></span> <span data-ttu-id="575aa-121">裝置物件必須執行 <a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdevice"><strong>IMMDevice</strong></a> 和 <a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immendpoint"><strong>IMMEndpoint</strong></a> 介面。</span><span class="sxs-lookup"><span data-stu-id="575aa-121">The device object must implement the <a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdevice"><strong>IMMDevice</strong></a> and <a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immendpoint"><strong>IMMEndpoint</strong></a> interfaces.</span></span><br/></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="575aa-122">屬性存放區物件</span><span class="sxs-lookup"><span data-stu-id="575aa-122">Property store object</span></span><br/></td>
    <td><span data-ttu-id="575aa-123">屬性存放區物件會公開與音訊裝置相關聯的屬性。</span><span class="sxs-lookup"><span data-stu-id="575aa-123">A property store object exposes the properties associated with an audio device.</span></span> <span data-ttu-id="575aa-124">系統會使用其中一些屬性，但應用程式也可以使用音訊端點儲存任意屬性。</span><span class="sxs-lookup"><span data-stu-id="575aa-124">Some of these properties are used by the system, but applications can store arbitrary properties with the audio endpoint as well.</span></span><br/> <span data-ttu-id="575aa-125">所有音訊裝置都有下列三個屬性：</span><span class="sxs-lookup"><span data-stu-id="575aa-125">All audio devices have the following three properties:</span></span><br/>
    <ul>
    <li><span data-ttu-id="575aa-126"><a href="/windows/desktop/CoreAudio/pkey-deviceinterface-friendlyname"><strong>PKEY_DeviceInterface_FriendlyName</strong></a></span><span class="sxs-lookup"><span data-stu-id="575aa-126"><a href="/windows/desktop/CoreAudio/pkey-deviceinterface-friendlyname"><strong>PKEY_DeviceInterface_FriendlyName</strong></a></span></span></li>
    <li><span data-ttu-id="575aa-127"><a href="/windows/desktop/CoreAudio/pkey-device-devicedesc"><strong>PKEY_Device_DeviceDesc</strong></a></span><span class="sxs-lookup"><span data-stu-id="575aa-127"><a href="/windows/desktop/CoreAudio/pkey-device-devicedesc"><strong>PKEY_Device_DeviceDesc</strong></a></span></span></li>
    <li><span data-ttu-id="575aa-128"><a href="/windows/desktop/CoreAudio/pkey-device-friendlyname"><strong>PKEY_Device_FriendlyName</strong></a></span><span class="sxs-lookup"><span data-stu-id="575aa-128"><a href="/windows/desktop/CoreAudio/pkey-device-friendlyname"><strong>PKEY_Device_FriendlyName</strong></a></span></span></li>
    </ul>
<span data-ttu-id="575aa-129">屬性存放區物件必須執行 <a href="/windows/win32/api/propsys/nn-propsys-ipropertystore">IPropertyStore</a> 介面。</span><span class="sxs-lookup"><span data-stu-id="575aa-129">The property store object must implement the <a href="/windows/win32/api/propsys/nn-propsys-ipropertystore">IPropertyStore</a> interface.</span></span><br/></td>
    </tr>
    </tbody>
    </table>

    

     

2.  <span data-ttu-id="575aa-130">自訂端點列舉值必須在可以載入音訊系統和其他應用程式的 DLL 中實作為。</span><span class="sxs-lookup"><span data-stu-id="575aa-130">The custom endpoint enumerator must be implemented in a DLL that can be loaded into the audio system and other applications.</span></span> <span data-ttu-id="575aa-131">DLL 必須經過簽署，才能讓安全的進程載入它。</span><span class="sxs-lookup"><span data-stu-id="575aa-131">The DLL must be signed so that secure processes can load it.</span></span> <span data-ttu-id="575aa-132">DLL 必須執行並匯出 [**GetTSAudioEndpointEnumeratorForSession**](gettsaudioendpointenumeratorforsession.md) 函式，作為自訂端點列舉值的進入點。</span><span class="sxs-lookup"><span data-stu-id="575aa-132">The DLL must implement and export the [**GetTSAudioEndpointEnumeratorForSession**](gettsaudioendpointenumeratorforsession.md) function, which acts as an entry point to the custom endpoint enumerator.</span></span>

<span data-ttu-id="575aa-133">遠端桌面服務服務會呼叫 [**QueryProperty**](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-queryproperty) 方法，並將 *QueryType* 參數設定為 **WTS \_ QUERY \_ AUDIOENUM \_ DLL** ，以取得列舉值物件的名稱。</span><span class="sxs-lookup"><span data-stu-id="575aa-133">The Remote Desktop Services service calls the [**QueryProperty**](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-queryproperty) method and sets the *QueryType* parameter to **WTS\_QUERY\_AUDIOENUM\_DLL** to retrieve the name of the enumerator object.</span></span>

<span data-ttu-id="575aa-134">自訂列舉值物件使用類似 COM 的介面和類似 COM 的參考計數機制，但它們不是真正的 COM 物件。</span><span class="sxs-lookup"><span data-stu-id="575aa-134">Custom enumerator objects use COM-like interfaces and a COM-like reference counting mechanism, but they are not true COM objects.</span></span> <span data-ttu-id="575aa-135">自訂端點列舉值必須能夠使用不支援 COM 之應用程式所使用的舊版音訊介面。</span><span class="sxs-lookup"><span data-stu-id="575aa-135">The custom endpoint enumerator must have the ability to work with legacy audio interfaces used by applications that do not support COM.</span></span> <span data-ttu-id="575aa-136">基於這個理由，自訂端點列舉值不能依賴 COM 的生命週期管理機制。</span><span class="sxs-lookup"><span data-stu-id="575aa-136">For this reason, the custom endpoint enumerator must not rely on COM's life cycle management mechanism.</span></span> <span data-ttu-id="575aa-137">音訊端點列舉值的取用者（例如 MMDevAPI.dll）會在使用者應用程式需要時載入自訂端點列舉值 DLL，而且當列舉值持有裝置列舉值物件、裝置集合物件、裝置物件或屬性存放區物件的參考時，就不會卸載列舉值。</span><span class="sxs-lookup"><span data-stu-id="575aa-137">Consumers of your audio endpoint enumerator, such as MMDevAPI.dll, load the custom endpoint enumerator DLL when required by user applications, and they will not unload the enumerator while the enumerator holds a reference to a device enumerator object, device collection object, device object, or property store object.</span></span> <span data-ttu-id="575aa-138">但是，這些取用者不可能追蹤自訂端點列舉值所擁有之其他類型物件的參考。</span><span class="sxs-lookup"><span data-stu-id="575aa-138">It is not possible, however, for these consumers to track references to other types of objects owned by the custom endpoint enumerator.</span></span> <span data-ttu-id="575aa-139">因此，我們建議您的自訂端點列舉值不會建立任何可能存留時間這四種物件類型的物件。</span><span class="sxs-lookup"><span data-stu-id="575aa-139">Accordingly, we recommend that your custom endpoint enumerator not create any objects that could outlive these four types of objects.</span></span>

## <a name="to-implement-a-custom-audio-endpoint"></a><span data-ttu-id="575aa-140">若要執行自訂音訊端點</span><span class="sxs-lookup"><span data-stu-id="575aa-140">To implement a custom audio endpoint</span></span>

<span data-ttu-id="575aa-141">若要執行自訂音訊裝置列舉值，您必須執行自訂音訊端點。</span><span class="sxs-lookup"><span data-stu-id="575aa-141">To implement a custom audio device enumerator, you must implement a custom audio endpoint.</span></span> <span data-ttu-id="575aa-142">自訂音訊裝置的連結方式是使用下列兩個語句：</span><span class="sxs-lookup"><span data-stu-id="575aa-142">The way that your custom audio devices are linked is by using the following two statements:</span></span>

-   `IMMDevice::Activate(IAudioOutputEndpointRT)`
-   `IMMDevice::Activate(IAudioInputEndpointRT)`

<span data-ttu-id="575aa-143">我們不希望您在自訂音訊裝置列舉值中執行 [**IMMDevice：： Activate**](/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-immdevice-activate) 介面的完整清單。</span><span class="sxs-lookup"><span data-stu-id="575aa-143">We do not expect you to implement the full list of [**IMMDevice::Activate**](/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-immdevice-activate) interfaces in your custom audio device enumerator.</span></span> <span data-ttu-id="575aa-144">相反地，您應該執行 [**IAudioOutputEndpointRT**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudiooutputendpointrt) 和 [**IAudioInputEndpointRT**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioinputendpointrt)。</span><span class="sxs-lookup"><span data-stu-id="575aa-144">Instead, you should implement [**IAudioOutputEndpointRT**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudiooutputendpointrt) and [**IAudioInputEndpointRT**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioinputendpointrt).</span></span> <span data-ttu-id="575aa-145">您可以選擇性地執行一些其他工作，例如 [**IAudioEndpointVolume**](/windows/desktop/api/endpointvolume/nn-endpointvolume-iaudioendpointvolume)。</span><span class="sxs-lookup"><span data-stu-id="575aa-145">You can optionally implement a few more, such as [**IAudioEndpointVolume**](/windows/desktop/api/endpointvolume/nn-endpointvolume-iaudioendpointvolume).</span></span> <span data-ttu-id="575aa-146">針對您未執行的任何介面，您應該傳回 **E \_ NOINTERFACE** (您必須使用這個特定的失敗代碼) 。</span><span class="sxs-lookup"><span data-stu-id="575aa-146">For any interface you do not implement, you should return **E\_NOINTERFACE** (you must use this specific failure code).</span></span> <span data-ttu-id="575aa-147">然後，Windows 會切換回介面的庫存實 (例如 [**IAudioClient2**](/windows/desktop/api/audioclient/nn-audioclient-iaudioclient2)) 。</span><span class="sxs-lookup"><span data-stu-id="575aa-147">Windows will then fall back to a stock implementation of the interface (for example, [**IAudioClient2**](/windows/desktop/api/audioclient/nn-audioclient-iaudioclient2)).</span></span>

<span data-ttu-id="575aa-148">如需如何執行和註冊音訊端點的其他參考檔，請參閱 [**IAudioInputEndpointRT**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioinputendpointrt)。</span><span class="sxs-lookup"><span data-stu-id="575aa-148">For additional reference documentation about how to implement and register audio endpoints, see [**IAudioInputEndpointRT**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioinputendpointrt).</span></span> <span data-ttu-id="575aa-149">如需顯示 WASAPI 運作方式的圖表，請參閱 [使用者模式音訊元件](/windows/desktop/CoreAudio/user-mode-audio-components)。</span><span class="sxs-lookup"><span data-stu-id="575aa-149">For a diagram that shows how WASAPI works, see [User-Mode Audio Components](/windows/desktop/CoreAudio/user-mode-audio-components).</span></span> <span data-ttu-id="575aa-150">請注意，從 Windows Server 2008 開始，所有使用者模式音訊都是新的。</span><span class="sxs-lookup"><span data-stu-id="575aa-150">Note that all of user-mode audio is new beginning with Windows Server 2008.</span></span>

## <a name="related-topics"></a><span data-ttu-id="575aa-151">相關主題</span><span class="sxs-lookup"><span data-stu-id="575aa-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="575aa-152">建立遠端桌面通訊協定提供者</span><span class="sxs-lookup"><span data-stu-id="575aa-152">Creating a Remote Desktop Protocol Provider</span></span>](creating-a-custom-remote-protocol.md)
</dt> <dt>

[<span data-ttu-id="575aa-153">**GetTSAudioEndpointEnumeratorForSession**</span><span class="sxs-lookup"><span data-stu-id="575aa-153">**GetTSAudioEndpointEnumeratorForSession**</span></span>](gettsaudioendpointenumeratorforsession.md)
</dt> <dt>

[<span data-ttu-id="575aa-154">**IMMDevice**</span><span class="sxs-lookup"><span data-stu-id="575aa-154">**IMMDevice**</span></span>](/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdevice)
</dt> <dt>

[<span data-ttu-id="575aa-155">**IMMDeviceCollection**</span><span class="sxs-lookup"><span data-stu-id="575aa-155">**IMMDeviceCollection**</span></span>](/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdevicecollection)
</dt> <dt>

[<span data-ttu-id="575aa-156">**IMMDeviceEnumerator**</span><span class="sxs-lookup"><span data-stu-id="575aa-156">**IMMDeviceEnumerator**</span></span>](/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator)
</dt> <dt>

[<span data-ttu-id="575aa-157">**IMMEndpoint**</span><span class="sxs-lookup"><span data-stu-id="575aa-157">**IMMEndpoint**</span></span>](/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immendpoint)
</dt> <dt>

[<span data-ttu-id="575aa-158">IPropertyStore</span><span class="sxs-lookup"><span data-stu-id="575aa-158">IPropertyStore</span></span>](/windows/win32/api/propsys/nn-propsys-ipropertystore)
</dt> </dl>