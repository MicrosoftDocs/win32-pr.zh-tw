---
description: LoadIPXAddresses 函式會由監視器呼叫，以填入取自 HTML 設定字串變數的 IPX 地址清單。
ms.assetid: d8ffd00b-2741-49e8-a90d-d41e56ee7101
title: 'LoadIPXAddresses 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LoadIPXAddresses
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: ed8bb6948102e8d28150edf102fa261c9c7f7adfcf105e377352054304b352df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119677308"
---
# <a name="loadipxaddresses-function"></a>LoadIPXAddresses 函式

**LoadIPXAddresses** 函式會由監視器呼叫，以填入取自 HTML 設定字串變數的 IPX 地址清單。

## <a name="syntax"></a>語法


```C++
BOOL LoadIPXAddresses(
  _In_  const char        *pConfig,
  _In_  const char        *pVarName,
  _Out_       IPX_ADDRESS **ppAddresses,
  _Out_       DWORD       *pNumAddresses
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

指向位址陣列指標的指標。 如果找到在 *pVarName* 中指定的變數，且具有非零長度的，則會使用 **HeapAllocMemory**) 來配置 (的足夠空間，而且所有的 IPX 位址都會儲存為數組。

</dd> <dt>

*pNumAddresses* \[擴展\]
</dt> <dd>

**DWORD** 變數的指標，此變數會設定為取自設定字串的 IPX 位址數目。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功 (已找到變數名稱，且有非零長度的字串表示) 的 IPX 位址，則傳回值為 **TRUE**。

如果函式不成功，則傳回值為 **FALSE**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                           |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                 |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl>  |
| 程式庫<br/>                  | <dl> <dt>Nmapi .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




