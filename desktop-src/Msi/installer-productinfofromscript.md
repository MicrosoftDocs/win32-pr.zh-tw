---
description: 安裝程式物件的 ProductInfoFromScript 屬性會傳回儲存在公告腳本中指定之屬性的值。
ms.assetid: 92aa479b-2b4c-482c-a186-a290461bc6d8
title: 安裝程式：:P roductInfoFromScript 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ProductInfoFromScript
- Installer.put_ProductInfoFromScript
- Installer.ProductInfoFromScript
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: a4c8e29adb93f68228008770a95ad9fb9185e966
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995967"
---
# <a name="installerproductinfofromscript-property"></a>安裝程式：:P roductInfoFromScript 屬性

[**安裝程式**](installer-object.md)物件的 **ProductInfoFromScript** 屬性會傳回儲存在公告腳本中指定之屬性的值。

此屬性是唯寫的。

## <a name="syntax"></a>Syntax


```JScript
Installer.ProductInfoFromScript = propVal 
```



## <a name="property-value"></a>屬性值

## <a name="error-codes"></a>錯誤碼

根據要求的屬性而定的字串或整數值。

## <a name="remarks"></a>備註

**ProductInfoFromScript** 屬性使用 [**MsiGetProductInfoFromScript**](/windows/desktop/api/Msi/nf-msi-msigetproductinfofromscripta)函數。

## <a name="examples"></a>範例

下列範例腳本示範如何使用 **ProductInfoFromScript** 屬性。


```VB
Dim installer
Set installer = CreateObject("WindowsInstaller.Installer")

' 
' Create an advertise script for Orca
'

installer.CreateAdvertiseScript "\\products\public\orca\orca.msi", "c:\scratch\orca.aas"

' 
' Output ProductName Information From Script
'

MsgBox  installer.ProductInfoFromScript("c:\scratch\orca.aas", 3)
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 和 Windows XP 上的 Windows Installer 4。5<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                           |
| IID<br/>     | IID \_ IInstaller 定義為000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                                |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**安裝程式**](installer-object.md)
</dt> <dt>

[Windows Installer 3.1 及更早版本不支援](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




