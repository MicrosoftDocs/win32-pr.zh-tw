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
ms.openlocfilehash: cafff03a392fc1977fd19b5b8415ca499d614c2c4ba3fb4f7104edd5344f3a86
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118630590"
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
| 版本<br/> | WindowsWindows Server 2012、Windows 8 Windows Server 2008 R2 或 Windows 7 上的安裝程式5.0。 WindowsWindows Server 2008 或 Windows Vista 上的安裝程式4.0 或 Windows Installer 4.5。 WindowsWindows Server 2003 或 Windows XP 上的安裝程式<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller 定義為000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MsiSourceListForceResolution**](/windows/desktop/api/Msi/nf-msi-msisourcelistforceresolutiona)
</dt> <dt>

[來源復原](source-resiliency.md)
</dt> </dl>

 

 




