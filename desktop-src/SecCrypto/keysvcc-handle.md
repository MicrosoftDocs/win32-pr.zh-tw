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
ms.openlocfilehash: 1427a4ffd4637e073e517e5df54af72191992d11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106983834"
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
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Rkeysvcc。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**RKeyCloseKeyService**](rkeyclosekeyservice.md)
</dt> <dt>

[**RKeyOpenKeyService**](rkeyopenkeyservice.md)
</dt> </dl>

 

 




