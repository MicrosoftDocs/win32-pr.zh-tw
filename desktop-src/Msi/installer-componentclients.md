---
description: 唯讀 ComponentClients 屬性會傳回 StringList 物件，以列舉指定元件的一組用戶端。
ms.assetid: 47553360-298f-4be8-819d-18f4df96667c
title: ComponentClients 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ComponentClients
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 2241babae283f367a15c8f742b51af280ed1a3b1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998410"
---
# <a name="installercomponentclients-property"></a>ComponentClients 屬性

唯讀 **ComponentClients** 屬性會傳回 [**StringList**](stringlist-object.md) 物件，以列舉指定元件的一組用戶端。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```JScript
propVal = Installer.ComponentClients
```



## <a name="property-value"></a>屬性值

字串 GUID，表示元件的元件代碼。 元件程式碼會在 [元件資料表](component-table.md)的 [元件] 資料行中指定。

## <a name="remarks"></a>備註

若要列舉元件用戶端，應用程式可以使用 For Each 結構來逐一查看 [**StringList**](stringlist-object.md) 物件。 因為不會排序用戶端，所以任何新元件都有任意的索引。 這表示函數可能會以任何順序傳回用戶端。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller 定義為000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MsiEnumClients**](/windows/desktop/api/Msi/nf-msi-msienumclientsa)
</dt> </dl>

 

 




