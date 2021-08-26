---
description: CoNtext 屬性會傳回此產品的內容。
ms.assetid: aa772a95-eb4e-45af-9788-9833d62139e8
title: Product. CoNtext 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.Context
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 21fb23a595b1f479f2468f0006cca7cd9218de03fc2cc76b794caae79ea45a24
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129118"
---
# <a name="productcontext-property"></a>Product. CoNtext 屬性

**CoNtext** 屬性會傳回此產品的內容。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```JScript
propVal = Product.Context
```



## <a name="property-value"></a>屬性值

## <a name="remarks"></a>備註

這個屬性可能會傳回下列其中一個值。



| Context                        | 值 | 意義                           |
|--------------------------------|-------|-----------------------------------|
| MSIINSTALLCONTEXT \_ USERMANAGED | 1     | 受管理內容下的產品。   |
| MSIINSTALLCONTEXT \_ 使用者        | 2     | 非受控內容下的產品。 |
| MSIINSTALLCONTEXT \_ 機器     | 4     | 電腦內容下的產品。   |



 

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

[Windows Installer 2.0 及更早版本不支援](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




