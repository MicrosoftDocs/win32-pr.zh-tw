---
description: PKEY \_ AudioEndpoint \_ GUID 屬性會提供對應于音訊端點裝置的 DirectSound 裝置識別碼。
ms.assetid: d3119504-9b6a-47b8-b3c6-15cb329929cb
title: 'PKEY_AudioEndpoint_GUID (Mmdeviceapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45405cd2350777e535b50859e77aa56755d191fc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972977"
---
# <a name="pkey_audioendpoint_guid"></a><span data-ttu-id="678b4-103">PKEY \_ AudioEndpoint \_ GUID</span><span class="sxs-lookup"><span data-stu-id="678b4-103">PKEY\_AudioEndpoint\_GUID</span></span>

<span data-ttu-id="678b4-104">**PKEY \_ AudioEndpoint \_ GUID** 屬性會提供對應于音訊端點裝置的 DirectSound 裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="678b4-104">The **PKEY\_AudioEndpoint\_GUID** property supplies the DirectSound device identifier that corresponds to the audio endpoint device.</span></span> <span data-ttu-id="678b4-105">屬性值是一個 GUID，用戶端可以將其作為裝置識別碼提供給 DirectSound API 中的 **DirectSoundCreate** 或 **DirectSoundCaptureCreate** 函式。</span><span class="sxs-lookup"><span data-stu-id="678b4-105">The property value is a GUID that the client can supply as the device identifier to the **DirectSoundCreate** or **DirectSoundCaptureCreate** function in the DirectSound API.</span></span> <span data-ttu-id="678b4-106">此值可唯一識別系統中所有音訊端點裝置上的音訊端點裝置。</span><span class="sxs-lookup"><span data-stu-id="678b4-106">This value uniquely identifies the audio endpoint device across all audio endpoint devices in the system.</span></span> <span data-ttu-id="678b4-107">如需 DirectSound 的詳細資訊，請參閱 DirectX SDK 檔。</span><span class="sxs-lookup"><span data-stu-id="678b4-107">For more information about DirectSound, see the DirectX SDK documentation.</span></span>

<span data-ttu-id="678b4-108">**PROPVARIANT** 結構的 **vt** 成員會設定為 vt \_ LPWSTR。</span><span class="sxs-lookup"><span data-stu-id="678b4-108">The **vt** member of the **PROPVARIANT** structure is set to VT\_LPWSTR.</span></span>

<span data-ttu-id="678b4-109">**PROPVARIANT** 結構的 **pwszVal** 成員指向以 null 結尾的寬字元字串，其中包含可識別 DirectSound 中音訊端點裝置的 GUID。</span><span class="sxs-lookup"><span data-stu-id="678b4-109">The **pwszVal** member of the **PROPVARIANT** structure points to a null-terminated, wide-character string that contains a GUID that identifies the audio endpoint device in DirectSound.</span></span>

<span data-ttu-id="678b4-110">如先前所述， [MMDEVICE API](mmdevice-api.md) 支援 [裝置角色](device-roles.md)。</span><span class="sxs-lookup"><span data-stu-id="678b4-110">As explained previously, the [MMDevice API](mmdevice-api.md) supports [device roles](device-roles.md).</span></span> <span data-ttu-id="678b4-111">雖然 DirectSound 不直接支援裝置角色，但 DirectSound 用戶端可以使用 PKEY \_ AudioEndpoint \_ GUID 屬性，根據裝置的裝置角色來選取 DirectSound 轉譯或捕獲裝置。</span><span class="sxs-lookup"><span data-stu-id="678b4-111">Although DirectSound does not directly support device roles, a DirectSound client can use the PKEY\_AudioEndpoint\_GUID property to select a DirectSound rendering or capture device based on its device role.</span></span>

<span data-ttu-id="678b4-112">例如，DirectSound 應用程式會執行下列步驟，以建立對應到使用者已指派 eMultimedia 角色之轉譯端點裝置的 DirectSound 裝置：</span><span class="sxs-lookup"><span data-stu-id="678b4-112">For example, a DirectSound application performs the following steps to create a DirectSound device that corresponds to the rendering endpoint device that the user has assigned the eMultimedia role to:</span></span>

1.  <span data-ttu-id="678b4-113">呼叫 [**IMMDeviceEnumerator：： GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) 方法，以取得具有 eMultimedia 角色之呈現端點裝置的 [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) 介面。</span><span class="sxs-lookup"><span data-stu-id="678b4-113">Call the [**IMMDeviceEnumerator::GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) method to get the [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) interface of the rendering endpoint device that has the eMultimedia role.</span></span>
2.  <span data-ttu-id="678b4-114">呼叫 [**IMMDevice：： OpenPropertyStore**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-openpropertystore) 方法，以取得 eMultimedia 裝置的 **IPropertyStore** 介面。</span><span class="sxs-lookup"><span data-stu-id="678b4-114">Call the [**IMMDevice::OpenPropertyStore**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-openpropertystore) method to obtain the **IPropertyStore** interface of the eMultimedia device.</span></span> <span data-ttu-id="678b4-115">如需 **IPropertyStore** 的詳細資訊，請參閱 Windows SDK 檔。</span><span class="sxs-lookup"><span data-stu-id="678b4-115">For more information about **IPropertyStore**, see the Windows SDK documentation.</span></span>
3.  <span data-ttu-id="678b4-116">呼叫 **IPropertyStore：： GetValue** 方法以取得 PKEY \_ AudioEndpoint \_ GUID 屬性值。</span><span class="sxs-lookup"><span data-stu-id="678b4-116">Call the **IPropertyStore::GetValue** method to obtain the PKEY\_AudioEndpoint\_GUID property value.</span></span>
4.  <span data-ttu-id="678b4-117">將字串格式的 GUID 中的屬性值轉換為16位元組的 GUID 結構。</span><span class="sxs-lookup"><span data-stu-id="678b4-117">Convert the property value from a GUID in string format to a 16-byte GUID structure.</span></span>
5.  <span data-ttu-id="678b4-118">使用 GUID 呼叫 **DirectSoundCreate** 函數，以建立具有 eMultimedia 角色的裝置。</span><span class="sxs-lookup"><span data-stu-id="678b4-118">Call the **DirectSoundCreate** function with the GUID to create the device with the eMultimedia role.</span></span>

> [!Note]  
> <span data-ttu-id="678b4-119">**PKEY \_AudioEndpoint \_ GUID** 是唯讀屬性，不論應用程式在 [**IMMDevice：： OpenPropertyStore**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-openpropertystore)中所要求的儲存存取模式為何。</span><span class="sxs-lookup"><span data-stu-id="678b4-119">**PKEY\_AudioEndpoint\_GUID** is a read-only property regardless of the storage-access mode requested by the application in [**IMMDevice::OpenPropertyStore**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-openpropertystore).</span></span> <span data-ttu-id="678b4-120">如果應用程式嘗試使用 **IPropertyStore：： SetValue** 設定值，此呼叫會失敗，並出現 E \_ ACCESSDENIED 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="678b4-120">If an application attempts to set a value by using **IPropertyStore::SetValue**, this call fails with the E\_ACCESSDENIED error code.</span></span>

 

<span data-ttu-id="678b4-121">請注意，在步驟4中產生的16位元組 GUID 會符合在 DirectSound 裝置列舉期間識別裝置的裝置 GUID。</span><span class="sxs-lookup"><span data-stu-id="678b4-121">Note that the 16-byte GUID generated in step 4 matches the device GUID that identifies the device during DirectSound device enumeration.</span></span> <span data-ttu-id="678b4-122">**DirectSoundEnumerate** 函式會列舉呈現端點裝置，而 **DirectSoundCaptureEnumerate** 函式會列舉 capture 端點裝置。</span><span class="sxs-lookup"><span data-stu-id="678b4-122">The **DirectSoundEnumerate** function enumerates rendering endpoint devices, and the **DirectSoundCaptureEnumerate** function enumerates capture endpoint devices.</span></span> <span data-ttu-id="678b4-123">在任一種情況下，裝置 GUID 是傳遞給列舉回呼函數的第一個參數。</span><span class="sxs-lookup"><span data-stu-id="678b4-123">In either case, the device GUID is the first parameter passed to the enumeration callback function.</span></span> <span data-ttu-id="678b4-124">如需 DirectSound 列舉的詳細資訊，請參閱 DirectX SDK 檔。</span><span class="sxs-lookup"><span data-stu-id="678b4-124">For more information about DirectSound enumeration, see the DirectX SDK documentation.</span></span>

<span data-ttu-id="678b4-125">如需使用 PKEY \_ AudioEndpoint \_ GUID 屬性的程式碼範例，請參閱 [DirectSound 應用程式的裝置角色](device-roles-for-directsound-applications.md)。</span><span class="sxs-lookup"><span data-stu-id="678b4-125">For a code example that uses the PKEY\_AudioEndpoint\_GUID property, see [Device Roles for DirectSound Applications](device-roles-for-directsound-applications.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="678b4-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="678b4-126">Requirements</span></span>



| <span data-ttu-id="678b4-127">需求</span><span class="sxs-lookup"><span data-stu-id="678b4-127">Requirement</span></span> | <span data-ttu-id="678b4-128">值</span><span class="sxs-lookup"><span data-stu-id="678b4-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="678b4-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="678b4-129">Minimum supported client</span></span><br/> | <span data-ttu-id="678b4-130">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="678b4-130">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="678b4-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="678b4-131">Minimum supported server</span></span><br/> | <span data-ttu-id="678b4-132">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="678b4-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="678b4-133">標頭</span><span class="sxs-lookup"><span data-stu-id="678b4-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="678b4-134"><dt>Mmdeviceapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="678b4-134"><dt>Mmdeviceapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="678b4-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="678b4-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="678b4-136">**音訊端點屬性**</span><span class="sxs-lookup"><span data-stu-id="678b4-136">**Audio Endpoint Properties**</span></span>](audio-endpoint-properties.md)
</dt> <dt>

[<span data-ttu-id="678b4-137">核心音訊屬性</span><span class="sxs-lookup"><span data-stu-id="678b4-137">Core Audio Properties</span></span>](core-audio-properties.md)
</dt> </dl>

 

 




