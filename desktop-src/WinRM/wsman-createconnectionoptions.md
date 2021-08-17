---
title: 'CreateConnectionOptions 方法 (WSManDisp .h) '
description: 建立 ConnectionOptions 物件，這個物件會指定建立會話時使用的使用者名稱和密碼。
ms.assetid: 3669a5fe-8305-4fa3-aa75-fafefcd8b33d
ms.tgt_platform: multiple
keywords:
- CreateConnectionOptions 方法 Windows 遠端管理
- CreateConnectionOptions 方法 Windows 遠端管理，WSMan 物件
- WSMan 物件 Windows 遠端管理，CreateConnectionOptions 方法
topic_type:
- apiref
api_name:
- WSMan.CreateConnectionOptions
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a4bd1218fcf6ca228cbc7538434b00b7b4e80d4c5b2df54807e031c11c14f99
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117742665"
---
# <a name="wsmancreateconnectionoptions-method"></a>WSMan. CreateConnectionOptions 方法

建立 [**ConnectionOptions**](connectionoptions.md) 物件，這個物件會指定建立會話時使用的使用者名稱和密碼。

## <a name="syntax"></a>語法


```VB
WSMan.CreateConnectionOptions()
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

用來指定使用者名稱和密碼組的 [**ConnectionOptions**](connectionoptions.md) 物件，用來識別要驗證的使用者。

## <a name="remarks"></a>備註

下列語法用來呼叫這個方法。


```VB
Set options = wsman.CreateConnectionOptions
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                 |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                           |
| 標頭<br/>                   | <dl> <dt>WSManDisp。h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WSManDisp .idl</dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>WSManDisp .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**WSMan**](wsman.md)
</dt> <dt>

[**ConnectionOptions**](connectionoptions.md)
</dt> </dl>

 

 





