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
ms.openlocfilehash: c54b9563898b093af324b02ca6a5bf48fbddf62b31c22a3d492c1132c46f13f8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119753918"
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
| 版本<br/> | WindowsWindows Server 2012、Windows 8 Windows Server 2008 R2 或 Windows 7 上的安裝程式5.0。 WindowsWindows Server 2008 或 Windows Vista 上的安裝程式4.0 或 Windows Installer 4.5。 WindowsWindows Server 2003、Windows XP 和 Windows 2000 上的安裝程式3.0 或更新版本<br/> |
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

 

 




