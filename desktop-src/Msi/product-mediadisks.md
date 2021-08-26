---
description: MediaDisks 屬性會列舉此產品實例的所有媒體磁片。 這個屬性會呼叫 MsiSourceListEnumMediaDisks。 以記錄物件的陣列形式傳回磁片資訊。
ms.assetid: 9ea7c9a8-4ff1-4b26-a8d5-c23510650566
title: MediaDisks 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.MediaDisks
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 00496739c9e51b5a735bf57788cdc47be0c41e177201ef445f58ea3748fb062f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120042198"
---
# <a name="productmediadisks-property"></a>MediaDisks 屬性

**MediaDisks** 屬性會列舉此產品實例的所有媒體磁片。 這個屬性會呼叫 [**MsiSourceListEnumMediaDisks**](/windows/desktop/api/Msi/nf-msi-msisourcelistenummediadisksa)。 以 [**記錄**](record-object.md) 物件的陣列形式傳回磁片資訊。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```JScript
propVal = Product.MediaDisks
```



## <a name="property-value"></a>屬性值

## <a name="remarks"></a>備註

在每一筆記錄中，第一個欄位包含磁片識別碼、第二個欄位包含磁片區標籤，而第三個欄位包含為磁片註冊的磁片提示。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | WindowsWindows Server 2012、Windows 8 Windows Server 2008 R2 或 Windows 7 上的安裝程式5.0。 WindowsWindows Server 2008 或 Windows Vista 上的安裝程式4.0 或 Windows Installer 4.5。 WindowsWindows Server 2003、Windows XP 和 Windows 2000 上的安裝程式3.0 或更新版本<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID \_ IProduct 定義為000C10A0-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                          |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**產品**](product-object.md)
</dt> <dt>

[**MsiSourceListEnumMediaDisks**](/windows/desktop/api/Msi/nf-msi-msisourcelistenummediadisksa)
</dt> <dt>

[Windows Installer 2.0 及更早版本不支援](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




