---
description: 取得 \_ SessionId 方法會取得32位 NTP (網路時間通訊協定) 值，作為會話識別碼。 這是在會話建立時自動產生的。
ms.assetid: 5177f120-4b93-40bc-9481-aedf65a8dee9
title: 'ITSdp：： get_SessionId 方法 (Sdpblb .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67f7e8ea9bef17e5cb34ca23443b1f16f815c964c3cf76b9b122878e8662d051
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119621538"
---
# <a name="itsdpget_sessionid-method"></a>ITSdp：： get \_ SessionId 方法

\[Windows Vista、Windows Server 2008 及後續版本的作業系統無法使用會合 IP 電話語音會議控制項和介面。 RTC 用戶端 API 提供類似的功能。\]

**取得 \_ SessionId** 方法會取得32位 NTP (網路時間通訊協定) 值，作為會話識別碼。 這是在會話建立時自動產生的。

## <a name="syntax"></a>語法


```C++
HRESULT get_SessionId(
  [out] DOUBLE *pSessionId
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pSessionId* \[擴展\]
</dt> <dd>

會話識別碼的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回碼                                                                                   | 描述                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>          | 方法成功。<br/>                                    |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | *PSessionId* 參數無效。<br/>             |
| <dl> <dt>**E \_ 指標**</dt> </dl>     | *PSessionId* 參數不是有效的指標。<br/>   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | 記憶體不足，無法執行操作。<br/> |
| <dl> <dt>**E \_ 失敗**</dt> </dl>        | 未指定的錯誤。<br/>                                   |
| <dl> <dt>**E \_ >NOTIMPL**</dt> </dl>     | 尚未實作這個方法。<br/>                  |



 

## <a name="remarks"></a>備註

這個方法的傳回值可以是 **ulong**，但是 Visual Basic 不支援 **ulong** 型別。 **DOUBLE** 是下一個最小的型別，其中包含所需的整個值範圍。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 3.0 或更新版本<br/>                                                 |
| 標頭<br/>       | <dl> <dt>Sdpblb。h</dt> </dl>   |
| 程式庫<br/>      | <dl> <dt>Uuid</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ITSdp**](itsdp.md)
</dt> </dl>

 

 




