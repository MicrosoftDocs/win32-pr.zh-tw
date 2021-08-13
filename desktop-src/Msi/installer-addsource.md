---
description: 安裝程式物件的 AddSource 方法會將來源新增至 sourcelist 中有效網路來源的清單。
ms.assetid: e24c8484-fe84-4f97-9c06-c063bb7c6810
title: AddSource 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.AddSource
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 8c5e2b87a1fc9a660ae835d9fb1cfa465673bb6698144a9695cbfb264535a948
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118633162"
---
# <a name="installeraddsource-method"></a>AddSource 方法

[**安裝程式**](installer-object.md)物件的 **AddSource** 方法會將來源新增至 sourcelist 中有效網路來源的清單。

## <a name="syntax"></a>語法


```JScript
Installer.AddSource(
  Product,
  User,
  Source
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*產品* 
</dt> <dd>

指定產品代碼。

</dd> <dt>

*使用者* 
</dt> <dd>

每個使用者安裝的使用者名稱;每一電腦安裝都是 null 或空字串。

</dd> <dt>

*來源* 
</dt> <dd>

指定來源之字串的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | WindowsWindows Server 2012、Windows 8 Windows Server 2008 R2 或 Windows 7 上的安裝程式5.0。 WindowsWindows Server 2008 或 Windows Vista 上的安裝程式4.0 或 Windows Installer 4.5。 WindowsWindows Server 2003 或 Windows XP 上的安裝程式<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller 定義為000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MsiSourceListAddSource**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourcea)
</dt> <dt>

[來源復原](source-resiliency.md)
</dt> </dl>

 

 




