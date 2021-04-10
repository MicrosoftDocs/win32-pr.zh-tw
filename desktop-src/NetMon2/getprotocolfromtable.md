---
description: GetProtocolFromTable 函式會 \# 根據指定的交付資料表和值，傳回通訊協定&郵件）的控制碼。
ms.assetid: 34b07079-0b20-40d8-a529-4179ecc68ebf
title: 'GetProtocolFromTable 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetProtocolFromTable
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 498892fc2cc5ada2e177b8fb3f70f40a1ef10dfe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936617"
---
# <a name="getprotocolfromtable-function"></a>GetProtocolFromTable 函式

**GetProtocolFromTable** 函數會根據給定的交付資料表和值，傳回通訊協定的控制碼。

## <a name="syntax"></a>語法


```C++
HPROTOCOL WINAPI GetProtocolFromTable(
  _In_  LPHANDOFFTABLE hTable,
  _In_  DWORD          ItemToFind,
  _Out_ PDWORD_PTR     lpInstData
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hTable* \[在\]
</dt> <dd>

提交資料表的控制碼。

</dd> <dt>

*ItemToFind* \[在\]
</dt> <dd>

用來在遞交資料表中尋找通訊協定的值。 此值必須可在通訊協定資料中使用。

</dd> <dt>

*lpInstData* \[擴展\]
</dt> <dd>

如果可在遞交資料表中使用，則為下一個通訊協定的實例資料。 實例資料的長度不能超過 DWORD \_ 指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為通訊協定控制碼。

如果函式不成功，則傳回值為 **Null**。

## <a name="remarks"></a>備註

在執行 [RecognizeFrame](recognizeframe.md) 匯出函式時，會使用 **GetProtocolFromTable** 函數來取得下一個通訊協定的控制碼。 如果通訊協定識別接下來的通訊協定，則會呼叫 **GetProtocolFromTable** 函式，以從下一個通訊協定取出控制碼。

**執行個體資料**

實例資料可以是小於或等於 DWORD 指標長度的任何資料，或是不需要由剖析器配置 \_ 或釋放的資料指標，例如原始框架資料。

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

[RecognizeFrame](recognizeframe.md)
</dt> </dl>

 

 




