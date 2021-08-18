---
description: 監視器會呼叫 LoadMACAddresses 函式，以填入取自 HTML 設定字串變數之位址的 MAC 地址清單。
ms.assetid: cb7d2812-e234-4858-8b25-f8fc72aeee79
title: 'LoadMACAddresses 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LoadMACAddresses
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 2de609ef0a1e820785ee7d62cbbe1e6af32c633aa29b133974f6f5f6f2a649b9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119742718"
---
# <a name="loadmacaddresses-function"></a>LoadMACAddresses 函式

監視器會呼叫 **LoadMACAddresses** 函式，以填入取自 HTML 設定字串變數之位址的 MAC 地址清單。

## <a name="syntax"></a>語法


```C++
BOOL LoadMACAddresses(
  _In_  const char   *pConfig,
  _In_  const char   *pVarName,
  _Out_       LPBYTE *ppAddresses,
  _Out_       DWORD  *pNumAddresses
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*>-pconfig* \[在\]
</dt> <dd>

[IMonitor：:D oconfigure](imonitor-doconfigure.md)方法傳遞給監視器的 HTML 設定字串指標。

</dd> <dt>

*pVarName* \[在\]
</dt> <dd>

設定字串中變數名稱的指標。

</dd> <dt>

*ppAddresses* \[擴展\]
</dt> <dd>

指向位址陣列指標的指標。 如果找到在 *pVarName* 中指定的變數，而且其長度不是零，則此函式會使用 **HeapAllocMemory**) 配置足夠的空間 (，並將所有 MAC 位址儲存為數組。

</dd> <dt>

*pNumAddresses* \[擴展\]
</dt> <dd>

**DWORD** 變數的指標，此變數會設定為取自設定字串的 MAC 位址數目。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功， (找到變數名稱，且具有非零長度的字串，表示 MAC 位址) ，傳回值為 **TRUE**。

如果函式不成功，則傳回值為 **FALSE**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                           |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                 |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl>  |
| 程式庫<br/>                  | <dl> <dt>Nmapi .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




