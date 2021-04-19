---
description: 安裝程式物件的 ForceSourceListResolution 方法會強制 Windows Installer 在來源清單中搜尋有效的產品來源。
ms.assetid: d5097331-8cf5-494f-9e88-bcffcad3fe5d
title: ForceSourceListResolution 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ForceSourceListResolution
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: cadc27f3eaa90cd6fb2729f73d07cbcfa1f96b73
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106988257"
---
# <a name="installerforcesourcelistresolution-method"></a>ForceSourceListResolution 方法

[**安裝程式**](installer-object.md)物件的 **ForceSourceListResolution** 方法會強制安裝程式在下次需要來源時于來源清單中搜尋有效的產品來源，例如，當安裝程式執行安裝或重新安裝時，或需要將元件的路徑設定為從來源執行時。

## <a name="syntax"></a>語法


```JScript
Installer.ForceSourceListResolution(
  Product,
  User
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

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller 定義為000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MsiSourceListForceResolution**](/windows/desktop/api/Msi/nf-msi-msisourcelistforceresolutiona)
</dt> <dt>

[來源復原](source-resiliency.md)
</dt> </dl>

 

 




