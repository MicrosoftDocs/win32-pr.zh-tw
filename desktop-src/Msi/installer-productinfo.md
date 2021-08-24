---
description: ProductInfo 屬性是唯讀屬性，可傳回已安裝或已發佈產品的指定屬性值。
ms.assetid: 144cbba7-ec2b-44cd-acc8-868c210ccebd
title: 'ProductInfo 屬性 (Oemupgex .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ProductInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 5d04ad49fd8c1cf017131b5ded6be088e6436731b6bd97dd437060d09988d3aa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119745288"
---
# <a name="installerproductinfo-property"></a>ProductInfo 屬性

**ProductInfo** 屬性是唯讀屬性，可傳回已安裝或已發佈產品的指定屬性值。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```JScript
propVal = Installer.ProductInfo
```



## <a name="property-value"></a>屬性值

## <a name="remarks"></a>備註

**ProductInfo** 屬性 ( "LocalPackage" ) 不一定會傳回快取封裝的路徑。 不應從 LocalPackage 叫用維護模式安裝。 快取的封裝僅供內部使用。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | WindowsWindows Server 2012、Windows 8 Windows Server 2008 R2 或 Windows 7 上的安裝程式5.0。 WindowsWindows Server 2008 或 Windows Vista 上的安裝程式4.0 或 Windows Installer 4.5。 WindowsWindows Server 2003 或 Windows XP 上的安裝程式3.0 或更新版本。<br/> |
| 標頭<br/>  | <dl> <dt>Oemupgex。h</dt> </dl>                                                                                                                                                                                 |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                    |
| IID<br/>     | IID \_ IInstaller 定義為000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                                         |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MsiGetProductInfo**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoa)
</dt> <dt>

[**MsiGetUserInfo**](/windows/desktop/api/Msi/nf-msi-msigetuserinfoa)
</dt> <dt>

[Windows Installer 2.0 及更早版本不支援](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




