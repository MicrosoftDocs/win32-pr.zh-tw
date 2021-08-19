---
description: 表示媒體資料流程沒有可在指定時間提供資料的信號。
ms.assetid: 1a00fff1-c3ab-4965-a663-3c15bb48ea98
title: 'MEStreamTick 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42b72a61964e296ac5f7aa69eb2be6773b622f7b44df8300affa0150af2f8a77
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974057"
---
# <a name="mestreamtick-event"></a>MEStreamTick 事件

表示媒體資料流程沒有可在指定時間提供資料的信號。

## <a name="event-values"></a>事件值

從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。



| VARTYPE           | 描述                                                                   |
|-------------------|-------------------------------------------------------------------------------|
| VT \_ I8<br/> | 間隔發生的時間，以 100-毫微秒單位表示。<br/> <br/> |



## <a name="remarks"></a>備註

此事件表示資料中有間距。 事件會通知下游元件在指定時間不會預期任何資料。

當物件產生串流中媒體範例的時間戳記時，應傳送此事件。 根據資料的格式而定，這可能是：

-   媒體來源上的媒體串流 ([**IMFMediaStream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) 介面) ，或
-    ([**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) 介面) 的解碼器轉換。

在這段時間內，物件應該傳送的事件與通常會產生範例的頻率相同。 針對影片，針對每個遺漏的框架傳送一個事件。 針對音訊，在間距期間每秒至少傳送一次事件。 事件的值為遺漏範例的時間戳記。 視需要傳送任意數量的 MEStreamTick 事件以填滿資料中的間距。

如果媒體來源有多個資料流程，而且有一個以上的資料流程有間距，則每個資料流程都應該傳送 MEStreamTick 事件。 例如，如果音訊和影片資料中有間距，則這兩個數據流都會傳送事件。

MEStreamTick 事件未完成 [**IMFMediaStream：： RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) 要求。 媒體來源仍然必須針對每個 **RequestSample** 呼叫傳送 [MEMediaSample](memediasample.md)事件。

媒體接收無法直接使用此事件。 若要對媒體接收器發出資料流程中的間隙，請使用 **MFSTREAMSINK \_ 標記 \_ 刻度** 標記來呼叫 [**IMFStreamSink：:P lacemarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) 。 媒體基礎管線會在需要時，將 MEStreamTick 事件轉換成 **MFSTREAMSINK \_ 標記 \_ 刻度** 標記。

請勿在 MEStreamTick 事件之後的下一個媒體範例中，設定 MFSampleExtension 不中斷屬性。 [**\_**](mfsampleextension-discontinuity-attribute.md) **MFSampleExtension 中斷 \_** 屬性工作表示時間戳記與先前的時間戳記不連續，而 MEStreamTick 表示時間戳記是連續的，但遺漏了部分資料。

> [!Note]  
> 較早版本的檔不正確地指出 MEStreamTick 事件之後的範例應該有 MFSampleExtension 不 [**連續 \_**](mfsampleextension-discontinuity-attribute.md) 屬性。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Mfobjects (包含 Mfidl) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎事件](media-foundation-events.md)
</dt> </dl>

 

 




