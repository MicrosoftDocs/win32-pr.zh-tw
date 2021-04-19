---
description: MediaDisks 屬性會列舉此產品實例的所有媒體磁片。 這個屬性會呼叫 MsiSourceListEnumMediaDisks。 以記錄物件的陣列形式傳回磁片資訊。
ms.assetid: 02faf211-16c8-4d2f-b192-c2ce8f3f2c66
title: MediaDisks 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.MediaDisks
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 40353ecce95cb0c4eb69228b004623bbb87c904e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992141"
---
# <a name="patchmediadisks-property"></a>MediaDisks 屬性

**MediaDisks** 屬性會列舉此產品實例的所有媒體磁片。 這個屬性會呼叫 [**MsiSourceListEnumMediaDisks**](/windows/desktop/api/Msi/nf-msi-msisourcelistenummediadisksa)。 以 [**記錄**](record-object.md) 物件的陣列形式傳回磁片資訊。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```JScript
propVal = Patch.MediaDisks
```



## <a name="property-value"></a>屬性值

## <a name="remarks"></a>備註

在每個記錄中，第一個欄位包含磁片識別碼，第二個欄位包含磁片區標籤，而第三個欄位包含為磁片註冊的磁片提示。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003、Windows XP 及 Windows 2000 上的 Windows Installer 3.0 或更新版本<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID \_ IPatch 定義為000C10A1-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                            |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Patch**](patch-object.md)
</dt> <dt>

[**MsiSourceListEnumMediaDisks**](/windows/desktop/api/Msi/nf-msi-msisourcelistenummediadisksa)
</dt> <dt>

[**Record**](record-object.md)
</dt> <dt>

[Windows Installer 2.0 及更早版本不支援](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




