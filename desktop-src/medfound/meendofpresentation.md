---
description: 在簡報結束時由媒體來源引發。 此事件表示簡報中的所有串流都已完成。 媒體會話將此事件轉送到應用程式。
ms.assetid: 259b00ae-a91b-461b-a12f-f7291ecc04ff
title: 'MEEndOfPresentation 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e97a2689b8d0e2ae156daa84f27f0e10fb31b828ffedf027a7be47a6c330b7b0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119941457"
---
# <a name="meendofpresentation-event"></a>MEEndOfPresentation 事件

在簡報結束時由媒體來源引發。 此事件表示簡報中的所有串流都已完成。 媒體會話將此事件轉送到應用程式。

## <a name="event-values"></a>事件值

從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。



| VARTYPE              | 描述                           |
|----------------------|---------------------------------------|
| VT \_ 空白<br/> | 沒有事件資料。<br/> <br/> |



## <a name="attributes"></a>屬性

此事件會定義下列屬性。



| 屬性                                                                                               | 描述                                                                               |
|---------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [**\_已取消 MF 事件 \_ 來源 \_ 拓撲 \_**](mf-event-source-topology-canceled-attribute.md)<br/> | 指定 sequencer 來源是否取消此展示。<br/> <br/> |



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

 

 




