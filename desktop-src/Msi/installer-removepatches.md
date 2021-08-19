---
description: RemovePatches 方法會移除有資格接收修補程式的一或多個產品修補程式。 RemovePatches 方法會呼叫 MsiRemovePatches。
ms.assetid: 09c6ad3a-9f5e-4f9a-82c8-be7e411efd60
title: RemovePatches 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.RemovePatches
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: bfa316b4ff01f6e5667b3fb2c5fce2333c4b4aaf34dc5a1dbb37feb61d1a9ce4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894028"
---
# <a name="installerremovepatches-method"></a>RemovePatches 方法

**RemovePatches** 方法會移除有資格接收修補程式的一或多個產品修補程式。 **RemovePatches** 方法會呼叫 [**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa)。

## <a name="syntax"></a>語法


```JScript
Installer.RemovePatches(
  PatchList,
  ProductCode,
  UninstallType,
  PropertyList
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*PatchList* 
</dt> <dd>

字串，包含要移除的修補程式清單（以分號分隔）。 每個修補程式都可以用修補封裝的完整路徑或 patch GUID 來表示。 此為必要參數。

</dd> <dt>

*ProductCode* 
</dt> <dd>

字串，其中包含要從中移除修補程式之產品的 GUID。 此為必要參數。

</dd> <dt>

*UninstallType* 
</dt> <dd>

指定修補程式移除類型的整數值。 此參數必須是 **msiInstallTypeSingleInstance**。

</dd> <dt>

*PropertyList* 
</dt> <dd>

字串，指定要包含的屬性 = 值配對。 這是選擇性參數。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

請參閱 [卸載修補](uninstalling-patches.md) 程式以取得示範應用程式如何從使用者可用的所有產品中移除修補程式的範例。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | WindowsWindows Server 2012、Windows 8 Windows Server 2008 R2 或 Windows 7 上的安裝程式5.0。 WindowsWindows Server 2008 或 Windows Vista 上的安裝程式4.0 或 Windows Installer 4.5。 WindowsWindows Server 2003 或 Windows XP 上的安裝程式3.0 或更新版本。<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                    |
| IID<br/>     | IID \_ IInstaller 定義為000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                                         |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ProductCode**](productcode.md)
</dt> <dt>

[**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa)
</dt> <dt>

[卸載修補程式](uninstalling-patches.md)
</dt> <dt>

[Windows Installer 2.0 及更早版本不支援](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




