---
description: 傳回 RecordList 物件，這個物件會列舉產品清單。
ms.assetid: 30735b9f-091b-4915-9b07-9688c9be2d26
title: ProductsEx 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ProductsEx
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 17d5e8290ab61b85fa8269f8b23f3cdabd30e012
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992957"
---
# <a name="installerproductsex-property"></a>ProductsEx 屬性

**ProductsEx** 屬性會傳回列舉產品清單的 [**RecordList**](recordlist-object.md)物件。 這個屬性會呼叫 [**MsiEnumProductsEx**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa)。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```JScript
propVal = Installer.ProductsEx
```



## <a name="property-value"></a>屬性值

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer 3.0 或更新版本。<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                    |
| IID<br/>     | IID \_ IInstaller 定義為000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                                         |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**安裝程式**](installer-object.md)
</dt> <dt>

[**MsiEnumProductsEx**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa)
</dt> <dt>

[**產品**](product-object.md)
</dt> <dt>

[Windows Installer 2.0 及更早版本不支援](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




