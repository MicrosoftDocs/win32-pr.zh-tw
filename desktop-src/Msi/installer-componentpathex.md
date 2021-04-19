---
description: 傳回 RecordList 物件，這個物件會提供指定已安裝元件的完整路徑。
ms.assetid: 0f4f9d21-f1cc-44fd-a22f-1b6f055fef9e
title: ComponentPathEx 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ComponentPathEx
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: b7bf98dd8e7a81a0dd261f22a565bec8298a86a1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977558"
---
# <a name="installercomponentpathex-property"></a>ComponentPathEx 屬性

這個屬性會傳回 [**RecordList**](recordlist-object.md) 物件，該物件會提供指定已安裝元件的完整路徑。 這個屬性會呼叫 [**MsiGetComponentPathEx**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpathexa)。

**[Windows Installer 4.5 或更早版本](not-supported-in-windows-installer-4-5.md)：** 不支援。 從 Windows Installer 5.0 開始，可以使用這個屬性。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```JScript
propVal = Installer.ComponentPathEx
```



## <a name="property-value"></a>屬性值

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5。0<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                      |
| IID<br/>     | IID \_ IInstaller 定義為000C1090-0000-0000-C000-000000000046<br/>                           |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MsiGetComponentPathEx**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpathexa)
</dt> </dl>

 

 




