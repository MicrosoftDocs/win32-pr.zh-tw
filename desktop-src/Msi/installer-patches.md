---
description: 安裝程式物件的唯讀修補程式屬性會傳回 StringList 物件，其中包含套用至產品的所有修補程式。
ms.assetid: a8d46073-399b-480e-b4b0-a7a2f832e160
title: 安裝程式. 修補程式屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.Patches
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 33576b92924493a99c058196639faa34f5b42e388b9e30b6e300c17444ddeeff
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119430778"
---
# <a name="installerpatches-property"></a>安裝程式. 修補程式屬性

[**安裝程式**](installer-object.md)物件的唯讀 **修補** 程式屬性會傳回 [**StringList**](stringlist-object.md)物件，其中包含套用至產品的所有修補程式。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```JScript
propVal = Installer.Patches
```



## <a name="property-value"></a>屬性值

指定產品代碼。

## <a name="remarks"></a>備註

若要列舉修補程式，應用程式會使用 For Each 結構逐一查看 [**StringList**](stringlist-object.md) 物件。 因為修補程式未排序，所以任何新的修補程式都有任意的索引。 這表示函數可以依任何順序傳回修補程式。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | WindowsWindows Server 2012、Windows 8 Windows Server 2008 R2 或 Windows 7 上的安裝程式5.0。 WindowsWindows Server 2008 或 Windows Vista 上的安裝程式4.0 或 Windows Installer 4.5。 WindowsWindows Server 2003 或 Windows XP 上的安裝程式<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller 定義為000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MsiEnumPatches**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddmediadiska)
</dt> </dl>

 

 




