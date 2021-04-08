---
description: DestroyPropertyDatabase 函式會釋放用來建立通訊協定屬性資料庫的資源。
ms.assetid: a0d1c416-8b08-47ca-a88e-e70588574376
title: 'DestroyPropertyDatabase 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DestroyPropertyDatabase
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: baedae22e948b38d9ff162942269ac4529896826
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945135"
---
# <a name="destroypropertydatabase-function"></a>DestroyPropertyDatabase 函式

**DestroyPropertyDatabase** 函式會釋放用來建立通訊協定 [*屬性資料庫*](p.md)的資源。

## <a name="syntax"></a>語法


```C++
DWORD WINAPI DestroyPropertyDatabase(
  _In_ HPROTOCOL hProtocol
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hProtocol* \[在\]
</dt> <dd>

要終結之屬性資料庫的控制碼。 當網路監視器呼叫取消 [註冊](deregister.md) 函式時，會將控制碼傳遞給剖析器 DLL。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為 NMERR \_ SUCCESS。

如果函式不成功，則傳回值為錯誤碼。



| 傳回碼                                                                                              | Description                                |
|----------------------------------------------------------------------------------------------------------|--------------------------------------------|
| <dl> <dt>**NMERR \_ 內部 \_ 錯誤**</dt> </dl>    | 發生內部錯誤。 <br/>    |
| <dl> <dt>**NMERR \_ 不正確 \_ HPROTOCOL**</dt> </dl> | *HProtocol* 中的控制碼無效。 <br/> |



 

## <a name="remarks"></a>備註

只有在為通訊協定執行取消 [註冊](deregister.md)匯出函數時，才應該呼叫 **DestroyPropertyDatabase** 函式。 針對支援多個通訊協定的剖析器 Dll，會針對每個取消 **註冊** 的執行呼叫 **DestroyPropertyDatabase** 函數。



| 如需相關資訊                                        | 請參閱                                                    |
|-----------------------------------------------------------|--------------------------------------------------------|
| 什麼是剖析器，以及它們如何搭配網路監視器運作。 | [解析 器](parsers.md)                                 |
| 剖析器 DLL 中包含的進入點。        | [剖析器 DLL 架構](parser-dll-architecture.md) |
| 如何執行取消 **註冊**  包含範例。     | [執行取消註冊](implementing-deregister.md) |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                           |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                 |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl>  |
| 程式庫<br/>                  | <dl> <dt>Nmapi .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[取消註冊](deregister.md)
</dt> </dl>

 

 




