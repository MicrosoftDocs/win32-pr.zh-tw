---
description: 使安全性識別碼的使用者名稱快取失效。
ms.assetid: 52f4a051-0caf-43c1-b190-c83c20e9fcf8
title: 'DiskQuotaControl. InvalidateSidNameCache 方法 (Dskquota .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.InvalidateSidNameCache
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 1a171aaaf8f3faa45f967f29bf0f9d742aa0fe0221b46ae4ba4f8527d9cf9715
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119455888"
---
# <a name="diskquotacontrolinvalidatesidnamecache-method"></a>DiskQuotaControl. InvalidateSidNameCache 方法

使安全性識別碼的使用者名稱快取失效。

## <a name="syntax"></a>語法


```JScript
DiskQuotaControl.InvalidateSidNameCache()
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

使用者名稱和相關聯的安全識別碼會儲存在快取中。 您可以藉由呼叫 **InvalidateSidNameCache** 來清除此快取。 如果您之後建立新的使用者物件，就必須從網域控制站取得資訊，而且必須重新建立快取。

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

 

 




