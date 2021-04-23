---
description: DVD 導覽器會使用此屬性來通知解碼器，導覽器會在其傳遞給解碼器的範例上設定正確的時間戳記。
ms.assetid: f04e8291-734f-483e-b756-5362beb68d9c
title: 'AM_RATE_CorrectTS 屬性 (Dvdmedia) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15c65b613f892708dc210af2ca2a05efb74785fb
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/22/2021
ms.locfileid: "107910296"
---
# <a name="am_rate_correctts-property"></a>AM \_ RATE \_ CorrectTS 屬性

DVD 導覽器會使用此屬性來通知解碼器，導覽器會在其傳遞給解碼器的範例上設定正確的時間戳記。



| 標籤 | 值 |
|-------------------|-------------------------------|
| 屬性集 GUID | AM \_ KSPROPSETID \_ TSRateChange |
| 屬性識別碼       | AM \_ RATE \_ CorrectTS           |
| 資料類型         | **LONG**                      |



 

## <a name="remarks"></a>備註

當播放速率是1.0 以外的時間時，較舊版本的 DVD Navigator 未設定正確的時間戳記。 許多的解碼器都能解決此問題，方法是忽略倒轉或向前快轉期間的時間戳記，並估計正確的呈現時間。

這些問題已在目前的 DVD 導覽器版本中修正。 為了與現有的解碼器具有回溯相容性，DVD 導覽器會藉由在 \_ \_ 具有 **TRUE** 值的解碼器上設定 AM RATE CorrectTS 屬性，來指出時間戳記是否正確。 當設定這個屬性時，解碼器應該使用實際的時間戳記，而不是估計呈現時間。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Dvdmedia。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**速率變更屬性集**](rate-change-property-set.md)
</dt> </dl>

 

 




