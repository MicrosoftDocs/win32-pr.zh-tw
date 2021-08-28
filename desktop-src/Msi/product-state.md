---
description: State 屬性會傳回這個產品實例的安裝狀態。
ms.assetid: ae4c7a43-d4af-4e06-a3f8-d7c2d0715d84
title: Product. State 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.State
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: befa632feae7b4c57983f13a28e695051842cb5d1a2ff0908e6ffd011c6e4918
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119753948"
---
# <a name="productstate-property"></a>Product. State 屬性

**State** 屬性會傳回這個產品實例的安裝狀態。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```JScript
propVal = Product.State
```



## <a name="property-value"></a>屬性值

## <a name="remarks"></a>備註

這個屬性會傳回下列其中一個值。



| 安裝狀態       | 意義                                |
|--------------------------|----------------------------------------|
| INSTALLSTATE \_ 預設值    | 在本機安裝之產品的實例。 |
| INSTALLSTATE \_ 公告 | 已公告產品的實例。        |
| INSTALLSTATE \_ 不明    | 未知產品的實例。           |



 

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

 

 




