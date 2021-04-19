---
description: ProductState 屬性是唯讀屬性，可傳回產品的安裝狀態資訊。
ms.assetid: 9ae3bc86-aa13-41b3-b058-4037607f7dd5
title: ProductState 屬性方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ProductState
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: cdd1397def1cd25405d0a80a6d5cfde2ee6ef77e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994745"
---
# <a name="installerproductstate-property-method"></a>ProductState 屬性方法

**ProductState 屬性** 是唯讀屬性，可傳回產品的安裝狀態資訊。

## <a name="syntax"></a>語法


```JScript
Installer.ProductState Property(
  Product
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*產品* 
</dt> <dd>

指定產品的產品代碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

傳回下表所示的其中一個值。



| 安裝狀態        | Description                                      |
|---------------------------|--------------------------------------------------|
| msiInstallStateAbsent     | 已針對不同的使用者安裝產品。   |
| msiInstallStateDefault    | 已為目前使用者安裝產品。   |
| msiInstallStateAdvertised | 產品已公告但未安裝。     |
| msiInstallStateInvalidArg | 傳遞給函數的參數無效。 |
| msiInstallStateUnknown    | 這項產品未公告或安裝。 |
| msiInstallStateBadConfig  | 設定資料已損毀。               |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller 定義為000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MsiQueryProductState**](/windows/desktop/api/Msi/nf-msi-msiqueryproductstatea)
</dt> </dl>

 

 




