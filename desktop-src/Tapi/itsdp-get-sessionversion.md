---
description: Get \_ SessionVersion 方法會取得32位 (理想的網路時間通訊協定，或作為會話版本的 NTP) 值。
ms.assetid: 39c2aef4-24e3-4ea0-8b23-dff842f9ab84
title: 'ITSdp：： get_SessionVersion 方法 (Sdpblb .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7661fb5f133d214748991510d56387991872fa69243353b5144623a1ef19f91
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119476588"
---
# <a name="itsdpget_sessionversion-method"></a>ITSdp：： get \_ SessionVersion 方法

\[Windows Vista、Windows Server 2008 及後續版本的作業系統無法使用會合 IP 電話語音會議控制項和介面。 RTC 用戶端 API 提供類似的功能。\]

**Get \_ SessionVersion** 方法會取得32位 (理想的網路時間通訊協定，或作為會話版本的 NTP) 值。 雖然這是在會話建立時自動產生的，但在更改 SDP 時，使用者必須負責變更。

## <a name="syntax"></a>語法


```C++
HRESULT get_SessionVersion(
  [out] DOUBLE *pSessionVersion
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pSessionVersion* \[擴展\]
</dt> <dd>

會話版本識別碼的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回碼                                                                                   | 描述                                                        |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>          | 方法成功。<br/>                                       |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | *PSessionVersion* 參數無效。<br/>           |
| <dl> <dt>**E \_ 指標**</dt> </dl>     | *PSessionVersion* 參數不是有效的指標。<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | 記憶體不足，無法執行操作。<br/>    |
| <dl> <dt>**E \_ 失敗**</dt> </dl>        | 未指定的錯誤。<br/>                                      |
| <dl> <dt>**E \_ >NOTIMPL**</dt> </dl>     | 尚未實作這個方法。<br/>                     |



 

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
</dt> <dt>

[**ITSdp：:p 的 \_ SessionVersion**](itsdp-put-sessionversion.md)
</dt> </dl>

 

 




