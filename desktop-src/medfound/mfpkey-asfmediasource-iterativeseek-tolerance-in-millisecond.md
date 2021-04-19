---
description: 設定當 ASF 媒體來源執行反復搜尋時，所使用的容錯（以毫秒為單位）。
ms.assetid: 3ee4410f-857c-4978-a308-87decfba0e2f
title: 'MFPKEY_ASFMediaSource_IterativeSeek_Tolerance_In_MilliSecond 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4190d9f87d906a701908dfc17b61633204fe8a2
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106981932"
---
# <a name="mfpkey_asfmediasource_iterativeseek_tolerance_in_millisecond-property"></a>MFPKEY \_ ASFMediaSource \_ IterativeSeek \_ 容錯 \_ In \_ 毫秒屬性

設定當 ASF 媒體來源執行反復搜尋時，所使用的容錯（以毫秒為單位）。



資料類型

PROPVARIANT 類型 (vt) 

PROPVARIANT 成員

**ULONG**

VT \_ UI4

**ulVal**



## <a name="remarks"></a>備註

使用這個屬性來設定 ASF 媒體來源。 若要設定屬性，請將 **IPropertyStore** 指標傳遞至來源解析程式。 如需詳細資訊，請參閱設定 [媒體來源](configuring-a-media-source.md)。

只有在已啟用反復搜尋時，才會套用此屬性。 如需詳細資訊，請參閱 [MFPKEY \_ ASFMediaSource \_ IterativeSeekIfNoIndex](mfpkey-asfmediasource-iterativeseekifnoindex.md)。

如果找到的封包與搜尋時間的距離在指定的容錯範圍內，則反復搜尋演算法會中止。 預設值為8000毫秒。

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

 

 




