---
title: 'MpThreatEnumerate 函式 (MpClient) '
description: 傳回列舉清單中下一個威脅的相關資訊。 您可以重複呼叫這個函式，直到所有威脅的列舉都完成為止。
ms.assetid: 33244F4F-4FB7-4FA7-BC56-B9A30ABC3644
keywords:
- MpThreatEnumerate 函式舊版 Windows 環境功能
topic_type:
- apiref
api_name:
- MpThreatEnumerate
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: acdbb7971371015a401c1a951ace8c55869fd405
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934743"
---
# <a name="mpthreatenumerate-function"></a>MpThreatEnumerate 函式

傳回列舉清單中下一個威脅的相關資訊。 您可以重複呼叫這個函式，直到所有威脅的列舉都完成為止。

## <a name="syntax"></a>語法


```C++
HRESULT WINAPI MpThreatEnumerate(
  _In_  MPHANDLE       hThreatEnumHandle,
  _Out_ PMPTHREAT_INFO *ppThreatInfo
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hThreatEnumHandle* \[在\]
</dt> <dd>

類型： **MPHANDLE**

[**MpThreatOpen**](mpthreatopen.md)所傳回的威脅列舉內容控制碼。

</dd> <dt>

*ppThreatInfo* \[擴展\]
</dt> <dd>

類型： **PMPTHREAT \_ INFO \** _

傳回威脅資訊結構的指標 [_ *MPTHREAT \_ 資訊* *](mpthreat-info.md)。 結構包含威脅識別碼、名稱和嚴重性等資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

如果函式成功，則傳回值為 **S \_ OK**。

如果沒有其他專案可傳回傳回值，則為 **\_ FALSE**。

如果函式失敗，則傳回值會是失敗的 **HRESULT** 程式碼。 呼叫端可以使用 [**MpErrorMessageFormat**](mperrormessageformat.md) 函數來取得錯誤訊息的一般描述。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>                                              |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ desktop 應用程式\]<br/>                                    |
| 標頭<br/>                   | <dl> <dt>MpClient。h</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>MpClient.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MpErrorMessageFormat**](mperrormessageformat.md)
</dt> <dt>

[**MpThreatOpen**](mpthreatopen.md)
</dt> <dt>

[**MPTHREAT \_ 資訊**](mpthreat-info.md)
</dt> </dl>

 

 





