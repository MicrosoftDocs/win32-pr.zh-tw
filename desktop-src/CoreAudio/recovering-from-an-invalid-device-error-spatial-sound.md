---
description: '從 (空間音效的 Invalid-Device 錯誤中復原) '
title: '從 (空間音效的 Invalid-Device 錯誤中復原) '
ms.topic: article
ms.date: 10/29/2020
ms.openlocfilehash: 124d4a804c2f99c051fee50d1c8d819d794b87a5943c216951e0c72870de8c18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118406216"
---
# <a name="recovering-from-an-invalid-device-error-spatial-sound"></a>從 (空間音效的 Invalid-Device 錯誤中復原) 

Microsoft 空間音訊 API 的許多方法（例如 [ISpatialAudioClient](/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient)、 [ISpatialAudioObjectRenderStream](/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobjectrenderstream)和 [ISpatialAudioObject](/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobject)）會傳回錯誤碼（如果用戶端應用程式所使用的音訊端點裝置變得無效，或端點上的空間音訊轉譯格式有所變更）。 這些錯誤碼表示端點裝置已卸載，或音訊硬體或相關聯的硬體資源已重新設定、停用、移除、空間音訊模式已變更或無法使用。 通常，應用程式可以從這個錯誤中復原。

指出無效裝置錯誤的錯誤碼包括下列各項：

- SPTLAUDCLNT_E_DESTROYED
- AUDCLNT_E_DEVICE_INVALIDATED
- AUDCLNT_E_RESOURCES_INVALIDATED
- AUDCLNT_E_UNSUPPORTED_FORMAT
- SPTLAUDCLNT_E_INTERNAL

## <a name="strategies-for-handling-invalid-device-errors"></a>處理無效裝置錯誤的策略

從無效裝置錯誤中復原的建議策略，取決於應用程式是否根據內部需求自動選取特定裝置，或允許使用者從可用裝置清單中明確選取裝置。 

### <a name="default-audio-device"></a>預設音訊裝置

如果應用程式自動選取預設裝置，請使用下列步驟來復原。

1. 釋放 [ISpatialAudioObjectRenderStream](/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobjectrenderstream) 和 [ISpatialAudioClient](/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) 介面，以及用來呈現的任何其他空間音訊介面。 
1. 呼叫 [IMMDeviceEnumerator：： GetDefaultAudioEndpoint](/windows/win32/api/mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) 來取得目前的預設音訊裝置。
1. 嘗試在音訊裝置上啟用 **ISpatialAudioClient** 。
1. 啟動 **ISpatialAudioObjectRenderStream**。 

### <a name="specifically-selected-audio-device"></a>特別選取的音訊裝置

如果應用程式選取特定音訊裝置，請使用下列步驟來復原。

1. 釋放 ISpatialAudioObjectRenderStream 介面以及用於轉譯的任何其他空間音訊介面，但不要發行 **ISpatialAudioClient**。
1. 使用目前的 **ISpatialAudioClient** 實例來啟用 **ISpatialAudioObjectRenderStream**。

請注意，上述兩個策略都可以將相同的步驟套用至使用 [ISpatialAudioObjectRenderStreamForMetadata](/windows/win32/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudioobjectrenderstreamformetadata) 或 [ISpatialAudioObjectRenderStreamForHrtf](/windows/win32/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectrenderstreamforhrtf) 介面的應用程式。 只要以中繼資料或 Hrtf 介面取代上述步驟中的 **ISpatialAudioObjectRenderStream** 即可。


## <a name="related-topics"></a>相關主題

<dl> <dt>
[從 Invalid-Device 錯誤](recovering-from-an-invalid-device-error.md) 
 中復原[串流管理](stream-management.md)
</dt> </dl>

 

 



