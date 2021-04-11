---
description: 指定輸出的品質。
ms.assetid: 7b45633b-7f1c-4951-a462-ad6240b9ca31
title: 'MFPKEY_WMRESAMP_FILTERQUALITY 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4027d4bc3c0306240986cf632e171fa9a59ed18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191785"
---
# <a name="mfpkey_wmresamp_filterquality-property"></a>MFPKEY \_ WMRESAMP \_ FILTERQUALITY 屬性

指定輸出的品質。

## <a name="constant-for-ipropertybag"></a>IPropertyBag 的常數

僅可使用 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)。

## <a name="data-type"></a>資料類型

VT \_ I4

## <a name="applies-to"></a>套用至

-   [音訊 Resampler DSP](audioresampler.md)

## <a name="remarks"></a>備註

這個屬性的有效範圍是1到60（含）。 較高的值會產生較高品質的輸出，但會導致更多延遲。 1的值基本上與線性插補相同。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                             |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                    |
| 標頭<br/>                   | <dl> <dt>Wmcodecdsp。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎屬性](media-foundation-properties.md)
</dt> </dl>

 

 
