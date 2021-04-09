---
description: 指定編碼傳遞的結尾。
ms.assetid: 8a7e6e09-766c-4346-8893-eea5614b2aa4
title: 'MFPKEY_ENDOFPASS 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a38e03867e11cde944bf902ae52f98cda7b8313
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848813"
---
# <a name="mfpkey_endofpass-property"></a>MFPKEY \_ ENDOFPASS 屬性

指定編碼傳遞的結尾。

## <a name="data-type"></a>資料類型

**VT \_ BOOL**

## <a name="constant-for-ipropertybag"></a>IPropertyBag 的常數

g \_ wszWMVCEndOfPass

## <a name="data-type-for-ipropertybag"></a>IPropertyBag 的資料類型

不需要任何資料類型。 若要設定這個屬性，請傳遞未初始化的 **VARIANT**。

## <a name="remarks"></a>備註

這個屬性不是一般屬性，因為不論值為 VARIANT \_ TRUE 或 variant FALSE，它都有相同的效果 \_ 。 您必須在處理前置處理傳遞的最後一個輸入範例之後設定這個屬性。 如果您正在執行多個行程，則必須在每個前置處理階段結束時設定此屬性 (目前沒有任何編解碼器支援多個) 。 如果您未設定此屬性，則編解碼器會假設您仍在傳遞範例以進行前置處理。

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

 

 




