---
description: 當來源特性變更時由媒體來源引發。
ms.assetid: df7bb9a3-5949-4a4a-8835-c5b1d01b5cb3
title: 'MESourceCharacteristicsChanged 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 659e9eea0352d131aac4959b2952e8426ae408a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106976810"
---
# <a name="mesourcecharacteristicschanged-event"></a>MESourceCharacteristicsChanged 事件

當來源的特性變更時由媒體來源引發。

## <a name="event-values"></a>事件值

從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。



| VARTYPE              | Description                           |
|----------------------|---------------------------------------|
| VT \_ 空白<br/> | 沒有事件資料。<br/> <br/> |



## <a name="attributes"></a>屬性

此事件會定義下列屬性。



| 屬性                                                                                                   | 描述                                                          |
|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [**MF \_ 事件 \_ 來源 \_ 特性**](mf-event-source-characteristics-attribute.md)<br/>          | 媒體來源的新特性。<br/> <br/>      |
| [**MF \_ 事件 \_ 來源 \_ 特性 \_ 舊**](mf-event-source-characteristics-old-attribute.md)<br/> | 媒體來源的先前特性。<br/> <br/> |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Mfobjects (包含 Mfidl) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)
</dt> <dt>

[媒體基礎事件](media-foundation-events.md)
</dt> </dl>

 

 




