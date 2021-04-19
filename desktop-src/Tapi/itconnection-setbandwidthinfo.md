---
description: SetBandwidthInfo 方法會設定頻寬資訊。
ms.assetid: bf5db456-ea67-4a65-a681-df0741f73fc9
title: 'ITConnection：： SetBandwidthInfo 方法 (Sdpblb .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c17054743f6d47775e994dbfe3b80c7afe1ab68
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994645"
---
# <a name="itconnectionsetbandwidthinfo-method"></a>ITConnection：： SetBandwidthInfo 方法

\[ 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用會合 IP 電話語音會議控制項和介面。 RTC 用戶端 API 提供類似的功能。\]

**SetBandwidthInfo** 方法會設定頻寬資訊。

## <a name="syntax"></a>語法


```C++
HRESULT SetBandwidthInfo(
  [in] BSTR   pModifier,
  [in] DOUBLE Bandwidth
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pModifier* \[在\]
</dt> <dd>

指向表示所設定之頻寬範圍的 **BSTR** 指標。 如需詳細資訊，請參閱接下來的＜備註＞一節。

</dd> <dt>

*頻寬* \[在\]
</dt> <dd>

頻寬。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 值                                                                                         | 意義                                                           |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>          | 方法成功。<br/>                                      |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | *PModifier* 或 *頻寬* 參數無效。<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | 記憶體不足，無法執行操作。<br/>   |
| <dl> <dt>**E \_ 失敗**</dt> </dl>        | 未指定的錯誤。<br/>                                     |
| <dl> <dt>**E \_ >NOTIMPL**</dt> </dl>     | 尚未實作這個方法。<br/>                    |



 

## <a name="remarks"></a>備註

應用程式必須使用 [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) 為 *pModifier* 參數配置記憶體，並在不再需要該變數時，使用 [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) 來釋放記憶體。

參考： RFC 2327。

頻寬修飾詞通常會是 CT 或如下：

**CT 會議總計：** 每次在 Mbone 上或特定多播系統管理範圍區域內，會有一 [*次*](t-tapgloss.md) 隱含的最大頻寬關聯 (TTL)  (Mbone 頻寬與 TTL 限制在 Mbone 常見問題) 中提供。 如果會話或媒體的頻寬與範圍隱含的頻寬不同，則 \` b = CT： ... '應為會話提供行，以提供所使用之頻寬的上限。 這項功能的主要目的是要讓您大致瞭解兩個或多個會議是否可以同時並存。

**Application-Specific 最大值：** 頻寬會被視為應用程式特定的，也就是應用程式的最大頻寬概念。 一般來說，這會與應用程式的「最大頻寬」控制項上的設定相符（如果適用）。

請注意，[CT] 會為所有網站上的所有媒體提供總頻寬圖。 在單一網站提供單一媒體的頻寬圖，雖然可能會同時傳送許多網站。

**延伸模組機制：** 工具寫入器可以定義實驗的頻寬修飾詞，方法是在其修飾詞前面加上 "X-"。

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

 

