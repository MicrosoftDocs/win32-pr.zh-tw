---
description: 不支援 RKeyCloseKeyService 函數。
ms.assetid: 3a3d41d4-d8ce-4ed8-a70b-dd3629ab7b44
title: 'RKeyCloseKeyService 函式 (Rkeysvcc) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RKeyCloseKeyService
api_type:
- HeaderDef
api_location:
- Rkeysvcc.h
ms.openlocfilehash: 3a35362876c067de011ec69a858e20150308cbd4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848043"
---
# <a name="rkeyclosekeyservice-function"></a>RKeyCloseKeyService 函式

不支援 **RKeyCloseKeyService** 函數。

**Windows Server 2003：****RKeyCloseKeyService** 函式會關閉先前呼叫 [**RKeyOpenKeyService**](rkeyopenkeyservice.md)函式所開啟的金鑰服務控制碼。 請注意，此行為已隨著 Windows Server 2003 Service Pack 1 (SP1) 而變更。

## <a name="syntax"></a>語法


```C++
ULONG RKeyCloseKeyService(
  _In_    KEYSVCC_HANDLE hKeySvcCli,
  _Inout_ void           *pReserved
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hKeySvcCli* \[在\]
</dt> <dd>

[**RKeyOpenKeyService**](rkeyopenkeyservice.md)先前開啟的 [**KEYSVCC \_ 句**](keysvcc-handle.md)柄控制碼。 此值不可以是 **Null**。

</dd> <dt>

*保留* \[in、out\]
</dt> <dd>

保留的。 將此值設定為 **Null**。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為 S \_ OK。

如果函式失敗，則傳回值為 **ULONG** ，表示錯誤。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                             |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Rkeysvcc。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**RKeyOpenKeyService**](rkeyopenkeyservice.md)
</dt> <dt>

[**RKeyPFXInstall**](rkeypfxinstall.md)
</dt> </dl>

 

 




