---
description: 安裝程式物件的 UseFeature 方法會遞增特定功能的使用計數，並傳回該功能的安裝狀態。 這個方法應該用來表示應用程式使用功能的意圖。
ms.assetid: c9ea812c-2f95-4ba4-ad8e-b96f7fc14bb1
title: UseFeature 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.UseFeature
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 355e7f4e64a5cb69ffc0371473cb0db1ac6313a7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001932"
---
# <a name="installerusefeature-method"></a>UseFeature 方法

[**安裝程式**](installer-object.md)物件的 **UseFeature** 方法會遞增特定功能的使用計數，並傳回該功能的安裝狀態。 這個方法應該用來表示應用程式使用功能的意圖。

## <a name="syntax"></a>語法


```JScript
Installer.UseFeature(
  Product,
  Feature,
  InstallMode
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*產品* 
</dt> <dd>

指定產品的產品代碼。

</dd> <dt>

*功能* 
</dt> <dd>

識別要使用的功能。

</dd> <dt>

*InstallMode* 
</dt> <dd>

此參數必須是 *msiInstallModeNoDetection*。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

**UseFeature** 方法只能用於已知要發行的功能。 應用程式應該藉由呼叫 [**FeatureState**](installer-featurestate.md) 屬性或 [**功能**](installer-features.md) 屬性或其對等 API 來判斷功能的狀態。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller 定義為000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MsiUseFeatureEx**](/windows/desktop/api/Msi/nf-msi-msiusefeatureexa)
</dt> </dl>

 

 




