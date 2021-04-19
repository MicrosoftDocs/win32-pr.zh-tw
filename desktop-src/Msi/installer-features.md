---
description: Features 屬性是唯讀屬性，它會傳回 StringList 物件，以列舉指定產品的已發行功能集。
ms.assetid: feb8f09a-fa97-4fee-9082-8f04288af22f
title: 安裝程式。 Features 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.Features
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 4f63ce80249fb8bd24d70f92e72c44420a13d798
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106986591"
---
# <a name="installerfeatures-property"></a>安裝程式。 Features 屬性

**Features** 屬性是唯讀屬性，它會傳回 [**StringList**](stringlist-object.md)物件，以列舉指定產品的已發行功能集。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```JScript
propVal = Installer.Features
```



## <a name="property-value"></a>屬性值

指定產品的產品代碼。

## <a name="remarks"></a>備註

若要列舉功能，應用程式會使用 For Each 結構逐一查看 [**StringList**](stringlist-object.md) 物件。 因為功能未排序，所以任何新功能都有任意的索引，這表示函式可以依任何順序傳回特徵。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller 定義為000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MsiEnumFeatures**](/windows/desktop/api/Msi/nf-msi-msienumfeaturesa)
</dt> <dt>

[系統狀態函數](installer-function-reference.md)
</dt> </dl>

 

 




