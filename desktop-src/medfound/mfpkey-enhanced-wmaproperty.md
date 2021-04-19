---
description: 指定核心編碼器是否使用 &\# 0034;加上&\# 0034; 功能。
ms.assetid: 1ace09da-7dee-469e-a533-63b40ac747ab
title: 'MFPKEY_ENHANCED_WMA 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df1c7ddc0e7bfb6d62d51e535f10b257eac6f2ef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999734"
---
# <a name="mfpkey_enhanced_wma-property"></a>MFPKEY \_ 增強型 \_ WMA 屬性

指定核心編碼器是否使用「加號」功能。

## <a name="constant-for-ipropertybag"></a>IPropertyBag 的常數

僅可使用 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)。

## <a name="data-type"></a>資料類型

**VT \_ UI4**

## <a name="default-value"></a>預設值

0

## <a name="remarks"></a>備註

這個屬性僅適用于 Windows Media 音訊無損。

如果您將此屬性保留為預設值0，或將它設定為1，核心編碼器會決定是否應該使用 "Plus" 部分。 如果您將此屬性設定為2，則核心編碼器不會使用 "Plus" 功能。

這個屬性會改變列舉的媒體類型，因此，如果您設定它，就必須在設定輸出類型之前先這麼做。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-----------------------------------------------------------------------------------------|
| 用戶端<br/> | Windows Vista 或 Windows 7<br/>                                                   |
| 標頭<br/> | <dl> <dt>Wmcodecdsp。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎屬性](media-foundation-properties.md)
</dt> </dl>

 

 
