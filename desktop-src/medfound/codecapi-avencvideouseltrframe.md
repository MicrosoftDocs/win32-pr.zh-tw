---
description: 指定目前的框架使用一或多個 LTR 框架進行編碼。
ms.assetid: 51FD6E36-9CDF-4005-942F-7A92CA706F38
title: 'CODECAPI_AVEncVideoUseLTRFrame 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c438a4e6e2656c5e952062d9e3c1c0000899f2c
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473154"
---
# <a name="codecapi_avencvideouseltrframe-property"></a>CODECAPI \_ AVEncVideoUseLTRFrame 屬性

指定目前的框架使用一或多個 LTR 框架進行編碼。

## <a name="data-type"></a>資料類型

**ULONG** (VT \_ UI4) 

## <a name="property-guid"></a>屬性 GUID

**CODECAPI \_ AVEncVideoUseLTRFrame**

## <a name="property-value"></a>屬性值

此控制項的值包含兩個欄位，其中每個欄位都有16個位。




| 值 | 意義 | 
|-------|---------|
| <span id="The_first_field"></span><span id="the_first_field"></span><span id="THE_FIRST_FIELD"></span><dl><dt><strong>第一個欄位</strong></dt><dt>位 [0.. 15]</dt></dl> | 指出哪些 LTR 框架 (s) 允許編碼目前的框架。 <br /><strong>H.264/AVC 編碼器：</strong><br /> 這是表示可以使用哪些 LTR 框架做為此框架參考的點陣圖。 最不重要的位會對應到 LTR 索引0，第二個最小的位則對應到 LTR 索引1等等。<br /> 此值不得為0。<br /> 此值指定的最高索引不能大於 <a href="codecapi-avencvideoltrbuffercontrol.md">CODECAPI_AVEncVideoLTRBufferControl</a> 屬性中指定的 LTR 框架數目上限。<br /> | 
| <span id="The_second_field"></span><span id="the_second_field"></span><span id="THE_SECOND_FIELD"></span><dl><dt><strong>第二個欄位</strong></dt><dt>位 [16.. 31]</dt></dl> | 指出編碼後續框架是否需要額外限制的旗標。 <br /><strong>H.264/AVC 編碼器：</strong><br /> 1是在此欄位唯一有效的值。 所有其他值都無效，並保留供日後使用。<br /> 當旗標為1時，編碼器應該依照下列條件約束，編碼編碼順序中的後續框架：<br /><ul><li>它不應使用比目前框架更舊的編碼順序或編碼順序中未來編碼的短期參考框架。</li><li>它不應該使用最近 CODECAPI_AVEncVideoUseLTRFrame 控制項未描述的 LTR 框架。</li><li>它可能會使用目前框架之後更新的 LTR 框架。</li></ul> | 




 

## <a name="remarks"></a>備註

**H.264/AVC 編碼器：**

如果使用 CODECAPI AVEncVideoUseLTRFrame 屬性發出了暫止的呼叫， \_ 但編碼器尚未產生使用 ltr 的框架，就不應呼叫這個屬性。 換句話說，編碼器不應將 CODECAPI AVEncVideoUseLTRFrame 要求排入佇列 \_ 。

如果在 \_ 其他 CODECAPI AVEncVideoUseLTRFrame 要求仍在擱置中時提交 CODECAPI AVEncVideoUseLTRFrame 要求 \_ ，則應捨棄較舊的要求。

\_在非基底分層框架上呼叫 CODECAPI AVEncVideoUseLTRFrame 是有效的，而且應該套用至非基底分層框架，而不會延遲基底圖層框架。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8.1 \[桌面應用程式 \| UWP 應用程式\]<br/>                                   |
| 最低支援的伺服器<br/> | Windows Server 2012R2 \[ desktop apps \| UWP 應用程式\]<br/>                        |
| 標頭<br/>                   | <dl> <dt>Codecapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎屬性](media-foundation-properties.md)
</dt> </dl>

 

 




