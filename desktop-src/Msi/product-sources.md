---
description: '[來源] 屬性會列舉產品實例的所有來源。'
ms.assetid: 26602099-d0e0-4269-91d9-82943859811a
title: Product. 來源屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.Sources
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: a82363f6a61ebb9c441dfcfeeeafe3760e63c462
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978426"
---
# <a name="productsources-property"></a>Product. 來源屬性

[ **來源** ] 屬性會列舉產品實例的所有來源。 這個屬性會呼叫 [**MsiSourceListEnumSources**](/windows/desktop/api/Msi/nf-msi-msisourcelistenumsourcesa) 並傳回字串陣列，並接受來源型別做為引數。 來源類型可以是 MSISOURCETYPE \_ NETWORK 或 MSISOURCETYPE \_ URL。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```JScript
propVal = Product.Sources
```



## <a name="property-value"></a>屬性值

要列舉的來源型別。 值可以 *msiInstallSourceTypeNetwork* (1) 或 *msiInstallSourceTypeURL* (2) 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003、Windows XP 及 Windows 2000 上的 Windows Installer 3.0 或更新版本<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID \_ IProduct 定義為000C10A0-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                          |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**產品**](product-object.md)
</dt> <dt>

[**MsiSourceListEnumSources**](/windows/desktop/api/Msi/nf-msi-msisourcelistenumsourcesa)
</dt> <dt>

[Windows Installer 2.0 及更早版本不支援](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




