---
description: 提供對品質管制員有關播放品質的意見反應。
ms.assetid: 1b4b6a2d-411e-42d1-a44b-bb1928e1c063
title: 'MEQualityNotify 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4dd019db55a0791ec5464cf67c7ee4d3e4a86f918efc2b4e87f4ddde2f3574ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118061873"
---
# <a name="mequalitynotify-event"></a>MEQualityNotify 事件

提供對品質管制員有關播放品質的意見反應。

## <a name="event-values"></a>事件值

從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。



| VARTYPE           | 描述                         |
|-------------------|-------------------------------------|
| VT \_ I8<br/> | 請參閱＜備註＞。<br/> <br/> |



## <a name="remarks"></a>備註

某些管線元件會引發此事件。 媒體會話藉由呼叫 [**IMFQualityManager：： NotifyQualityEvent**](/windows/desktop/api/mfidl/nf-mfidl-imfqualitymanager-notifyqualityevent) 方法，將事件轉寄給品質管制員。

事件的擴充類型表示事件資料的意義。



| 擴充類型                            | 事件資料                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MF \_ 品質 \_ 通知 \_ 處理 \_ 延遲 | 元件所引進的大約處理延遲（100-毫微秒單位）。<br/> 處理延遲是元件透過處理範例導入管線中的延遲量。 在某些情況下，只需查看 [**IMFQualityManager：： NotifyProcessInput**](/windows/desktop/api/mfidl/nf-mfidl-imfqualitymanager-notifyprocessinput) 和 [**IMFQualityManager：： NotifyProcessOutput**](/windows/desktop/api/mfidl/nf-mfidl-imfqualitymanager-notifyprocessoutput)的呼叫，就無法衍生延遲。 例如，輸入範例和輸出範例之間可能不會有一對一的對應關係。 在此情況下，元件可能會傳送具有處理延遲的 MEQualityNotify 事件。 如果處理延遲變更，元件可以在串流期間隨時傳送新的事件。<br/> |
| MF \_ 品質 \_ 通知 \_ 範例 \_ 延遲         | 範例的延遲時間，以 100-毫微秒單位表示。 如果值為正數，則表示此範例為晚期。 如果值為負數，則會提早範例。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |



 

若要取得延伸型別，請呼叫 [**IMFMediaEvent：： GetExtendedType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getextendedtype)。

傳送此事件時不需要管線元件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Mfobjects (包含 Mfidl) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMFQualityManager**](/windows/desktop/api/mfidl/nn-mfidl-imfqualitymanager)
</dt> <dt>

[媒體基礎事件](media-foundation-events.md)
</dt> </dl>

 

 




