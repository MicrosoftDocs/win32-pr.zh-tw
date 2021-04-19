---
description: 如果產品是受控的，安裝程式物件的 ProductElevated 屬性會傳回 True，如果產品不受管理，則傳回 False。
ms.assetid: 8126f5a0-751f-46c3-9014-208e9c2db34c
title: 安裝程式：:P roductElevated 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ProductElevated
- Installer.get_ProductElevated
- Installer.ProductElevated
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 22591c20cbabfda2eb052e4746e87739b9681804
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976249"
---
# <a name="installerproductelevated-property"></a>安裝程式：:P roductElevated 屬性

如果產品是受控的，[**安裝程式**](installer-object.md)物件的 **ProductElevated** 屬性會傳回 True，如果產品不受管理，則傳回 False。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```JScript
propVal = Installer.ProductElevated
```



## <a name="property-value"></a>屬性值

產品的完整產品代碼 GUID。 此為必要參數。

## <a name="remarks"></a>備註

**ProductElevated** 屬性使用 [**MsiIsProductElevated**](/windows/desktop/api/Msi/nf-msi-msiisproductelevateda)函數。 傳回屬性不會考慮 [AlwaysInstallElevated](alwaysinstallelevated.md) 原則。

## <a name="examples"></a>範例

下列範例腳本示範如何使用 **ProductElevated** 屬性。


```VB
Dim installer
Set installer = CreateObject("WindowsInstaller.Installer")

' 
' Install Orca tool per-machine
'
installer.InstallProduct "\\products\public\orca\orca.msi", "ALLUSERS=1"

'
' Verify Orca is managed
'

Dim bManaged
bManaged = installer.ProductElevated("{85F4CBCB-9BBC-4B50-A7D8-E1106771498D}")

If bManaged Then
    MsgBox "Success - Product Is Managed"
Else
    MsgBox "Failure - Product Is Not Managed"
End If
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

 

 




