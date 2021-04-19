---
description: 此屬性會查詢解碼器所支援的最大全畫面播放速率。 這個屬性的資料型別是 AM \_ QueryRate 結構。
ms.assetid: 98808ed4-6d34-437b-9729-9cc805bc81f0
title: 'AM_RATE_QueryFullFrameRate 屬性 (Dvdmedia) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab2c99564caa09253198b101a3e2467ec88c7e34
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993558"
---
# <a name="am_rate_queryfullframerate-property"></a>AM \_ RATE \_ QueryFullFrameRate 屬性

此屬性會查詢解碼器所支援的最大全畫面播放速率。 這個屬性的資料型別是 **AM \_ QueryRate** 結構。

這個屬性是針對這個屬性集的1.1 版所定義;請參閱 [**AM \_ RATE \_ UseRateVersion**](am-rate-userateversion-property.md)。



|                   |                                       |
|-------------------|---------------------------------------|
| 屬性集 GUID | AM \_ KSPROPSETID \_ TSRateChange         |
| 屬性識別碼       | AM \_ RATE \_ QueryFullFrameRate 屬性 |
| 資料類型         | [**AM \_ QueryRate**](/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_queryrate) |



 

## <a name="remarks"></a>備註

如果播放速率超過解碼器的最大速率，來源篩選會傳送連續樣本的群組（以不連續分隔）。 時間戳記會跳到不連續。 即使播放速率是在解碼器的最大速率內，來源篩選也可能這樣做，因為可能會有其他因素，例如磁片 IO，這會限制完整的播放速率。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Dvdmedia。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**速率變更屬性集**](rate-change-property-set.md)
</dt> </dl>

 

 




