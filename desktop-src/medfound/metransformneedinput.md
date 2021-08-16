---
description: 由非同步媒體基礎轉換 (MFT) 傳送，以要求新的輸入範例。
ms.assetid: 5d5c50d9-fe4e-47ff-ae09-980911ebfb22
title: 'METransformNeedInput 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cc15bdffebfd22b4aecac2818da85e39379f681aec0e12fe92f895824edb78f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013498"
---
# <a name="metransformneedinput-event"></a>METransformNeedInput 事件

由非同步媒體基礎轉換 (MFT) 傳送，以要求新的輸入範例。

## <a name="event-values"></a>事件值

從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。



| VARTYPE              | Description               |
|----------------------|---------------------------|
| VT \_ 空白<br/> | 沒有事件資料。<br/> |



## <a name="attributes"></a>屬性

此事件會定義下列屬性。



| 屬性                                                                        | 描述                                                                           |
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [MF \_ 事件 \_ MFT \_ 輸入 \_ 資料流程 \_ 識別碼](mf-event-mft-input-stream-id.md)<br/> | 需要輸入資料之資料流程的識別碼。<br/>*需要 ()*<br/> |



## <a name="remarks"></a>備註

非同步 MFTs 透過 [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) 介面傳送此事件。 同步 MFTs 不會傳送此事件。

當 MFT 用戶端收到此事件時，它應該呼叫 [**IMFTransform：:P rocessinput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) 來傳遞下一個範例。 事件物件的 [ [MF \_ 事件 \_ MFT \_ 輸入 \_ 資料流程 \_ 識別碼](mf-event-mft-input-stream-id.md) ] 屬性會指定需要資料的輸入資料流程。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>                                                               |
| 最低支援的伺服器<br/> | Windows僅限 Server 2008 R2 \[ desktop 應用程式\]<br/>                                                  |
| 標頭<br/>                   | <dl> <dt>Mfobjects (包含 Mfidl) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎事件](media-foundation-events.md)
</dt> <dt>

[非同步 MFTs](asynchronous-mfts.md)
</dt> </dl>

 

 




