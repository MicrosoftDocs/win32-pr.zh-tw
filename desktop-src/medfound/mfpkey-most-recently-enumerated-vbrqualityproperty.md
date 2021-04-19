---
description: 指定最新列舉輸出類型的 VBR 品質層級。
ms.assetid: 7d67e41f-060b-49a1-9e17-5db081ef4210
title: 'MFPKEY_MOST_RECENT_ENUMERATED_VBRQUALITY 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ccd3b5f3aae6dc5347672cf6697c3431163dcbd1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991007"
---
# <a name="mfpkey_most_recent_enumerated_vbrquality-property"></a>MFPKEY \_ 最 \_ 新的 \_ 列舉 \_ VBRQUALITY 屬性

指定最新列舉輸出類型的 VBR 品質層級。 唯讀。

## <a name="constant-for-ipropertybag"></a>IPropertyBag 的常數

僅可使用 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)。

## <a name="data-type"></a>資料類型

**VT \_ UI4**

## <a name="remarks"></a>備註

當編碼器做為媒體基礎轉換 (MFT) ，且它會在呼叫 [**IMFTransform：： GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype)時列舉輸出類型時，您可以針對 **MFPKEY \_ \_ 最近 \_ 列舉的 \_ VBRQUALITY** 屬性查詢 MFT。 傳回的值表示最近傳回之輸出媒體類型的 VBR 品質。 然後您可以使用該值來設定編碼器的 [**MFPKEY \_ 所需 \_ VBRQUALITY**](mfpkey-desired-vbrqualityproperty.md) 屬性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-----------------------------------------------------------------------------------------|
| 用戶端<br/> | Windows Vista 或 Windows 7<br/>                                                   |
| 標頭<br/> | <dl> <dt>Wmcodecdsp。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MFPKEY \_ VBRENABLED**](mfpkey-vbrenabledproperty.md)
</dt> <dt>

[**MFPKEY \_ 限制 \_ 列舉 \_ VBRQUALITY**](mfpkey-constrain-enumerated-vbrqualityproperty.md)
</dt> <dt>

[媒體基礎屬性](media-foundation-properties.md)
</dt> </dl>

 

 
