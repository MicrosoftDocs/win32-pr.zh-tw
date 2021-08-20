---
description: AM_RATE_ReverseMaxFullDataRate 屬性-適用于 Windows Vista 和更新版本。
ms.assetid: 4f170736-516d-4420-a215-e0e414f036cd
title: 'AM_RATE_ReverseMaxFullDataRate 屬性 (Dvdmedia) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c02007ec0b8f7b3f14dee8490f69d654a99ad11480512408efdc656bbbc8561
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118002373"
---
# <a name="am_rate_reversemaxfulldatarate-property"></a>AM \_ RATE \_ ReverseMaxFullDataRate 屬性

適用于 Windows Vista 和更新版本。

傳回解碼器的最高反向播放速率。 屬性的值是最大反向速度 x 10000 的絕對值。 例如，如果最大的反向速度是-2.0，則此屬性的值為20000。

這個屬性的資料類型是 **\_ MaxFullDataRate**，其為 `typedef` **LONG**。

這是唯讀的屬性。



| 標籤 | 值 |
|-------------------|----------------------------------|
| 屬性集 GUID | AM \_ KSPROPSETID \_ TSRateChange    |
| 屬性識別碼       | AM \_ RATE \_ ReverseMaxFullDataRate |
| 資料類型         | **AM \_ MaxFullDataRate**          |



 

## <a name="remarks"></a>備註

支援順利反向播放的解碼器應該會公開此屬性。 如需詳細資訊，請參閱[Windows Vista 中的 DVD 播放增強功能](dvd-playback-enhancements-in-windows-vista.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Dvdmedia。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**速率變更屬性集**](rate-change-property-set.md)
</dt> </dl>

 

 




