---
description: 使用 IKsControl 介面存取音訊屬性
ms.assetid: 72bf9164-96c6-4543-b858-19480b032fdb
title: 使用 IKsControl 介面存取音訊屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a67639a0e51334da80b7bff88293414a58bb204c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104187773"
---
# <a name="using-the-ikscontrol-interface-to-access-audio-properties"></a><span data-ttu-id="7151b-103">使用 IKsControl 介面存取音訊屬性</span><span class="sxs-lookup"><span data-stu-id="7151b-103">Using the IKsControl Interface to Access Audio Properties</span></span>

<span data-ttu-id="7151b-104">在罕見的情況下，特殊的音訊應用程式可能需要使用 [**IKsControl**](/windows-hardware/drivers/ddi/ksproxy/nn-ksproxy-ikscontrol) 介面，來存取 [DeviceTopology API](devicetopology-api.md) 或 [MMDevice API](mmdevice-api.md)未公開之音訊介面卡的特定硬體功能。</span><span class="sxs-lookup"><span data-stu-id="7151b-104">In rare cases, a specialized audio application might need to use the [**IKsControl**](/windows-hardware/drivers/ddi/ksproxy/nn-ksproxy-ikscontrol) interface to access certain hardware capabilities of an audio adapter that are not exposed by the [DeviceTopology API](devicetopology-api.md) or the [MMDevice API](mmdevice-api.md).</span></span> <span data-ttu-id="7151b-105">**IKsControl** 介面會讓核心串流 (KS) 裝置的屬性、事件和方法可供使用者模式應用程式使用。</span><span class="sxs-lookup"><span data-stu-id="7151b-105">The **IKsControl** interface makes the properties, events, and methods of kernel-streaming (KS) devices available to user-mode applications.</span></span> <span data-ttu-id="7151b-106">音訊應用程式的主要興趣是 KS 屬性。</span><span class="sxs-lookup"><span data-stu-id="7151b-106">Of primary interest to audio applications are KS properties.</span></span> <span data-ttu-id="7151b-107">**IKsControl** 介面可搭配 DeviceTopology API 和 MMDevice API 使用，以存取音訊介面卡的 KS 屬性。</span><span class="sxs-lookup"><span data-stu-id="7151b-107">The **IKsControl** interface can be used in conjunction with the DeviceTopology API and the MMDevice API to access the KS properties of audio adapters.</span></span>

<span data-ttu-id="7151b-108">[**IKsControl**](/windows-hardware/drivers/ddi/ksproxy/nn-ksproxy-ikscontrol)介面主要是供撰寫控制台應用程式來管理其音訊硬體的硬體供應商使用。</span><span class="sxs-lookup"><span data-stu-id="7151b-108">The [**IKsControl**](/windows-hardware/drivers/ddi/ksproxy/nn-ksproxy-ikscontrol) interface is intended primarily for use by hardware vendors who write control-panel applications to manage their audio hardware.</span></span> <span data-ttu-id="7151b-109">針對未系結至特定硬體裝置的一般用途音訊應用程式， **IKsControl** 較不實用。</span><span class="sxs-lookup"><span data-stu-id="7151b-109">**IKsControl** is less useful for general-purpose audio applications that are not tied to particular hardware devices.</span></span> <span data-ttu-id="7151b-110">原因是硬體廠商經常採用專屬機制來存取裝置的音訊內容。</span><span class="sxs-lookup"><span data-stu-id="7151b-110">The reason is that hardware vendors frequently implement proprietary mechanisms to access the audio properties of their devices.</span></span> <span data-ttu-id="7151b-111">相較于 DeviceTopology API，它會隱藏硬體特定的驅動程式，並提供相當一致的介面來存取音訊屬性，而應用程式會使用 **IKsControl** 直接與驅動程式通訊。</span><span class="sxs-lookup"><span data-stu-id="7151b-111">In contrast to the DeviceTopology API, which hides hardware-specific driver quirks and provides a relatively uniform interface for accessing audio properties, applications use **IKsControl** to communicate directly with drivers.</span></span> <span data-ttu-id="7151b-112">如需 **IKsControl** 的詳細資訊，請參閱 Windows DDK 檔。</span><span class="sxs-lookup"><span data-stu-id="7151b-112">For more information about **IKsControl**, see the Windows DDK documentation.</span></span>

<span data-ttu-id="7151b-113">如同在 [裝置拓撲](device-topologies.md)中所討論的，介面卡裝置拓撲中的子單位可能會支援下表左邊資料行中所顯示的一或多個函式特定的控制介面。</span><span class="sxs-lookup"><span data-stu-id="7151b-113">As discussed in [Device Topologies](device-topologies.md), a subunit in the topology of an adapter device might support one or more of the function-specific control interfaces shown in the left column of the following table.</span></span> <span data-ttu-id="7151b-114">資料表右邊資料行中的每個專案都是對應至左側控制項介面的 KS 屬性。</span><span class="sxs-lookup"><span data-stu-id="7151b-114">Each entry in the right column of the table is the KS property that corresponds to the control interface on the left.</span></span> <span data-ttu-id="7151b-115">控制項介面可方便您存取屬性。</span><span class="sxs-lookup"><span data-stu-id="7151b-115">The control interface provides convenient access to the property.</span></span> <span data-ttu-id="7151b-116">大部分的音訊驅動程式都會使用 KS 屬性來代表次單元連接的函式特定處理功能 (也稱為「KS 節點」（) 在其音訊介面卡的拓撲中）。</span><span class="sxs-lookup"><span data-stu-id="7151b-116">Most audio drivers use KS properties to represent the function-specific processing capabilities of the subunits (also referred to as KS nodes) in the topologies of their audio adapters.</span></span> <span data-ttu-id="7151b-117">如需有關 KS 屬性和 KS 節點的詳細資訊，請參閱 Windows DDK 檔。</span><span class="sxs-lookup"><span data-stu-id="7151b-117">For more information about KS properties and KS nodes, see the Windows DDK documentation.</span></span>



| <span data-ttu-id="7151b-118">控制項介面</span><span class="sxs-lookup"><span data-stu-id="7151b-118">Control interface</span></span>                                          | <span data-ttu-id="7151b-119">KS 屬性</span><span class="sxs-lookup"><span data-stu-id="7151b-119">KS property</span></span>                        |
|------------------------------------------------------------|------------------------------------|
| [<span data-ttu-id="7151b-120">**IAudioAutoGainControl**</span><span class="sxs-lookup"><span data-stu-id="7151b-120">**IAudioAutoGainControl**</span></span>](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioautogaincontrol)     | <span data-ttu-id="7151b-121">KSPROPERTY \_ 音訊 \_ AGC</span><span class="sxs-lookup"><span data-stu-id="7151b-121">KSPROPERTY\_AUDIO\_AGC</span></span>             |
| [<span data-ttu-id="7151b-122">**IAudioBass**</span><span class="sxs-lookup"><span data-stu-id="7151b-122">**IAudioBass**</span></span>](/windows/win32/api/devicetopology/nn-devicetopology-iaudiobass)                           | <span data-ttu-id="7151b-123">KSPROPERTY \_ 音訊 \_ 低音</span><span class="sxs-lookup"><span data-stu-id="7151b-123">KSPROPERTY\_AUDIO\_BASS</span></span>            |
| [<span data-ttu-id="7151b-124">**IAudioChannelConfig**</span><span class="sxs-lookup"><span data-stu-id="7151b-124">**IAudioChannelConfig**</span></span>](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiochannelconfig)         | <span data-ttu-id="7151b-125">KSPROPERTY \_ 音訊 \_ 通道 \_ 設定</span><span class="sxs-lookup"><span data-stu-id="7151b-125">KSPROPERTY\_AUDIO\_CHANNEL\_CONFIG</span></span> |
| [<span data-ttu-id="7151b-126">**IAudioInputSelector**</span><span class="sxs-lookup"><span data-stu-id="7151b-126">**IAudioInputSelector**</span></span>](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioinputselector)         | <span data-ttu-id="7151b-127">KSPROPERTY \_ 音訊 \_ MUX \_ 來源</span><span class="sxs-lookup"><span data-stu-id="7151b-127">KSPROPERTY\_AUDIO\_MUX\_SOURCE</span></span>     |
| [<span data-ttu-id="7151b-128">**IAudioLoudness**</span><span class="sxs-lookup"><span data-stu-id="7151b-128">**IAudioLoudness**</span></span>](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudioloudness)                   | <span data-ttu-id="7151b-129">KSPROPERTY \_ 音訊 \_ 音量</span><span class="sxs-lookup"><span data-stu-id="7151b-129">KSPROPERTY\_AUDIO\_LOUDNESS</span></span>        |
| [<span data-ttu-id="7151b-130">**IAudioMidrange**</span><span class="sxs-lookup"><span data-stu-id="7151b-130">**IAudioMidrange**</span></span>](/windows/win32/api/devicetopology/nn-devicetopology-iaudiomidrange)                   | <span data-ttu-id="7151b-131">KSPROPERTY \_ 音訊 \_ 中間</span><span class="sxs-lookup"><span data-stu-id="7151b-131">KSPROPERTY\_AUDIO\_MID</span></span>             |
| [<span data-ttu-id="7151b-132">**IAudioMute**</span><span class="sxs-lookup"><span data-stu-id="7151b-132">**IAudioMute**</span></span>](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiomute)                           | <span data-ttu-id="7151b-133">KSPROPERTY \_ 音訊 \_ 靜音</span><span class="sxs-lookup"><span data-stu-id="7151b-133">KSPROPERTY\_AUDIO\_MUTE</span></span>            |
| [<span data-ttu-id="7151b-134">**IAudioOutputSelector**</span><span class="sxs-lookup"><span data-stu-id="7151b-134">**IAudioOutputSelector**</span></span>](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiooutputselector)       | <span data-ttu-id="7151b-135">KSPROPERTY \_ 音訊 \_ DEMUX \_ 目的地</span><span class="sxs-lookup"><span data-stu-id="7151b-135">KSPROPERTY\_AUDIO\_DEMUX\_DEST</span></span>     |
| [<span data-ttu-id="7151b-136">**IAudioPeakMeter**</span><span class="sxs-lookup"><span data-stu-id="7151b-136">**IAudioPeakMeter**</span></span>](/windows/desktop/api/Devicetopology/nn-devicetopology-iaudiopeakmeter)                 | <span data-ttu-id="7151b-137">KSPROPERTY \_ 音訊 \_ PEAKMETER</span><span class="sxs-lookup"><span data-stu-id="7151b-137">KSPROPERTY\_AUDIO\_PEAKMETER</span></span>       |
| [<span data-ttu-id="7151b-138">**IAudioTreble**</span><span class="sxs-lookup"><span data-stu-id="7151b-138">**IAudioTreble**</span></span>](/windows/win32/api/devicetopology/nn-devicetopology-iaudiotreble)                       | <span data-ttu-id="7151b-139">KSPROPERTY \_ 音訊 \_ 高音</span><span class="sxs-lookup"><span data-stu-id="7151b-139">KSPROPERTY\_AUDIO\_TREBLE</span></span>          |
| [<span data-ttu-id="7151b-140">**IAudioVolumeLevel**</span><span class="sxs-lookup"><span data-stu-id="7151b-140">**IAudioVolumeLevel**</span></span>](/windows/win32/api/devicetopology/nn-devicetopology-iaudiovolumelevel)             | <span data-ttu-id="7151b-141">KSPROPERTY \_ 音訊 \_ VOLUMELEVEL</span><span class="sxs-lookup"><span data-stu-id="7151b-141">KSPROPERTY\_AUDIO\_VOLUMELEVEL</span></span>     |
| [<span data-ttu-id="7151b-142">**IDeviceSpecificProperty**</span><span class="sxs-lookup"><span data-stu-id="7151b-142">**IDeviceSpecificProperty**</span></span>](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicespecificproperty) | <span data-ttu-id="7151b-143">KSPROPERTY \_ 音訊 \_ 開發 \_ 專用</span><span class="sxs-lookup"><span data-stu-id="7151b-143">KSPROPERTY\_AUDIO\_DEV\_SPECIFIC</span></span>   |



 

<span data-ttu-id="7151b-144">某些音訊介面卡的拓撲可能包含具有上表未列出之 KS 屬性的次單元連接。</span><span class="sxs-lookup"><span data-stu-id="7151b-144">The topologies of some audio adapters might contain subunits that have KS properties that are not listed in the preceding table.</span></span> <span data-ttu-id="7151b-145">例如，假設特定次級的 [**IPart：： GetSubType**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getsubtype) 方法呼叫會抓取 GUID 值 KSNODETYPE \_ 語氣。</span><span class="sxs-lookup"><span data-stu-id="7151b-145">For example, assume that a call to the [**IPart::GetSubType**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getsubtype) method for a particular subunit retrieves the GUID value KSNODETYPE\_TONE.</span></span> <span data-ttu-id="7151b-146">此子類型 GUID 表示子單位支援下列其中一個或多個 KS 屬性：</span><span class="sxs-lookup"><span data-stu-id="7151b-146">This subtype GUID indicates that the subunit supports one or more of the following KS properties:</span></span>

-   <span data-ttu-id="7151b-147">KSPROPERTY \_ 音訊 \_ 低音</span><span class="sxs-lookup"><span data-stu-id="7151b-147">KSPROPERTY\_AUDIO\_BASS</span></span>
-   <span data-ttu-id="7151b-148">KSPROPERTY \_ 音訊 \_ 中間</span><span class="sxs-lookup"><span data-stu-id="7151b-148">KSPROPERTY\_AUDIO\_MID</span></span>
-   <span data-ttu-id="7151b-149">KSPROPERTY \_ 音訊 \_ 高音</span><span class="sxs-lookup"><span data-stu-id="7151b-149">KSPROPERTY\_AUDIO\_TREBLE</span></span>
-   <span data-ttu-id="7151b-150">KSPROPERTY \_ 音訊 \_ 低音 \_ 提升</span><span class="sxs-lookup"><span data-stu-id="7151b-150">KSPROPERTY\_AUDIO\_BASS\_BOOST</span></span>

<span data-ttu-id="7151b-151">這份清單中的前三個屬性可透過上表所顯示的控制項介面存取，但 KSPROPERTY \_ 音訊 \_ 低音 \_ 提升屬性在 DeviceTopology API 中沒有對應的控制介面。</span><span class="sxs-lookup"><span data-stu-id="7151b-151">The first three properties in this list can be accessed through the control interfaces that appear in the preceding table, but the KSPROPERTY\_AUDIO\_BASS\_BOOST property has no corresponding control interface in the DeviceTopology API.</span></span> <span data-ttu-id="7151b-152">但是，如果子單位支援屬性，則應用程式可以使用 [**IKsControl**](/windows-hardware/drivers/ddi/ksproxy/nn-ksproxy-ikscontrol) 介面來存取這個屬性。</span><span class="sxs-lookup"><span data-stu-id="7151b-152">However, an application can use the [**IKsControl**](/windows-hardware/drivers/ddi/ksproxy/nn-ksproxy-ikscontrol) interface to access this property, if the subunit supports the property.</span></span>

<span data-ttu-id="7151b-153">您必須執行下列步驟，才能存取 \_ \_ 子類型 KSNODETYPE 語氣之子單位的 KSPROPERTY 音訊低音 \_ 增強屬性 \_ ：</span><span class="sxs-lookup"><span data-stu-id="7151b-153">The following steps are required to access the KSPROPERTY\_AUDIO\_BASS\_BOOST property of a subunit of subtype KSNODETYPE\_TONE:</span></span>

1.  <span data-ttu-id="7151b-154">呼叫 [**IConnector：： GetDeviceIdConnectedTo**](/windows/desktop/api/Devicetopology/nf-devicetopology-iconnector-getdeviceidconnectedto) 或 [**IDeviceTopology：： GetDeviceId**](/windows/desktop/api/Devicetopology/nf-devicetopology-idevicetopology-getdeviceid) 方法，以取得可識別介面卡裝置的裝置識別碼字串。</span><span class="sxs-lookup"><span data-stu-id="7151b-154">Call the [**IConnector::GetDeviceIdConnectedTo**](/windows/desktop/api/Devicetopology/nf-devicetopology-iconnector-getdeviceidconnectedto) or [**IDeviceTopology::GetDeviceId**](/windows/desktop/api/Devicetopology/nf-devicetopology-idevicetopology-getdeviceid) method to obtain the device ID string that identifies the adapter device.</span></span> <span data-ttu-id="7151b-155">此字串類似于 [端點識別碼字串](endpoint-id-strings.md)，不同之處在于它會識別介面卡裝置，而不是端點裝置。</span><span class="sxs-lookup"><span data-stu-id="7151b-155">This string is similar to an [endpoint ID string](endpoint-id-strings.md), except that it identifies an adapter device instead of an endpoint device.</span></span> <span data-ttu-id="7151b-156">如需介面卡裝置與端點裝置之間差異的詳細資訊，請參閱 [音訊端點裝置](audio-endpoint-devices.md)。</span><span class="sxs-lookup"><span data-stu-id="7151b-156">For more information about the difference between an adapter device and an endpoint device, see [Audio Endpoint Devices](audio-endpoint-devices.md).</span></span>
2.  <span data-ttu-id="7151b-157">以裝置識別碼字串呼叫 [**IMMDeviceEnumerator：： GetDevice**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice)方法，以取得介面卡裝置的 [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice)介面。</span><span class="sxs-lookup"><span data-stu-id="7151b-157">Obtain the [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) interface of the adapter device by calling the [**IMMDeviceEnumerator::GetDevice**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice) method with the device ID string.</span></span> <span data-ttu-id="7151b-158">這個 **IMMDevice** 介面與 **IMMDevice 介面** 中所述的介面相同，但它代表介面卡裝置，而不是端點裝置。</span><span class="sxs-lookup"><span data-stu-id="7151b-158">This **IMMDevice** interface is the same as the interface described in **IMMDevice Interface**, but it represents an adapter device instead of an endpoint device.</span></span>
3.  <span data-ttu-id="7151b-159">藉由呼叫 [**IMMDevice：： Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate)方法並將參數 *Iid* 設定為 **REFIID** iid IKsControl，以取得子單位上的 [**IKsControl**](/windows-hardware/drivers/ddi/ksproxy/nn-ksproxy-ikscontrol)介面 \_ 。</span><span class="sxs-lookup"><span data-stu-id="7151b-159">Obtain the [**IKsControl**](/windows-hardware/drivers/ddi/ksproxy/nn-ksproxy-ikscontrol) interface on the subunit by calling the [**IMMDevice::Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) method with parameter *iid* set to **REFIID** IID\_IKsControl.</span></span> <span data-ttu-id="7151b-160">請注意，此 **啟動** 方法所支援的介面（適用于介面卡裝置）不同于端點裝置的 **啟動** 方法所支援的介面。</span><span class="sxs-lookup"><span data-stu-id="7151b-160">Note that the interfaces supported by this **Activate** method, which is for an adapter device, are different from the interfaces supported by the **Activate** method for an endpoint device.</span></span> <span data-ttu-id="7151b-161">尤其是，介面卡裝置的 **啟動** 方法支援 **IKsControl**。</span><span class="sxs-lookup"><span data-stu-id="7151b-161">In particular, the **Activate** method for an adapter device supports **IKsControl**.</span></span>
4.  <span data-ttu-id="7151b-162">呼叫 [**IPart：： GetLocalId**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getlocalid) 方法，以取得子領域的本機識別碼。</span><span class="sxs-lookup"><span data-stu-id="7151b-162">Call the [**IPart::GetLocalId**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getlocalid) method to obtain the local ID of the subunit.</span></span>
5.  <span data-ttu-id="7151b-163">建立 KS 屬性要求。</span><span class="sxs-lookup"><span data-stu-id="7151b-163">Construct a KS property request.</span></span> <span data-ttu-id="7151b-164">要求所需的 KS 節點識別碼包含在上一個步驟中取得之本機識別碼的16個最少有效位。</span><span class="sxs-lookup"><span data-stu-id="7151b-164">The KS node ID required for the request is contained in the 16 least-significant bits of the local ID obtained in the previous step.</span></span>
6.  <span data-ttu-id="7151b-165">藉由呼叫 [**IKsControl：： KsProperty**](/windows-hardware/drivers/ddi/ksproxy/nf-ksproxy-ikscontrol-ksproperty) 方法，將 KS 屬性要求傳送到音訊驅動程式。</span><span class="sxs-lookup"><span data-stu-id="7151b-165">Send the KS property request to the audio driver by calling the [**IKsControl::KsProperty**](/windows-hardware/drivers/ddi/ksproxy/nf-ksproxy-ikscontrol-ksproperty) method.</span></span> <span data-ttu-id="7151b-166">如需此方法的詳細資訊，請參閱 Windows DDK 檔。</span><span class="sxs-lookup"><span data-stu-id="7151b-166">For more information about this method, see the Windows DDK documentation.</span></span>

<span data-ttu-id="7151b-167">下列程式碼範例會 \_ \_ \_ 從子類型 KSNODETYPE 語氣的子單位，抓取 KSPROPERTY 音訊低音增強屬性的值 \_ ：</span><span class="sxs-lookup"><span data-stu-id="7151b-167">The following code example retrieves the value of the KSPROPERTY\_AUDIO\_BASS\_BOOST property from a subunit of subtype KSNODETYPE\_TONE:</span></span>


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



<span data-ttu-id="7151b-168">在上述程式碼範例中，GetBassBoost 函數會採用下列三個參數：</span><span class="sxs-lookup"><span data-stu-id="7151b-168">In the preceding code example, the GetBassBoost function takes the following three parameters:</span></span>

-   <span data-ttu-id="7151b-169">`pEnumerator` 指向音訊端點列舉值的 [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) 介面。</span><span class="sxs-lookup"><span data-stu-id="7151b-169">`pEnumerator` points to the [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) interface of an audio endpoint enumerator.</span></span>
-   <span data-ttu-id="7151b-170">`pPart` 指向具有 KSNODETYPE 語氣子類型之子單位的 [**IPart**](/windows/desktop/api/Devicetopology/nn-devicetopology-ipart) 介面 \_ 。</span><span class="sxs-lookup"><span data-stu-id="7151b-170">`pPart` points to the [**IPart**](/windows/desktop/api/Devicetopology/nn-devicetopology-ipart) interface of a subunit that has a subtype of KSNODETYPE\_TONE.</span></span>
-   <span data-ttu-id="7151b-171">`pbValue` 指向 **BOOL** 變數，函式會將屬性值寫入其中。</span><span class="sxs-lookup"><span data-stu-id="7151b-171">`pbValue` points to a **BOOL** variable into which the function writes the property value.</span></span>

<span data-ttu-id="7151b-172">程式只會在呼叫 [**IPart：： GetSubType**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getsubtype) 之後呼叫 GetBassBoost，並判斷子單位的子類型為 KSNODETYPE \_ 語氣。</span><span class="sxs-lookup"><span data-stu-id="7151b-172">A program calls GetBassBoost only after it calls [**IPart::GetSubType**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-getsubtype) and determines that the subtype of the subunit is KSNODETYPE\_TONE.</span></span> <span data-ttu-id="7151b-173">如果啟用了低音提升，則屬性值為 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="7151b-173">The property value is **TRUE** if bass boost is enabled.</span></span> <span data-ttu-id="7151b-174">如果已停用低音提升，則為 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="7151b-174">It is **FALSE** if bass boost is disabled.</span></span>

<span data-ttu-id="7151b-175">在 GetBassBoost 函式的開頭， [**IPart：： GetTopologyObject**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-gettopologyobject) 方法的呼叫會取得包含 KSNODETYPE 語氣子單位的介面卡裝置 [**IDeviceTopology**](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicetopology) 介面 \_ 。</span><span class="sxs-lookup"><span data-stu-id="7151b-175">At the beginning of the GetBassBoost function, the call to the [**IPart::GetTopologyObject**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-gettopologyobject) method obtains the [**IDeviceTopology**](/windows/desktop/api/Devicetopology/nn-devicetopology-idevicetopology) interface of the adapter device that contains the KSNODETYPE\_TONE subunit.</span></span> <span data-ttu-id="7151b-176">[**IDeviceTopology：： GetDeviceId**](/windows/desktop/api/Devicetopology/nf-devicetopology-idevicetopology-getdeviceid)方法呼叫會捕獲識別介面卡裝置的裝置識別碼字串。</span><span class="sxs-lookup"><span data-stu-id="7151b-176">The [**IDeviceTopology::GetDeviceId**](/windows/desktop/api/Devicetopology/nf-devicetopology-idevicetopology-getdeviceid) method call retrieves the device ID string that identifies the adapter device.</span></span> <span data-ttu-id="7151b-177">[**IMMDeviceEnumerator：： GetDevice**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice)方法呼叫會接受裝置識別碼字串做為輸入參數，並取得介面卡裝置的 [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice)介面。</span><span class="sxs-lookup"><span data-stu-id="7151b-177">The [**IMMDeviceEnumerator::GetDevice**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice) method call takes the device ID string as an input parameter, and retrieves the [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) interface of the adapter device.</span></span> <span data-ttu-id="7151b-178">接下來， [**IMMDevice：： Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) 方法呼叫會抓取子單位的 [**IKsControl**](/windows-hardware/drivers/ddi/ksproxy/nn-ksproxy-ikscontrol) 介面。</span><span class="sxs-lookup"><span data-stu-id="7151b-178">Next, the [**IMMDevice::Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) method call retrieves the [**IKsControl**](/windows-hardware/drivers/ddi/ksproxy/nn-ksproxy-ikscontrol) interface of the subunit.</span></span> <span data-ttu-id="7151b-179">如需有關 **IKsControl** 介面的詳細資訊，請參閱 Windows DDK 檔。</span><span class="sxs-lookup"><span data-stu-id="7151b-179">For more information about the **IKsControl** interface, see the Windows DDK documentation.</span></span>

<span data-ttu-id="7151b-180">接下來，上述程式碼範例會建立 [**KSNODEPROPERTY \_ 音訊 \_ 通道**](/windows-hardware/drivers/ddi/ksmedia/ns-ksmedia-ksnodeproperty_audio_channel) 結構，以描述低音提升屬性。</span><span class="sxs-lookup"><span data-stu-id="7151b-180">Next, the preceding code example creates a [**KSNODEPROPERTY\_AUDIO\_CHANNEL**](/windows-hardware/drivers/ddi/ksmedia/ns-ksmedia-ksnodeproperty_audio_channel) structure that describes the bass-boost property.</span></span> <span data-ttu-id="7151b-181">此程式碼範例會將結構的指標傳遞至 [**IKsControl：： KsProperty**](/windows-hardware/drivers/ddi/ksproxy/nf-ksproxy-ikscontrol-ksproperty) 方法，該方法會使用結構中的資訊來取得屬性值。</span><span class="sxs-lookup"><span data-stu-id="7151b-181">The code example passes a pointer to the structure to the [**IKsControl::KsProperty**](/windows-hardware/drivers/ddi/ksproxy/nf-ksproxy-ikscontrol-ksproperty) method, which uses the information in the structure to retrieve the property value.</span></span> <span data-ttu-id="7151b-182">如需有關 **KSNODEPROPERTY \_ 音訊 \_ 通道** 結構和 **IKsControl：： KsProperty** 方法的詳細資訊，請參閱 Windows DDK 檔。</span><span class="sxs-lookup"><span data-stu-id="7151b-182">For more information about the **KSNODEPROPERTY\_AUDIO\_CHANNEL** structure and the **IKsControl::KsProperty** method, see the Windows DDK documentation.</span></span>

<span data-ttu-id="7151b-183">音訊硬體通常會為音訊串流中的每個通道指派不同的低音提升狀態。</span><span class="sxs-lookup"><span data-stu-id="7151b-183">Audio hardware typically assigns a separate bass-boost state to each channel in an audio stream.</span></span> <span data-ttu-id="7151b-184">基本上，您可以針對某些通道啟用低音提升，並為其他通道停用。</span><span class="sxs-lookup"><span data-stu-id="7151b-184">In principle, bass boost can be enabled for some channels and disabled for others.</span></span> <span data-ttu-id="7151b-185">[**KSNODEPROPERTY \_ 音訊 \_ 通道**](/windows-hardware/drivers/ddi/ksmedia/ns-ksmedia-ksnodeproperty_audio_channel)結構包含指定頻道號碼的 **通道** 成員。</span><span class="sxs-lookup"><span data-stu-id="7151b-185">The [**KSNODEPROPERTY\_AUDIO\_CHANNEL**](/windows-hardware/drivers/ddi/ksmedia/ns-ksmedia-ksnodeproperty_audio_channel) structure contains a **Channel** member that specifies the channel number.</span></span> <span data-ttu-id="7151b-186">如果資料流程包含 *N* 個通道，則通道的編號是從0到 *N*-1。</span><span class="sxs-lookup"><span data-stu-id="7151b-186">If a stream contains *N* channels, the channels are numbered from 0 to *N*— 1.</span></span> <span data-ttu-id="7151b-187">上述程式碼範例只會針對 channel 0 取得低音提升屬性的值。</span><span class="sxs-lookup"><span data-stu-id="7151b-187">The preceding code example gets the value of the bass-boost property for channel 0 only.</span></span> <span data-ttu-id="7151b-188">這項實行隱含地假設所有通道的低音提升屬性都會一致地設定為相同的狀態。</span><span class="sxs-lookup"><span data-stu-id="7151b-188">This implementation implicitly assumes that the bass-boost properties for all of the channels are set uniformly to the same state.</span></span> <span data-ttu-id="7151b-189">因此，讀取通道0的低音提升屬性就足以判斷資料流程的低音提升屬性值。</span><span class="sxs-lookup"><span data-stu-id="7151b-189">Thus, reading the bass-boost property for channel 0 is sufficient to determine the bass-boost property value for the stream.</span></span> <span data-ttu-id="7151b-190">為了與此假設一致，設定增強型屬性的對應函式會將所有通道設定為相同的低音提升屬性值。</span><span class="sxs-lookup"><span data-stu-id="7151b-190">To be consistent with this assumption, a corresponding function to set the bass-boost property would set all channels to the same bass-boost property value.</span></span> <span data-ttu-id="7151b-191">這些都是合理的慣例，但並非所有硬體廠商都必須遵循它們。</span><span class="sxs-lookup"><span data-stu-id="7151b-191">These are reasonable conventions, but not all hardware vendors necessarily follow them.</span></span> <span data-ttu-id="7151b-192">例如，廠商可能會提供一個控制台應用程式，只對驅動全範圍喇叭的通道啟用低音提升。</span><span class="sxs-lookup"><span data-stu-id="7151b-192">For example, a vendor might supply a control-panel application that enables bass boost only for channels that drive full-range speakers.</span></span> <span data-ttu-id="7151b-193"> (全範圍的喇叭可以從低音到高音播放整個範圍的音效。 ) 在這種情況下，上述程式碼範例所抓取的屬性值可能無法正確呈現資料流程的低音提升狀態。</span><span class="sxs-lookup"><span data-stu-id="7151b-193">(A full-range speaker is capable of playing sounds over the full range from bass to treble.) In that case, the property value retrieved by the preceding code example might not accurately represent the bass-boost state of the stream.</span></span>

<span data-ttu-id="7151b-194">使用上表所列控制項介面的用戶端可以呼叫 [**IPart：： RegisterControlChangeCallback**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-registercontrolchangecallback) 方法，以便在控制項參數的值變更時註冊通知。</span><span class="sxs-lookup"><span data-stu-id="7151b-194">Clients that use the control interfaces listed in the preceding table can call the [**IPart::RegisterControlChangeCallback**](/windows/desktop/api/Devicetopology/nf-devicetopology-ipart-registercontrolchangecallback) method to register for notifications when the value of a control parameter changes.</span></span> <span data-ttu-id="7151b-195">請注意， [**IKsControl**](/windows-hardware/drivers/ddi/ksproxy/nn-ksproxy-ikscontrol) 介面未提供類似的方法，讓用戶端在屬性值變更時註冊通知。</span><span class="sxs-lookup"><span data-stu-id="7151b-195">Note that the [**IKsControl**](/windows-hardware/drivers/ddi/ksproxy/nn-ksproxy-ikscontrol) interface does not provide a similar means for clients to register for notifications when a property value changes.</span></span> <span data-ttu-id="7151b-196">如果 **IKsControl** 支援屬性變更通知，則可能會在另一個應用程式變更屬性值時通知應用程式。</span><span class="sxs-lookup"><span data-stu-id="7151b-196">If **IKsControl** did support property-change notifications, it could inform an application when another application changed a property value.</span></span> <span data-ttu-id="7151b-197">不過，相較于透過 [**IPart**](/windows/desktop/api/Devicetopology/nn-devicetopology-ipart) 通知監視的常用控制項， **IKsControl** 所管理的屬性主要是供硬體廠商使用，而且這些屬性可能只會由廠商所撰寫的控制台應用程式來變更。</span><span class="sxs-lookup"><span data-stu-id="7151b-197">However, in contrast to the more commonly used controls that are monitored through [**IPart**](/windows/desktop/api/Devicetopology/nn-devicetopology-ipart) notifications, the properties managed by **IKsControl** are intended primarily for use by hardware vendors, and those properties are likely to be changed only by control-panel applications written by the vendors.</span></span> <span data-ttu-id="7151b-198">如果應用程式必須偵測其他應用程式所做的屬性變更，它可以透過 **IKsControl** 定期輪詢屬性值，來偵測變更。</span><span class="sxs-lookup"><span data-stu-id="7151b-198">If an application must detect property changes made by another application, it can detect the changes by periodically polling the property value through **IKsControl**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7151b-199">相關主題</span><span class="sxs-lookup"><span data-stu-id="7151b-199">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7151b-200">程式設計指南</span><span class="sxs-lookup"><span data-stu-id="7151b-200">Programming Guide</span></span>](programming-guide.md)
</dt> </dl>

 

 
