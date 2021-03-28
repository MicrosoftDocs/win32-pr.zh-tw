---
description: 當已解析 DIDiskQuotaUser 物件的名稱資訊時發生。
ms.assetid: df32cb17-ad90-4535-a36b-60c5b4e9999f
title: 'OnUserNameChanged 函式 (Dskquota) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OnUserNameChanged
api_type:
- DllExport
api_location:
- Shell32.dll
ms.openlocfilehash: 98906f281c6c93a64754c1aa5cecfc6624599c40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319551"
---
# <a name="onusernamechanged-function"></a>OnUserNameChanged 函式

當已解析 [**DIDiskQuotaUser**](didiskquotauser-object.md) 物件的名稱資訊時發生。

## <a name="parameters"></a>參數

<dl> <dt>

*oUser* 
</dt> <dd>

物件，該 **物件** 會評估為與已解析其名稱之使用者相關聯的 [**DIDiskQuotaUser**](didiskquotauser-object.md) 物件。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="remarks"></a>備註

當用戶端 [**列舉使用者**](didiskquotauser-object.md)或呼叫 [**AddUser**](diskquotacontrol-adduser.md) 或 [**FindUser**](diskquotacontrol-finduser.md) 方法時，必須將使用者名稱解析為相關聯的安全識別碼 (SID) 。 因為這個程式可能很耗時，所以用戶端可以在背景執行緒上以非同步方式進行名稱解析。 當使用者的名稱解析時， [**DiskQuotaControl**](diskquotacontrol-object.md) 物件會引發 **OnUserNameChanged** 事件來通知其用戶端。 與使用者相關聯的 **DIDiskQuotaUser** 物件會以參數形式傳遞。 此物件可讓用戶端修改使用者的配額設定。

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

 

 




