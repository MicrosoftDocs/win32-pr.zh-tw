---
description: GetFrameRecognizeData 函數會傳回 RECOGNIZEDATA 結構的資料表。 其中每個結構都包含通訊協定識別碼，以及指向資料中指定之通訊協定開頭的位移。
ms.assetid: 3bf809ff-8d87-4746-95ee-fb68c5e51d42
title: 'GetFrameRecognizeData 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameRecognizeData
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 2b04472e0fee0238677a6592cace0d1c7fbe078635ac85b92ff8922c68da3c1d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118366496"
---
# <a name="getframerecognizedata-function"></a>GetFrameRecognizeData 函式

**GetFrameRecognizeData** 函數會傳回 **RECOGNIZEDATA** 結構的資料表。 其中每個結構都包含通訊協定識別碼，以及指向資料中指定之通訊協定開頭的位移。

## <a name="syntax"></a>語法


```C++
LPRECOGNIZEDATATABLE WINAPI GetFrameRecognizeData(
  _In_ HFRAME hFrame
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hFrame* \[在\]
</dt> <dd>

框架的控制碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值是 **RECOGNIZEDATATABLE** 結構的指標。

如果函式不成功，則傳回值為零。

## <a name="remarks"></a>備註

[*專家*](e.md) 和 [*剖析*](p.md) 器可以呼叫 **GetFrameRecognizeData** 函數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                           |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                 |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl>  |
| 程式庫<br/>                  | <dl> <dt>Nmapi .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




