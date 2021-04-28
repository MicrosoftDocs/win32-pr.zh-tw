---
description: AM_RATE_ResetOnTimeDisc 屬性-適用于 Windows Vista 和更新版本。
ms.assetid: 3e342219-341e-49a2-9f8f-4188dd7bf719
title: 'AM_RATE_ResetOnTimeDisc 屬性 (Dvdmedia) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e867bff1f344e80ffd06c9c40276515f2cd4920c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096606"
---
# <a name="am_rate_resetontimedisc-property"></a>AM \_ RATE \_ ResetOnTimeDisc 屬性

適用于 Windows Vista 和更新版本。

此屬性會查詢當解碼器收到具有不連續旗標的範例時，是否將輸出時間戳記重新同步處理至輸入時間戳記。

這是可讀寫的屬性。



| 標籤 | 值 |
|-------------------|-------------------------------|
| 屬性集 GUID | AM \_ KSPROPSETID \_ TSRateChange |
| 屬性識別碼       | AM \_ RATE \_ ResetOnTimeDisc     |
| 資料類型         | **Dword**                     |



 

## <a name="remarks"></a>備註

這個屬性支援流暢的速率變更。 如果這個屬性的值為 **TRUE** ，且解碼器收到具有 AM 範例 TIMEDISCONTINUITY 旗標的輸入範例 \_ \_ ，則已解碼的框架應該具有與輸入框架相同的時間戳記。

若要取出 AM \_ 範例 \_ TIMEDISCONTINUITY 旗標，請在範例上呼叫 [**IMediaSample2：： GetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-getproperties) 。 旗標是設定在 [**AM \_ sample2.xml \_ 屬性**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties)結構的 **dwSampleFlags** 成員中。

如需詳細資訊，請參閱 [Windows Vista 中的 DVD 播放增強功能](dvd-playback-enhancements-in-windows-vista.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Dvdmedia。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**速率變更屬性集**](rate-change-property-set.md)
</dt> </dl>

 

 




