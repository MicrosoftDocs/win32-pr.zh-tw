---
description: 將指定的使用者物件放在行中，以進行名稱解析。
ms.assetid: 4c75f966-2e7d-4415-b1db-c98f8bdd4ce3
title: 'DiskQuotaControl. GiveUserNameResolutionPriority 方法 (Dskquota .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.GiveUserNameResolutionPriority
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 1acf50e0cec59a7ee14fbd9d7760fb68b27c4de5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511039"
---
# <a name="diskquotacontrolgiveusernameresolutionpriority-method"></a>DiskQuotaControl. GiveUserNameResolutionPriority 方法

將指定的使用者物件放在行中，以進行名稱解析。

## <a name="syntax"></a>語法


```JScript
DiskQuotaControl.GiveUserNameResolutionPriority(
  oUser
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*oUser* 
</dt> <dd>

Type： **Object**

評估為使用者 [**DIDiskQuotaUser**](didiskquotauser-object.md) 物件的物件運算式。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

如果已啟用非同步名稱解析，則使用者物件會放置在佇列中。 依預設，系統會依其放置在佇列中的順序來提供服務。 **GiveUserNameResolutionPriority** 方法會將物件移至佇列前端，讓它成為要服務的下一個。

您可以使用 [**UserNameResolution**](diskquotacontrol-usernameresolution.md) 屬性來啟用非同步名稱解析。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>Dskquota。h</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (5.0 版或更新版本) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**DiskQuotaControl 物件**](diskquotacontrol-object.md)
</dt> </dl>

 

 




