---
description: Put \_ TransportProtocol 方法會設定傳輸通訊協定。
ms.assetid: d2f74d4a-a65d-4829-ad17-7548ef06cfeb
title: 'ITMedia：:p ut_TransportProtocol 方法 (Sdpblb .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c6b4228a5d2a6ea49ae3f87b9306ea80e94fc36
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990060"
---
# <a name="itmediaput_transportprotocol-method"></a>ITMedia：:p 的 \_ TransportProtocol 方法

\[ 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用會合 IP 電話語音會議控制項和介面。 RTC 用戶端 API 提供類似的功能。\]

**Put \_ TransportProtocol** 方法會設定傳輸通訊協定。 除了媒體格式之外，還會指定相同的標準媒體格式，即使網路通訊協定相同（例如，使用 Vat PCM 音訊和 RTP PCM 音訊），相同的標準媒體格式也可能會透過不同的傳輸通訊協定來執行。

## <a name="syntax"></a>語法


```C++
HRESULT put_TransportProtocol(
  [in] BSTR pProtocol
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pProtocol* \[在\]
</dt> <dd>

包含傳輸通訊協定之 **BSTR** 的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回碼                                                                                   | Description                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>          | 方法成功。<br/>                                    |
| <dl> <dt>**E \_ 指標**</dt> </dl>     | *PProtocol* 參數不是有效的指標。<br/>    |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | 記憶體不足，無法執行操作。<br/> |
| <dl> <dt>**E \_ 失敗**</dt> </dl>        | 未指定的錯誤。<br/>                                   |
| <dl> <dt>**E \_ >NOTIMPL**</dt> </dl>     | 尚未實作這個方法。<br/>                  |



 

## <a name="remarks"></a>備註

應用程式必須使用 [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) 為 *pProtocol* 參數配置記憶體，並在不再需要該變數時，使用 [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) 來釋放記憶體。

此函式可能會以未加密的形式，在網路上傳送資料。因此，在網路上竊聽的人可以讀取資料。 使用這個方法之前，請先考慮以純文字傳送資料的安全性風險。

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
</dt> <dt>

[**ITMedia：： get \_ TransportProtocol**](itmedia-get-transportprotocol.md)
</dt> </dl>

 

