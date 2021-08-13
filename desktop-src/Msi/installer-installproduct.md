---
description: 安裝程式物件的 InstallProduct 方法會開啟安裝程式套件，並初始化安裝會話。
ms.assetid: 6828ca34-3cf1-4738-882d-9ff1450f1014
title: InstallProduct 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.InstallProduct
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 1605fc0f2e955d6f0364159779ae90f8f59e9ace0f3ff14a1106f7623ab7d99d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118630390"
---
# <a name="installerinstallproduct-method"></a>InstallProduct 方法

[**安裝程式**](installer-object.md)物件的 **InstallProduct** 方法會開啟安裝程式套件，並初始化安裝會話。

## <a name="syntax"></a>語法


```JScript
Installer.InstallProduct(
  packagePath,
  propertyValues
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*packagePath* 
</dt> <dd>

必要的字串，其中包含安裝套件的路徑。

</dd> <dt>

*propertyValues* 
</dt> <dd>

選擇性字串，包含以空白字元分隔的屬性 = 值配對。

若要執行系統管理安裝，請在 *propertyValues* 中包含 ACTION = ADMIN。 如需詳細資訊，請參閱 [**ACTION**](action.md) 屬性。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

若要完全移除產品，請在 *propertyValues* 中設定 REMOVE = ALL。 如需詳細資訊，請參閱 [**移除**](remove.md) 屬性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | WindowsWindows Server 2012、Windows 8 Windows Server 2008 R2 或 Windows 7 上的安裝程式5.0。 WindowsWindows Server 2008 或 Windows Vista 上的安裝程式4.0 或 Windows Installer 4.5。 WindowsWindows Server 2003 或 Windows XP 上的安裝程式<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller 定義為000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 




