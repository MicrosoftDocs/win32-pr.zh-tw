---
description: 設定 ASF 媒體來源，以在原始程式檔沒有索引時使用反復搜尋。
ms.assetid: 0dd6f202-cdbc-4a28-8907-5530a0a2141b
title: 'MFPKEY_ASFMediaSource_IterativeSeekIfNoIndex 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10cdc22f0b4f5490c7691cc40166cf929a16ba64
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "103696254"
---
# <a name="mfpkey_asfmediasource_iterativeseekifnoindex-property"></a>MFPKEY \_ ASFMediaSource \_ IterativeSeekIfNoIndex 屬性

設定 ASF 媒體來源，以在原始程式檔沒有索引時使用反復搜尋。



資料類型

PROPVARIANT 類型 (vt) 

PROPVARIANT 成員

**VARIANT \_ BOOL**

VT \_ BOOL

**boolVal**



## <a name="remarks"></a>備註

使用這個屬性來設定 ASF 媒體來源。 若要設定屬性，請將 **IPropertyStore** 指標傳遞至 *來源解析程式*。 如需詳細資訊，請參閱設定 [媒體來源](configuring-a-media-source.md)。

*反復搜尋* 是一種演算法，可在沒有索引的 ASF 檔案中尋找位置。 它會根據平均位元速率來使用一連串的近似值，以逐漸接近目標搜尋時間。  (演算法類似于二進位搜尋。 ) 反復的搜尋可能需要比依索引搜尋更長的時間，因此預設為停用。

如果設定此屬性，請使用下列屬性來設定搜尋參數：

-   [MFPKEY \_ ASFMediaSource \_ IterativeSeek \_ 最大 \_ 計數](mfpkey-asfmediasource-iterativeseek-max-count.md)
-   [MFPKEY \_ ASFMediaSource \_ IterativeSeek \_ 容錯 \_ （ \_ 毫秒）](mfpkey-asfmediasource-iterativeseek-tolerance-in-millisecond.md)

這些屬性會分別設定反覆運算次數和容錯值的最大數目。 當演算法達到反覆運算次數上限時，或當它找到的封包與搜尋時間的距離在指定的容錯範圍內時，就會中止。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 7 \[ 桌面應用程式 \| UWP 應用程式\]<br/>                                  |
| 最低支援的伺服器<br/> | Windows Server 2008 R2 \[ 桌面應用程式 \| UWP 應用程式\]<br/>                     |
| 標頭<br/>                   | <dl> <dt>Mfidl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎屬性](media-foundation-properties.md)
</dt> </dl>

 

 




