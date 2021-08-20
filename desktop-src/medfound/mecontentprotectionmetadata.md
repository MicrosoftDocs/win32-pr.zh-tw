---
description: 媒體資料流程會使用此事件將保護系統專屬的中繼資料傳送給該解碼器。
ms.assetid: 249446CA-AEF7-41A1-98EB-0B9392AE4AD8
title: 'MEContentProtectionMetadata 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d972dc667c7119f01b39bff132b36dfa11c2810960ed638bd41a0cd9336f7d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118062285"
---
# <a name="mecontentprotectionmetadata-event"></a>MEContentProtectionMetadata 事件

媒體資料流程會使用此事件將保護系統專屬的中繼資料傳送給該解碼器。

## <a name="event-values"></a>事件值

從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。



| VARTYPE              | 描述                           |
|----------------------|---------------------------------------|
| VT \_ 空白<br/> | 沒有事件資料。<br/> <br/> |



## <a name="attributes"></a>屬性

此事件會定義下列屬性。



| 屬性                                                                                              | 描述                                                                                         |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [MF \_ 事件 \_ 串流 \_ 中繼資料 \_ >KEYDATA](mf-event-stream-metadata-keydata.md)<br/>                | 這是選擇性屬性。 保護系統特定資料。<br/> <br/>              |
| [MF \_ 事件 \_ 串流 \_ 中繼資料 \_ 內容 \_ KEYIDS](mf-event-stream-metadata-content-keyids.md)<br/> | 與事件相關聯的內容金鑰識別碼。<br/> <br/>                          |
| [MF \_ 事件 \_ 串流 \_ 中繼資料 \_ SYSTEMID](mf-event-stream-metadata-systemid.md)<br/>              | 這是選擇性屬性。 主要資料的目標系統識別碼。<br/> <br/> |



## <a name="remarks"></a>備註

例如，會使用此事件來傳達金鑰旋轉事件。 在此情況下，應儘早傳送，以在使用新的金鑰識別碼開始傳遞的範例之前，先將它準備好給解碼器。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8.1 \[僅限桌面應用程式\]<br/>                                                             |
| 最低支援的伺服器<br/> | Windows Server 2012\[僅限 R2 desktop 應用程式\]<br/>                                                  |
| 標頭<br/>                   | <dl> <dt>Mfobjects (包含 Mfidl) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎事件](media-foundation-events.md)
</dt> </dl>

 

 




