---
description: Get \_ NumPorts 方法會取得會話所需的埠數目。 會話會使用從 get StartPort 傳回的值開始的指定埠數目 \_ 。
ms.assetid: 9ebdcf51-e095-4173-97d6-7754560abfb5
title: 'ITMedia：： get_NumPorts 方法 (Sdpblb .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 928f1622c26159720a5eaabe42a16dd5513705c4d9abe9ad75db47160ab3e218
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118865001"
---
# <a name="itmediaget_numports-method"></a>ITMedia：： get \_ NumPorts 方法

\[Windows Vista、Windows Server 2008 及後續版本的作業系統無法使用會合 IP 電話語音會議控制項和介面。 RTC 用戶端 API 提供類似的功能。\]

**Get \_ NumPorts** 方法會取得會話所需的埠數目。 會話會使用從 [**get \_ StartPort**](itmedia-get-startport.md)傳回的值開始的指定埠數目。

## <a name="syntax"></a>語法


```C++
HRESULT get_NumPorts(
  [out] LONG *pNumPorts
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pNumPorts* \[擴展\]
</dt> <dd>

埠數目的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回碼                                                                                   | 描述                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>          | 方法成功。<br/>                                    |
| <dl> <dt>**E \_ 指標**</dt> </dl>     | *PNumPorts* 參數不是有效的指標。<br/>    |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | 記憶體不足，無法執行操作。<br/> |
| <dl> <dt>**E \_ 失敗**</dt> </dl>        | 未指定的錯誤。<br/>                                   |
| <dl> <dt>**E \_ >NOTIMPL**</dt> </dl>     | 尚未實作這個方法。<br/>                  |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 3.0 或更新版本<br/>                                                 |
| 標頭<br/>       | <dl> <dt>Sdpblb。h</dt> </dl>   |
| 程式庫<br/>      | <dl> <dt>Uuid</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ITMedia**](itmedia.md)
</dt> </dl>

 

 




