---
description: 針對以品質為基礎 (1-通過) 可變位速率 (VBR) 編碼音訊串流，指定所需的品質等級。
ms.assetid: 0bbb4f51-78c3-4455-bd96-9a6d80110220
title: 'MFPKEY_DESIRED_VBRQUALITY 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f52ab8cc791a5309b5df6537d133bce68e49d66a15ab79c12beeb7411cece8e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119939941"
---
# <a name="mfpkey_desired_vbrquality-property"></a>MFPKEY \_ 所需的 \_ VBRQUALITY 屬性

針對以品質為基礎 (1-通過) 可變位速率 (VBR) 編碼音訊串流，指定所需的品質等級。

## <a name="constant-for-ipropertybag"></a>IPropertyBag 的常數

僅可使用 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)。

## <a name="data-type"></a>資料類型

**VT \_ UI4**

## <a name="default-value"></a>預設值

0

## <a name="remarks"></a>備註

這個值可以是0到100，其中100是最高品質。 值為0表示不使用以品質為基礎的 VBR 編碼方法。

若要列舉符合特定品質需求的 VBR 模式，請設定下列編碼器屬性。

-   將 [**MFPKEY \_ VBRENABLED**](mfpkey-vbrenabledproperty.md) 設定為 **VARIANT \_ TRUE**。
-   Set [**MFPKEY \_ 將 \_ 列舉的 \_ VBRQUALITY 限制**](mfpkey-constrain-enumerated-vbrqualityproperty.md) 為 **VARIANT \_ TRUE**。
-   將 **MFPKEY \_ 所需的 \_ VBRQUALITY** 設定為所需的品質。 若為不失真模式，請將所需的品質設定為100。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                    |
| 標頭<br/>                   | <dl> <dt>Wmcodecdsp。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎屬性](media-foundation-properties.md)
</dt> </dl>

 

 
