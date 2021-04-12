---
description: 傳回已編碼的影片框架數目。
ms.assetid: ade9fe69-b3dd-44aa-856b-75d4a7e4c680
title: 'AVEncStatVideoCodedFrames 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3aed3ed0a06003807a6bd0db90b8978282042daf
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109372"
---
# <a name="avencstatvideocodedframes-property"></a>AVEncStatVideoCodedFrames 屬性

傳回已編碼的影片框架數目。

這是可讀寫的屬性。

## <a name="data-type"></a>資料類型

**UINT32** (**VT \_ UI4**) 

## <a name="property-guid"></a>屬性 GUID

**CODECAPI \_ AVEncStatVideoCodedFrames**

## <a name="remarks"></a>備註

編碼完成之後，就可以使用這個屬性。

這個屬性的值等於 [**AVEncStatVideoTotalFrames**](avencstatvideototalframes-property.md) 屬性減去捨棄的框架數目。 編碼器可能會捨棄框架，以保持在指定的位速率條件約束內。 它也可能會捨棄資料流程結尾的框架 (請參閱 [**AVEncCommonStreamEndHandling**](avenccommonstreamendhandling-property.md) 屬性) 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 專業版傳統型 \[ 應用程式 \| UWP 應用程式\]<br/>                     |
| 最低支援的伺服器<br/> | Windows 2000 Server \[ desktop 應用程式 \| UWP 應用程式\]<br/>                           |
| 標頭<br/>                   | <dl> <dt>Codecapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[編解碼器 API 屬性](codec-api-properties.md)
</dt> <dt>

[**ICodecAPI 介面**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




