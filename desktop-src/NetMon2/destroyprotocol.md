---
description: DestroyProtocol 函式會終結 CreateProtocol 函數所建立的通訊協定。
ms.assetid: f7621c2a-1905-4748-b8e3-7b49f3f2bf03
title: 'DestroyProtocol 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DestroyProtocol
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: be96a13816a6a35bdd554380dacd5e8e2f5d5450
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192632"
---
# <a name="destroyprotocol-function"></a>DestroyProtocol 函式

**DestroyProtocol** 函式會終結 **CreateProtocol** 函數所建立的通訊協定。

## <a name="syntax"></a>語法


```C++
VOID WINAPI DestroyProtocol(
  _In_ HPROTOCOL hProtocol
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hProtocol* \[在\]
</dt> <dd>

要終結之通訊協定的控制碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

無。

## <a name="remarks"></a>備註

剖析器 DLL 會在其 [DllMain](dllmain-parser.md)的執行期間呼叫 **DestroyProtocol** 函數。 當作業系統即將卸載 DLL 時，會呼叫 **DestroyProtocol** 。



| 如需相關資訊                                        | 請參閱                                                     |
|-----------------------------------------------------------|---------------------------------------------------------|
| 什麼是剖析器，以及它們如何搭配網路監視器運作。 | [解析 器](parsers.md)                                  |
| 如何執行 **DllMain** 包含範例。         | [執行 DllMain](implementing-dllmain-parser.md) |



 

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

[DllMain](dllmain-parser.md)
</dt> </dl>

 

 




