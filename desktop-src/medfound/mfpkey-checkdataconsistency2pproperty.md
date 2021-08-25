---
description: 指定在執行雙向 VBR 編碼時，編碼器是否應該檢查跨行程的資料一致性。 讀寫。
ms.assetid: 68750820-e931-41c2-9d12-89ab83b4b97e
title: 'MFPKEY_CHECKDATACONSISTENCY2P 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a1cef9c8c2a8e4fcd536ce73653e80e62282b40734cc695493d6cba4187c8f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119954718"
---
# <a name="mfpkey_checkdataconsistency2p-property"></a>MFPKEY \_ CHECKDATACONSISTENCY2P 屬性

指定在執行雙向 VBR 編碼時，編碼器是否應該檢查跨行程的資料一致性。 讀寫。

## <a name="constant-for-ipropertybag"></a>IPropertyBag 的常數

僅可使用 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)。

## <a name="data-type"></a>資料類型

**VT \_ BOOL**

## <a name="default-value"></a>預設值

**VARIANT \_ TRUE**

## <a name="remarks"></a>備註

如果您將此屬性保留 **\_ 為 VARIANT TRUE** 的預設值，則編碼器會確認輸入範例在兩個階段之間相符，如果偵測到不一致，則會失敗。 導致差異的主要案例是當輸入來自裝置時。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-----------------------------------------------------------------------------------------|
| 用戶端<br/> | Windows Vista 或 Windows 7<br/>                                                   |
| 標頭<br/> | <dl> <dt>Wmcodecdsp。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎屬性](media-foundation-properties.md)
</dt> </dl>

 

 
