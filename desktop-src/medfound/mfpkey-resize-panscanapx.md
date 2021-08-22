---
description: 指定移動流覽/掃描區域左上角的 x 座標。
ms.assetid: 1aed8614-d856-4885-80fe-c3f2bf3304ad
title: 'MFPKEY_RESIZE_PANSCANAPX 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22e127601764a9131a5dd494e3c8d6fddc2692106275ad5912bbfdd3b8026951
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119463218"
---
# <a name="mfpkey_resize_panscanapx-property"></a>MFPKEY \_ RESIZE \_ PANSCANAPX 屬性

指定移動流覽/掃描區域左上角的 x 座標。

## <a name="constant-for-ipropertybag"></a>IPropertyBag 的常數

僅可使用 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)。

## <a name="data-type"></a>資料類型

VT \_ I4

## <a name="applies-to"></a>套用至

-   [影片尺寸調整 DSP](videoresizer.md)

## <a name="remarks"></a>備註

此值為固定點實數。 數位的整數部分會儲存在較高的2個位元組中，小數部分則會儲存在2個較低的位元組中。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>                                             |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                    |
| 標頭<br/>                   | <dl> <dt>Wmcodecdsp。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎屬性](media-foundation-properties.md)
</dt> </dl>

 

 
