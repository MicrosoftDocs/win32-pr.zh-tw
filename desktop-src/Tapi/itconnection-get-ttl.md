---
description: 取得 \_ ttl 方法會取得位址上的傳輸 (Ttl) 範圍的存留時間。
ms.assetid: ea3c22d8-476e-4b4b-98c6-f1075e704f3d
title: 'ITConnection：： get_Ttl 方法 (Sdpblb .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0522098f9959f3595d3deae83161fece53ad95353b9e41a60e653980353b22ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119003376"
---
# <a name="itconnectionget_ttl-method"></a>ITConnection：： get \_ Ttl 方法

\[Windows Vista、Windows Server 2008 及後續版本的作業系統無法使用會合 IP 電話語音會議控制項和介面。 RTC 用戶端 API 提供類似的功能。\]

**取得 \_ ttl** 方法會取得位址上的傳輸 (Ttl) 範圍的 [*存留時間*](t-tapgloss.md)。

## <a name="syntax"></a>語法


```C++
HRESULT get_Ttl(
  [out] unsigned char *pTtl
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pTtl* \[擴展\]
</dt> <dd>

TTL 範圍。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 值                                                                                         | 意義                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>          | 方法成功。<br/>                                    |
| <dl> <dt>**E \_ 指標**</dt> </dl>     | *PTtl* 參數不是有效的指標。<br/>         |
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

[**ITConnection**](itconnection.md)
</dt> </dl>

 

 




