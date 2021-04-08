---
description: GetCaptureMacType 函式會傳回指定之捕捉的 MAC 型別。
ms.assetid: de0dfb36-df3a-4f6e-b266-09c81dfdc88b
title: 'GetCaptureMacType 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCaptureMacType
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 73569109db5b958e854135461a0e480178d0105a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689724"
---
# <a name="getcapturemactype-function"></a>GetCaptureMacType 函式

**GetCaptureMacType** 函式會傳回指定之捕捉的 MAC 型別。

## <a name="syntax"></a>語法


```C++
DWORD WINAPI GetCaptureMacType(
  _In_ HCAPTURE hCapture
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hCapture* \[在\]
</dt> <dd>

捕捉的控制碼。 如需取得 capture 控制碼的詳細資訊，請參閱本 **GetCaptureMacType** 主題中的「備註」一節。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值是下列其中一種 MAC 類型。

-   MAC \_ 類型 \_ 不明
-   MAC \_ 類型 \_ ETHERNET
-   MAC \_ 類型 \_ TOKENRING
-   MAC \_ 類型的 \_ FDDI

如果函式不成功，則傳回值為錯誤碼。



| 傳回碼                                                                                              | Description                                                 |
|----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <dt>**NMERR \_ MAC \_ 類型 \_ 不明**</dt> </dl> | 網路監視器找不到已知的 MAC 類型。<br/> |



 

## <a name="remarks"></a>備註

您可以透過數種方式取得 capture 的控制碼，視呼叫者而定。 對於專家而言，控制碼是在 [EXPERTSTARTUPINFO](expertstartupinfo.md)結構的 **hCapture** 成員中指定的。 若為剖析器，可以藉由呼叫 [GetFrameCaptureHandle](getframecapturehandle.md) 函數來取得 capture 控制碼。

[*專家*](e.md) 和 [*剖析*](p.md) 器可以呼叫 **GetCaptureMacType** 函數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                           |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                 |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl>  |
| 程式庫<br/>                  | <dl> <dt>Nmapi .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




