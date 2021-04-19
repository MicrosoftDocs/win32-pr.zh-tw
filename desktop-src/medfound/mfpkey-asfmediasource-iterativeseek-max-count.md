---
description: 設定 ASF 媒體來源在執行反復搜尋時，所要使用的搜尋反復專案數目上限。
ms.assetid: 5b596faf-1217-424d-ae16-8c9ec6f31af1
title: 'MFPKEY_ASFMediaSource_IterativeSeek_Max_Count 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfb9268f1def2ab0d489f58cafa0b1720196c7ac
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106985817"
---
# <a name="mfpkey_asfmediasource_iterativeseek_max_count-property"></a>MFPKEY \_ ASFMediaSource \_ IterativeSeek \_ Max \_ Count 屬性

設定 ASF 媒體來源在執行反復搜尋時，所要使用的搜尋反復專案數目上限。



資料類型

PROPVARIANT 類型 (vt) 

PROPVARIANT 成員

**ULONG**

VT \_ UI4

**ulVal**



## <a name="remarks"></a>備註

使用這個屬性來設定 ASF 媒體來源。 若要設定屬性，請將 **IPropertyStore** 指標傳遞至來源解析程式。 如需詳細資訊，請參閱設定 [媒體來源](configuring-a-media-source.md)。

只有在已啟用反復搜尋時，才會套用此屬性。 如需詳細資訊，請參閱 [MFPKEY \_ ASFMediaSource \_ IterativeSeekIfNoIndex](mfpkey-asfmediasource-iterativeseekifnoindex.md)。

這個屬性的有效範圍是 \[ 1-10 \] （含）。 使用較高的數位，反復的搜尋通常更準確，但需要較長的時間。

預設值為 5。

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

 

 




