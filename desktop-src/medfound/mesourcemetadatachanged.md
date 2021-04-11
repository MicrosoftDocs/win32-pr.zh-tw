---
description: 當媒體來源更新其中繼資料時引發。
ms.assetid: 6818b0c9-9628-41e6-8dc6-dff26f4fcfd2
title: 'MESourceMetadataChanged 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b72463d145d7b4b4b14ac3c321f19a7f9a4c2178
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943548"
---
# <a name="mesourcemetadatachanged-event"></a>MESourceMetadataChanged 事件

當媒體來源更新其中繼資料時引發。

## <a name="event-values"></a>事件值

從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。



| VARTYPE              | Description                           |
|----------------------|---------------------------------------|
| VT \_ 空白<br/> | 沒有事件資料。<br/> <br/> |



## <a name="remarks"></a>備註

如果媒體來源是在第一次建立來源時無法提供所有中繼資料，則應該在中繼資料可供使用之後引發此事件。

媒體來源應該建立新的簡報描述項，並將 (PD) 的表示描述項的所有屬性複製到事件物件。 應用程式可以使用事件物件來列舉新的 PD 屬性。 尤其是，在完全下載檔案之前， [mf \_ pd \_ DURATION](mf-pd-duration-attribute.md) 和 [MF \_ pd 檔案 \_ \_ \_ 大小總計](mf-pd-total-file-size-attribute.md) 的值可能是未知的。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Mfobjects (包含 Mfidl) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎事件](media-foundation-events.md)
</dt> <dt>

[展示描述項屬性](presentation-descriptor-attributes.md)
</dt> </dl>

 

 




