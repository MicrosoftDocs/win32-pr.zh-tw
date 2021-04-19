---
description: 唯讀 RelatedProducts 屬性會傳回 StringList 物件，以列舉其屬性工作表中具有指定 UpgradeCode 屬性之目前使用者和電腦的所有已安裝或公告的產品集合。
ms.assetid: 0316e536-ccd4-4d7a-9c49-66e6c4a07f1c
title: RelatedProducts 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.RelatedProducts
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: fb30be6ea5250a90ef8aa18065e9be679946e503
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978473"
---
# <a name="installerrelatedproducts-property"></a>RelatedProducts 屬性

唯讀 **RelatedProducts** 屬性會傳回 [**StringList**](stringlist-object.md)物件，以列舉其 [屬性工作表](property-table.md)中具有指定 [**UpgradeCode**](upgradecode.md)屬性之目前使用者和電腦的所有已安裝或公告的產品集合。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```JScript
propVal = Installer.RelatedProducts
```



## <a name="property-value"></a>屬性值

安裝程式所列舉之相關產品的升級程式碼。

## <a name="remarks"></a>備註

若要列舉相關的產品，應用程式會使用 For Each 結構逐一查看 [**StringList**](stringlist-object.md) 。 由於相關產品未排序，因此任何新的相關產品都有任意的索引。 這表示函數可以依任何順序傳回相關的產品。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller 定義為000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MsiEnumRelatedProducts**](/windows/desktop/api/Msi/nf-msi-msienumrelatedproductsa)
</dt> </dl>

 

 




