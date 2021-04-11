---
description: CreateNPPInterface 函式會使用 finder 傳回的 BLOB 來建立應用程式可使用的 NPP。
ms.assetid: 41f48c72-3284-4ebc-baff-63553c8971e6
title: 'CreateNPPInterface 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateNPPInterface
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: d0efa1c33dd5e0778f13ddd59290de324c92e813
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944523"
---
# <a name="createnppinterface-function"></a>CreateNPPInterface 函式

**CreateNPPInterface** 函式會使用 finder 傳回的 BLOB 來建立應用程式可使用的 NPP。

## <a name="syntax"></a>語法


```C++
DWORD CreateNPPInterface(
  _In_  HBLOB  hBlob,
  _In_  REFIID iid,
  _Out_ void   **ppvObject
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hBlob* \[在\]
</dt> <dd>

從搜尋工具傳回之 BLOB 的控制碼。

</dd> <dt>

 \[ 中的 iid\]
</dt> <dd>

您從 NPP 呼叫之介面的識別碼 (**IRTC** 或 **IDelaydC**，例如) 。

</dd> <dt>

*ppvObject* \[擴展\]
</dt> <dd>

傳回所要求介面之指標的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為 NMERR \_ SUCCESS。

如果函式不成功，則傳回值為描述錯誤的 NMERR 值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                              |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                    |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl>     |
| 程式庫<br/>                  | <dl> <dt>Npptools .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Npptools.dll</dt> </dl> |



 

 




