---
description: KEYSVCC \_ 控制碼資料類型會定義金鑰服務控制碼。 \_RKeyOpenKeyService 和 RKeyCloseKeyService 函數會使用 KEYSVCC 控制碼控制碼。
ms.assetid: d0fd5184-5c8e-4f96-9ff1-8abd6f718d05
title: 'KEYSVCC_HANDLE (Rkeysvcc) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 32e34285c6291cb7cb87aeb9095e5261b43999b0eefa82e33704719e7673f1b0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119515948"
---
# <a name="keysvcc_handle"></a>KEYSVCC \_ 控制碼

**KEYSVCC \_ 控制碼** 資料類型會定義金鑰服務控制碼。 [**RKeyOpenKeyService**](rkeyopenkeyservice.md)和 [**RKeyCloseKeyService**](rkeyclosekeyservice.md)函數會使用 **KEYSVCC \_ 句** 柄控制碼。


```C++
typedef void* KEYSVCC_HANDLE;
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                             |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Rkeysvcc。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**RKeyCloseKeyService**](rkeyclosekeyservice.md)
</dt> <dt>

[**RKeyOpenKeyService**](rkeyopenkeyservice.md)
</dt> </dl>

 

 




