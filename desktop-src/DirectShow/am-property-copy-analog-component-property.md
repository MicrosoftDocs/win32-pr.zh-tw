---
description: 查詢影片輸出是否為標準定義、類比元件影片。
ms.assetid: bd4fc5bc-c45d-4228-9759-6300fdfff6a0
title: 'AM_PROPERTY_COPY_ANALOG_COMPONENT 屬性 (Dvdmedia) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6448bfbcc07be6ca37189c15c7c605887e6d22b3
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/22/2021
ms.locfileid: "107910306"
---
# <a name="am_property_copy_analog_component-property"></a>AM \_ 屬性 \_ 複製 \_ 類比 \_ 元件屬性

查詢影片輸出是否為標準定義、類比元件影片。



| 標籤 | 值 |
|-------------------|---------------------------------------|
| 屬性集 GUID | AM \_ KSPROPSETID \_ CopyProt             |
| 屬性識別碼       | AM \_ 屬性 \_ 複製 \_ 類比 \_ 元件 |
| 資料類型         | **ULONG**                             |



 

## <a name="remarks"></a>備註

這是唯讀的屬性。

如果影片輸出是類比元件影片，其解析度不大於480p （針對 NTSC）或540p （適用于 PAL），則此屬性的值為 **TRUE** 。 否則，此值為 **FALSE**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Dvdmedia。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**DVD 禁止複製屬性集**](dvd-copy-protection-property-set.md)
</dt> </dl>

 

 




