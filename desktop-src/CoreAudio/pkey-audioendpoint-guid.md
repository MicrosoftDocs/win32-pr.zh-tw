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
# <a name="pkey_audioendpoint_guid"></a>PKEY \_ AudioEndpoint \_ GUID

**PKEY \_ AudioEndpoint \_ GUID** 屬性會提供對應于音訊端點裝置的 DirectSound 裝置識別碼。 屬性值是一個 GUID，用戶端可以將其作為裝置識別碼提供給 DirectSound API 中的 **DirectSoundCreate** 或 **DirectSoundCaptureCreate** 函式。 此值可唯一識別系統中所有音訊端點裝置上的音訊端點裝置。 如需 DirectSound 的詳細資訊，請參閱 DirectX SDK 檔。

**PROPVARIANT** 結構的 **vt** 成員會設定為 vt \_ LPWSTR。

**PROPVARIANT** 結構的 **pwszVal** 成員指向以 null 結尾的寬字元字串，其中包含可識別 DirectSound 中音訊端點裝置的 GUID。

如先前所述， [MMDEVICE API](mmdevice-api.md) 支援 [裝置角色](device-roles.md)。 雖然 DirectSound 不直接支援裝置角色，但 DirectSound 用戶端可以使用 PKEY \_ AudioEndpoint \_ GUID 屬性，根據裝置的裝置角色來選取 DirectSound 轉譯或捕獲裝置。

例如，DirectSound 應用程式會執行下列步驟，以建立對應到使用者已指派 eMultimedia 角色之轉譯端點裝置的 DirectSound 裝置：

1.  呼叫 [**IMMDeviceEnumerator：： GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) 方法，以取得具有 eMultimedia 角色之呈現端點裝置的 [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) 介面。
2.  呼叫 [**IMMDevice：： OpenPropertyStore**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-openpropertystore) 方法，以取得 eMultimedia 裝置的 **IPropertyStore** 介面。 如需 **IPropertyStore** 的詳細資訊，請參閱 Windows SDK 檔。
3.  呼叫 **IPropertyStore：： GetValue** 方法以取得 PKEY \_ AudioEndpoint \_ GUID 屬性值。
4.  將字串格式的 GUID 中的屬性值轉換為16位元組的 GUID 結構。
5.  使用 GUID 呼叫 **DirectSoundCreate** 函數，以建立具有 eMultimedia 角色的裝置。

> [!Note]  
> **PKEY \_AudioEndpoint \_ GUID** 是唯讀屬性，不論應用程式在 [**IMMDevice：： OpenPropertyStore**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-openpropertystore)中所要求的儲存存取模式為何。 如果應用程式嘗試使用 **IPropertyStore：： SetValue** 設定值，此呼叫會失敗，並出現 E \_ ACCESSDENIED 錯誤碼。

 

請注意，在步驟4中產生的16位元組 GUID 會符合在 DirectSound 裝置列舉期間識別裝置的裝置 GUID。 **DirectSoundEnumerate** 函式會列舉呈現端點裝置，而 **DirectSoundCaptureEnumerate** 函式會列舉 capture 端點裝置。 在任一種情況下，裝置 GUID 是傳遞給列舉回呼函數的第一個參數。 如需 DirectSound 列舉的詳細資訊，請參閱 DirectX SDK 檔。

如需使用 PKEY \_ AudioEndpoint \_ GUID 屬性的程式碼範例，請參閱 [DirectSound 應用程式的裝置角色](device-roles-for-directsound-applications.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                     |
| 標頭<br/>                   | <dl> <dt>Mmdeviceapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**音訊端點屬性**](audio-endpoint-properties.md)
</dt> <dt>

[核心音訊屬性](core-audio-properties.md)
</dt> </dl>

 

 




