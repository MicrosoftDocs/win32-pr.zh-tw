---
description: 自訂事件種類。
ms.assetid: a54a446c-0e96-467b-90f6-0f64a7c1727d
title: 'MEExtendedType 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d5551110fc3637a40834a7bf9251826f151ec62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983396"
---
# <a name="meextendedtype-event"></a>MEExtendedType 事件

自訂事件種類。 您可以使用此事件種類來定義元件的自訂事件。 使用擴充的事件種類來識別事件。 擴充的事件種類是與事件相關聯的 GUID 值。 如需詳細資訊，請參閱 [**IMFMediaEvent：： GetExtendedType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getextendedtype)。

## <a name="event-values"></a>事件值

從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。



| VARTYPE              | Description                           |
|----------------------|---------------------------------------|
| VT \_ 空白<br/> | 沒有事件資料。<br/> <br/> |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Mfobjects (包含 Mfidl) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎事件](media-foundation-events.md)
</dt> </dl>

 

 




