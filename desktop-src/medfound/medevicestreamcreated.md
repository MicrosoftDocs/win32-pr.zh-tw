---
description: MEDeviceStreamCreated 是由裝置 MFT 以 MEUnknown 媒體事件產生的擴充媒體事件種類。
ms.assetid: 8aaa6908-0f2e-4a73-9362-69f42b74f495
title: 'MEDeviceStreamCreated 事件 (mftransform) '
ms.topic: article
ms.date: 08/31/2018
ms.openlocfilehash: 632ebc305473cd596656a21f562be25d53c2bace
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191632"
---
# <a name="medevicestreamcreated-event"></a>MEDeviceStreamCreated 事件

MEDeviceStreamCreated 是由裝置 MFT 以 MEUnknown 媒體事件產生的擴充媒體事件種類。

此擴充媒體事件種類沒有承載。  應透過 [**IMFMediaEvent：： GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus) 方法提供適當的 HRESULT。




## <a name="remarks"></a>備註

此擴充媒體事件必須由裝置 MFT 傳送，作為 DMFT 輸出資料流程中的媒體類型選取專案。  在 IMFDeviceTransform 介面上叫用 SetOutputStreamState 時，DMFT 會負責以 [METransformInputStreamStateChanged](/windows-hardware/drivers/stream/metransforminputstreamstatechanged) 媒體事件來通知必要輸入資料流程狀態中的變更。 當管線已透過呼叫 DMFT 的 SetInputStreamState 確認輸入資料流程狀態變更時，DMFT 會負責完成其內部狀態設定，並引發 **MEDeviceStreamCreated** 擴充媒體事件種類。

如果未引發此擴充媒體事件種類，裝置轉換管理員將不會傳遞任何輸入框架給 DMFT。
擴充的媒體事件種類也必須設定為 IMFMediaEvent 的屬性，也就是使用 **MF_EVENT_MFT_INPUT_STREAM_ID** 屬性的輸出資料流程識別碼。

```cpp
IMFMediaEvent* pMediaEvent = nullptr;

hr = MFCreateMediaEvent (MEUnknown,
                         MEDeviceStreamCreated,
                         S_OK,
                         nullptr,
                         &pMediaEvent);
if (SUCCEEDED(hr))
{
    hr = pMediaEvent->SetUINT32(MF_EVENT_MFT_INPUT_STREAM_ID, GetOutputStreamId());
}

if (SUCCEEDED(hr))
{
    hr = m_pEventQueue->QueueEvent(pMediaEvent);
}

if (nullptr != pMediaEvent)
{
    pMediaEvent->Release();
    pMediaEvent = nullptr;
}

return hr;
```

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 10 桌面應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2016 \[ desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>mftransform。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎事件](media-foundation-events.md)
</dt> <dt>

[串流音訊轉譯器](streaming-audio-renderer.md)
</dt> </dl>

 

 
