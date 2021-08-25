---
description: SourceListClearAll 方法，Product 物件會移除產品的所有來源。 您可以指定要移除的來源型別。
ms.assetid: c8a63b54-7be6-424a-8653-0182b561faab
title: SourceListClearAll 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.SourceListClearAll
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 8718522de7395a4fc6811e210fac0ee7b9f7758f6ea4b632f9fec122ffd5be3b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119925876"
---
# <a name="productsourcelistclearall-method"></a>SourceListClearAll 方法

**SourceListClearAll** 方法， [**product**](product-object.md)物件會移除產品的所有來源。 您可以指定要移除的來源型別。

## <a name="syntax"></a>語法


```JScript
Product.SourceListClearAll(
  Type
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*類型* 
</dt> <dd>

要移除的來源類型： MSISOURCETYPE \_ MEDIA、MSISOURCETYPE \_ NETWORK 或 MSISOURCETYPE \_ URL。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

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

[**MsiSourceListClearSource**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearsourcea)
</dt> <dt>

[Windows Installer 2.0 及更早版本不支援](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




