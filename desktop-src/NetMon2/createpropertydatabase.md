---
description: CreatePropertyDatabase 函數會建立一個屬性資料庫來儲存通訊協定的屬性。
ms.assetid: 0a3be6ae-d7ce-4315-b4f2-b46bcfa25b69
title: 'CreatePropertyDatabase 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreatePropertyDatabase
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 7c07f6f3e4569c06f0b3890e3ef3a26bca10b3272849fc005dfb3be6cbc2836b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118367215"
---
# <a name="createpropertydatabase-function"></a>CreatePropertyDatabase 函式

**CreatePropertyDatabase** 函數會建立一個屬性資料庫來儲存通訊協定的屬性。

## <a name="syntax"></a>語法


```C++
DWORD WINAPI CreatePropertyDatabase(
  _In_ HPROTOCOL hProtocol,
  _In_ DWORD     nProperties
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hProtocol* \[在\]
</dt> <dd>

與資料庫相關聯之通訊協定的控制碼。 當網路監視器呼叫 [Register](register-parser.md) 函數時，網路監視器會將通訊協定控制碼傳遞給剖析器 DLL。

</dd> <dt>

*nProperties* \[在\]
</dt> <dd>

儲存在資料庫中的屬性數目。 將此參數設定為通訊協定支援的屬性數目。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為 NMERR \_ SUCCESS。

如果函式不成功，則傳回值為錯誤碼。



| 傳回碼                                                                                             | Description                                                                    |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ 內部 \_ 錯誤**</dt> </dl>   | 發生內部錯誤。<br/>                                     |
| <dl> <dt>**NMERR \_ 不正確 \_ HPOTOCOL**</dt> </dl> | *HProtocol* 中指定之通訊協定的控制碼無效。<br/>     |
| <dl> <dt>**NMERR \_ \_ 記憶體不足 \_**</dt> </dl>   | 網路監視器沒有足夠的記憶體來建立資料庫。<br/> |



 

## <a name="remarks"></a>備註

只有在執行 [Register](register-parser.md)函數時，才應該呼叫 **CreatePropertyDatabase** 函數。 剖析器會使用 **CreatePropertyDatabase** 來建立描述通訊協定屬性的屬性資料庫。 網路監視器會使用資料庫來解讀通訊協定內的資訊。

**CreatePropertyDatabase** 函數會配置網路監視器需要維護屬性資料庫的結構。

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

[註冊](register-parser.md)
</dt> </dl>

 

 




