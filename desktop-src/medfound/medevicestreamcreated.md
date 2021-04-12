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
# <a name="medevicestreamcreated-event"></a><span data-ttu-id="d164f-103">MEDeviceStreamCreated 事件</span><span class="sxs-lookup"><span data-stu-id="d164f-103">MEDeviceStreamCreated event</span></span>

<span data-ttu-id="d164f-104">MEDeviceStreamCreated 是由裝置 MFT 以 MEUnknown 媒體事件產生的擴充媒體事件種類。</span><span class="sxs-lookup"><span data-stu-id="d164f-104">MEDeviceStreamCreated is an extended media event type generated with an MEUnknown media event by the Device MFT.</span></span>

<span data-ttu-id="d164f-105">此擴充媒體事件種類沒有承載。</span><span class="sxs-lookup"><span data-stu-id="d164f-105">This extended media event type has no payload.</span></span>  <span data-ttu-id="d164f-106">應透過 [**IMFMediaEvent：： GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus) 方法提供適當的 HRESULT。</span><span class="sxs-lookup"><span data-stu-id="d164f-106">Appropriate HRESULT should be provided via the [**IMFMediaEvent::GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus) method.</span></span>




## <a name="remarks"></a><span data-ttu-id="d164f-107">備註</span><span class="sxs-lookup"><span data-stu-id="d164f-107">Remarks</span></span>

<span data-ttu-id="d164f-108">此擴充媒體事件必須由裝置 MFT 傳送，作為 DMFT 輸出資料流程中的媒體類型選取專案。</span><span class="sxs-lookup"><span data-stu-id="d164f-108">This extended media event must be sent by the Device MFT as a part of the media type selection on the output stream of the DMFT.</span></span>  <span data-ttu-id="d164f-109">在 IMFDeviceTransform 介面上叫用 SetOutputStreamState 時，DMFT 會負責以 [METransformInputStreamStateChanged](/windows-hardware/drivers/stream/metransforminputstreamstatechanged) 媒體事件來通知必要輸入資料流程狀態中的變更。</span><span class="sxs-lookup"><span data-stu-id="d164f-109">When the SetOutputStreamState is invoked on the IMFDeviceTransform interface, the DMFT is responsible for signaling the change in the required input stream states with the [METransformInputStreamStateChanged](/windows-hardware/drivers/stream/metransforminputstreamstatechanged) media event.</span></span> <span data-ttu-id="d164f-110">當管線已透過呼叫 DMFT 的 SetInputStreamState 確認輸入資料流程狀態變更時，DMFT 會負責完成其內部狀態設定，並引發 **MEDeviceStreamCreated** 擴充媒體事件種類。</span><span class="sxs-lookup"><span data-stu-id="d164f-110">When the input stream state change has been acknowledged by the pipeline with the call into SetInputStreamState of the DMFT, the DMFT is responsible for completing its internal state configuration and raising the **MEDeviceStreamCreated** extended media event type.</span></span>

<span data-ttu-id="d164f-111">如果未引發此擴充媒體事件種類，裝置轉換管理員將不會傳遞任何輸入框架給 DMFT。</span><span class="sxs-lookup"><span data-stu-id="d164f-111">If this extended media event type is not raised, the Device Transform Manager will not deliver any input frames to the DMFT.</span></span>
<span data-ttu-id="d164f-112">擴充的媒體事件種類也必須設定為 IMFMediaEvent 的屬性，也就是使用 **MF_EVENT_MFT_INPUT_STREAM_ID** 屬性的輸出資料流程識別碼。</span><span class="sxs-lookup"><span data-stu-id="d164f-112">The extended media event type must also set as an attribute of the IMFMediaEvent, the output stream ID using the **MF_EVENT_MFT_INPUT_STREAM_ID** attribute.</span></span>

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

## <a name="requirements"></a><span data-ttu-id="d164f-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="d164f-113">Requirements</span></span>



| <span data-ttu-id="d164f-114">需求</span><span class="sxs-lookup"><span data-stu-id="d164f-114">Requirement</span></span> | <span data-ttu-id="d164f-115">值</span><span class="sxs-lookup"><span data-stu-id="d164f-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d164f-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d164f-116">Minimum supported client</span></span><br/> | <span data-ttu-id="d164f-117">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d164f-117">Windows 10 \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="d164f-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d164f-118">Minimum supported server</span></span><br/> | <span data-ttu-id="d164f-119">僅限 Windows Server 2016 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d164f-119">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d164f-120">標頭</span><span class="sxs-lookup"><span data-stu-id="d164f-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="d164f-121"><dt>mftransform。h</dt></span><span class="sxs-lookup"><span data-stu-id="d164f-121"><dt>mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d164f-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d164f-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d164f-123">媒體基礎事件</span><span class="sxs-lookup"><span data-stu-id="d164f-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="d164f-124">串流音訊轉譯器</span><span class="sxs-lookup"><span data-stu-id="d164f-124">Streaming Audio Renderer</span></span>](streaming-audio-renderer.md)
</dt> </dl>

 

 
