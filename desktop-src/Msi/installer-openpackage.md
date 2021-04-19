---
description: 安裝程式物件的 OpenPackage 方法會開啟安裝程式封裝，以搭配存取產品資料庫和安裝引擎的函式使用，以傳回會話物件。
ms.assetid: 22b03bde-29ae-4dd4-a41c-d55b3a4f424c
title: OpenPackage 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.OpenPackage
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 621fac51155b2ac89eba40d39da6d5af6c305e67
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989260"
---
# <a name="installeropenpackage-method"></a>OpenPackage 方法

[**安裝程式**](installer-object.md)物件的 **OpenPackage** 方法會開啟安裝程式封裝，以搭配存取產品資料庫和安裝引擎的函式使用，以傳回 [**會話**](session-object.md)物件。

## <a name="syntax"></a>語法


```JScript
Installer.OpenPackage(
  packagePath,
  options
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*packagePath* 
</dt> <dd>

必要的字串，其中包含封裝的路徑名稱。

</dd> <dt>

*options* 
</dt> <dd>

選擇性的整數值，指定當建立會話物件時， **OpenPackage** 是否應該忽略目前的電腦狀態。 如果選項預設為原始行為，則沒有值或0值。 當選項為1時， **OpenPackage** 方法會在開啟封裝時忽略目前的電腦狀態。 值為1時，可防止變更目前的電腦狀態。 如需詳細資訊，請參閱 [**MsiOpenPackageEx**](/windows/desktop/api/Msi/nf-msi-msiopenpackageexa)。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

**OpenPackage** 方法可以直接接受資料庫控制碼，而不是封裝路徑的字串。

請注意，單一進程只能開啟一個 [**會話**](session-object.md) 物件。 **OpenPackage** 不能用在自訂動作中，因為使用中的安裝是唯一允許的會話。

安全 [**會話**](session-object.md) 物件會在開啟封裝時忽略目前的電腦狀態，並防止變更目前的電腦狀態。 如需詳細資訊，請參閱 [**MsiOpenPackageEx**](/windows/desktop/api/Msi/nf-msi-msiopenpackageexa)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller 定義為000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 




