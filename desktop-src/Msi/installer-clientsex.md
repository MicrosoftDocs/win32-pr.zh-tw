---
description: 傳回 RecordList 物件，這個物件會列出使用指定已安裝元件的產品。
ms.assetid: c9756526-68d7-4d04-97e2-56a5eaf816be
title: ClientsEx 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ClientsEx
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 5a609ab0ba6edc5b0e3e9bbd26bc3539858ebdee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989863"
---
# <a name="installerclientsex-property"></a>ClientsEx 屬性

這個屬性會傳回 [**RecordList**](recordlist-object.md) 物件，其中會列出使用指定之已安裝元件的產品。 這個屬性會呼叫 [**MsiEnumClientsEx**](/windows/desktop/api/Msi/nf-msi-msienumclientsexa)。

**[Windows Installer 4.5 或更早版本](not-supported-in-windows-installer-4-5.md)：** 不支援。 從 Windows Installer 5.0 開始，可以使用這個屬性。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```JScript
propVal = Installer.ClientsEx
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

[**MsiEnumClientsEx**](/windows/desktop/api/Msi/nf-msi-msienumclientsexa)
</dt> </dl>

 

 




