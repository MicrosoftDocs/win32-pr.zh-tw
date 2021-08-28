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
ms.openlocfilehash: bd93b21b01721be8d4be0e432f83c507762b5d76c758419ed157c85f8a0ac419
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119388138"
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
| 版本<br/> | WindowsWindows Server 2012、Windows 8 Windows Server 2008 R2 或 Windows 7 上的安裝程式5.0。 WindowsWindows Server 2008 或 Windows Vista 上的安裝程式4.0 或 Windows Installer 4.5。 WindowsWindows Server 2003 或 Windows XP 上的安裝程式<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller 定義為000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MsiEnumProducts**](/windows/desktop/api/Msi/nf-msi-msienumproductsa)
</dt> </dl>

 

 




