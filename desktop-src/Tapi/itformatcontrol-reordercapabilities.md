---
description: ReOrderCapabilities 方法會為格式功能設定新的順序。
ms.assetid: 05785d64-a22f-411f-9fae-318828d30c52
title: 'ITFormatControl：： ReOrderCapabilities 方法 (Ipmsp .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d6f7800e4a04dbd70c5b270778cd7eb0ff540b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987180"
---
# <a name="itformatcontrolreordercapabilities-method"></a>ITFormatControl：： ReOrderCapabilities 方法

\[ 在 Windows Vista、Windows Server 2008 和後續的作業系統版本中，無法使用這個方法。 RTC 用戶端 API 提供類似的功能。\]

**ReOrderCapabilities** 方法會為格式功能設定新的順序。

## <a name="syntax"></a>語法


```C++
HRESULT ReOrderCapabilities(
  [in] DWORD *pdwIndices,
  [in] BOOL  *pfEnabled,
  [in] BOOL  *pfPublicize,
  [in] DWORD dwNumIndices
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pdwIndices* \[在\]
</dt> <dd>

要重新排序之格式的索引。

</dd> <dt>

*pfEnabled* \[在\]
</dt> <dd>

指出是否應該啟用或停用格式。

</dd> <dt>

*pfPublicize* \[在\]
</dt> <dd>

指出是否應該將格式設為可用。

</dd> <dt>

*dwNumIndices* \[在\]
</dt> <dd>

格式的新索引編號。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回碼                                                                                   | Description                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>          | 方法成功。<br/>                                    |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | 記憶體不足，無法執行操作。<br/> |



 

## <a name="remarks"></a>備註

使用這個方法之前，必須先呼叫 [**GetNumberOfCapabilities**](itformatcontrol-getnumberofcapabilities.md) 方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|--------------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 3。1<br/>                                                         |
| 標頭<br/>       | <dl> <dt>Ipmsp。h</dt> </dl>   |
| 程式庫<br/>      | <dl> <dt>Uuid</dt> </dl>  |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ITFormatControl**](itformatcontrol.md)
</dt> <dt>

[**GetNumberOfCapabilities**](itformatcontrol-getnumberofcapabilities.md)
</dt> </dl>

 

 




