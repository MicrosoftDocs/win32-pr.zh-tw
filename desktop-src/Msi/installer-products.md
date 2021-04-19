---
description: Products 屬性是唯讀屬性，它會傳回 StringList 物件，以列舉針對目前使用者和電腦安裝或公告的所有產品集。
ms.assetid: 5c210827-a7cc-4358-bfe6-4d8e9767bd8c
title: 安裝程式. Products 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.Products
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 8d5b20a770154382e7e7a68cc3fe4d81c350fb1f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992930"
---
# <a name="installerproducts-property"></a>安裝程式. Products 屬性

**Products** 屬性是唯讀屬性，它會傳回 [**StringList**](stringlist-object.md)物件，以列舉針對目前使用者和電腦安裝或公告的所有產品集。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```JScript
propVal = Installer.Products
```



## <a name="property-value"></a>屬性值

## <a name="remarks"></a>備註

若要列舉產品，應用程式會使用 For Each 結構逐一查看 [**StringList**](stringlist-object.md) 物件。 由於產品未排序，因此任何新產品都有任意的索引。 這表示函數可以依任何順序傳回產品。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller 定義為000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MsiEnumProducts**](/windows/desktop/api/Msi/nf-msi-msienumproductsa)
</dt> </dl>

 

 




