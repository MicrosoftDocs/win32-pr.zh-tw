---
description: 指定成功連接至媒體接收器的串流。
ms.assetid: b5e45bfc-d91d-41b8-aaa4-72b3a23d869e
title: 'MFP_PKEY_StreamRenderingResults 屬性 (Mfplay) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6acf04f751e8611f3add3a62fc7b4406d757999e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318547"
---
# <a name="mfp_pkey_streamrenderingresults-property"></a>MFP \_ PKEY \_ StreamRenderingResults 屬性

> [!IMPORTANT]
> 已取代。 此 API 可能會從 Windows 的未來版本中移除。 應用程式應該使用 [媒體會話](media-session.md) 來播放。

 

指定成功連接至媒體接收器的串流。



資料類型

PROPVARIANT 類型 (vt) 

PROPVARIANT 成員

**DWORD** 值的陣列 (**CAUL**) 

VT \_ 向量 \| vt \_ UI4

**科爾**



## <a name="remarks"></a>備註

這個屬性可以使用 [MFP] **\_ 事件 \_ 類型 \_ MEDIAITEM \_ SET** 事件來傳送。

屬性的值是 **HRESULT** s 的陣列。 陣列專案對應到目前媒體專案上的資料流程。 陣列中的每個專案都會指出對應的資料流程是否已連接到媒體接收器，如下所示：

-   如果資料流程連接到媒體接收器，則值為 **S \_ OK**。
-   如果未選取資料流程，則值為 **S \_ FALSE**。
-   如果嘗試連接資料流程時發生錯誤，此值會是錯誤碼。

如果至少有一個資料流程連接成功，就可以播放。 例如，使用者可能會有播放音訊串流所需的編解碼器，但無法播放影片串流。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 R2 \[ desktop 應用程式\]<br/>                             |
| 標頭<br/>                   | <dl> <dt>Mfplay。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎屬性](media-foundation-properties.md)
</dt> <dt>

[**MFP \_ MEDIAITEM \_ 設定 \_ 事件**](/windows/desktop/api/mfplay/ns-mfplay-mfp_mediaitem_set_event)
</dt> </dl>

 

 




