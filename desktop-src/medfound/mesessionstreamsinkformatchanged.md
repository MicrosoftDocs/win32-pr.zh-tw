---
description: 當媒體接收器的格式變更時，由媒體會話引發。
ms.assetid: f56419f8-7f50-4eda-bf4a-fcdbbe46e180
title: 'MESessionStreamSinkFormatChanged 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f08d086d5966e0fc1f6ce4b4b3d639b40d795a4e05799f3928f61afa9abddf4d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119268588"
---
# <a name="mesessionstreamsinkformatchanged-event"></a>MESessionStreamSinkFormatChanged 事件

當媒體接收器的格式變更時，由媒體會話引發。

## <a name="event-values"></a>事件值

從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。



| VARTYPE              | 描述                           |
|----------------------|---------------------------------------|
| VT \_ 空白<br/> | 沒有事件資料。<br/> <br/> |



## <a name="attributes"></a>屬性

此事件會定義下列屬性。



| 屬性                                                                    | 描述                                                                                  |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [**MF \_ 事件 \_ 輸出 \_ 節點**](mf-event-output-node-attribute.md)<br/> | 識別其格式已變更之媒體接收器的拓撲節點。<br/> <br/> |



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

 

 




