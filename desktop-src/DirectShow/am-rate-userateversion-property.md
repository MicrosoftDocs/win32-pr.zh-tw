---
description: 這個屬性是用來指出應使用哪個版本的速率變更屬性設定。
ms.assetid: 49d1bfda-749b-4614-9a75-1f76fa8b320d
title: 'AM_RATE_UseRateVersion 屬性 (Dvdmedia) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4dd33ef96c50ecc3da0711f08f0c7ffbf0a20825
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/22/2021
ms.locfileid: "107910216"
---
# <a name="am_rate_userateversion-property"></a>AM \_ RATE \_ UseRateVersion 屬性

這個屬性是用來指出應使用哪個版本的速率變更屬性設定。 值是 **文字** 類型。 高序位位元組包含次要版本號碼，而低序位位元組則包含低序位位元組。 因此，1.1 版會以0x0101 的值發出信號。

如果此解碼器不支援指定的版本，它應該會使 [**IKsPropertySet：： Set**](ikspropertyset-set.md) 的呼叫失敗，並傳回 E \_ NOINTERFACE。 如果來源篩選未設定版本，則該解碼器應預設為1.0 版。



| 標籤 | 值 |
|-------------------|-------------------------------|
| 屬性集 GUID | AM \_ KSPROPSETID \_ TSRateChange |
| 屬性識別碼       | AM \_ RATE \_ UseRateVersion      |
| 資料類型         | **WORD**                      |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Dvdmedia。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**速率變更屬性集**](rate-change-property-set.md)
</dt> </dl>

 

 




