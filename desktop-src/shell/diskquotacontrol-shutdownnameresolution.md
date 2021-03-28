---
description: 關閉使用者名稱解析執行緒。
ms.assetid: 6c4544b9-81e7-4a72-aa00-70011e5cd85a
title: 'DiskQuotaControl. ShutdownNameResolution 方法 (Dskquota .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.ShutdownNameResolution
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 0db952a502210e509abeb527b2006eab087434e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026170"
---
# <a name="diskquotacontrolshutdownnameresolution-method"></a>DiskQuotaControl. ShutdownNameResolution 方法

關閉使用者名稱解析執行緒。

## <a name="syntax"></a>語法


```JScript
DiskQuotaControl.ShutdownNameResolution()
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

安全識別碼 (SID) 名稱解析程式會將 SID 轉譯為背景執行緒上的使用者名稱。 當相關聯的配額控制物件終結時，就會自動關閉這個執行緒。 不過，在某些情況下，已不再需要執行緒，但物件尚未準備好終結。 典型的範例是，當沒有進一步的處理時，用戶端仍會保留物件的參考。 **ShutdownNameResolution** 方法可讓您終止解析程式執行緒，並釋放相關聯的資源，而不會終結配額控制物件。

> [!Note]  
> 當您關閉解析程式執行緒時，非同步名稱解析會立即停止。 如果後續對 [**AddUser**](diskquotacontrol-adduser.md) 或 [**FindUser**](diskquotacontrol-finduser.md)等方法進行呼叫，配額物件可能會重新建立解析程式執行緒。

 

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

 

 




