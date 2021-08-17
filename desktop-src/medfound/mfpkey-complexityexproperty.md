---
description: MFPKEY_COMPLEXITYEX 屬性-指定編碼器演算法的複雜度。
ms.assetid: abfc84d5-954f-4524-b3cb-5c5b9cfc7fa0
title: 'MFPKEY_COMPLEXITYEX 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e658e438909677f326372caa9e4da533e350b7133cc647b8f56562d09ad949e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117873535"
---
# <a name="mfpkey_complexityex-property"></a>MFPKEY \_ COMPLEXITYEX 屬性

指定編碼器演算法的複雜度。

## <a name="constant-for-ipropertybag"></a>IPropertyBag 的常數

g \_ wszWMVCComplexityEx

## <a name="data-type"></a>資料類型

VT \_ I4

## <a name="default-value"></a>預設值

預設值取決於影片編碼器的版本，如下表所示。



| 編碼器版本                 | 預設值 |
|---------------------------------|---------------|
| WindowsMedia Video 9 編碼器   | 3             |
| Windows媒體影片7/8 編碼器 | 1             |



 

## <a name="possible-values"></a>可能的值

可能的值取決於影片編碼器的版本，如下表所示。



| 編碼器版本                 | 可能值  |
|---------------------------------|------------------|
| WindowsMedia Video 9 編碼器   | 0、1、2、3、4、5 |
| Windows媒體影片7/8 編碼器 | 0、1             |



 

## <a name="remarks"></a>備註

較低的值會使編解碼器使用較不復雜的編碼演算法。 雖然更簡單的演算法會產生較低品質的輸出，但編碼程式較快，而且需要較少的處理能力。 從即時來源編碼內容時，這可能很重要，因為編碼器必須快速處理輸入，才能跟上來源的高度。

如果 [MFPKEY \_ COMPRESSIONOPTIMIZATIONTYPE](mfpkey-compressionoptimizationtypeproperty.md) 屬性設定為1，則會忽略任何指派給這個屬性的值。 在此情況下，MFPKEY \_ COMPLEXITYEX 會自動設為3。

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

 

 




