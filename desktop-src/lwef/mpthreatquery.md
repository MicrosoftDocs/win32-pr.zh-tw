---
title: 'MpThreatQuery 函式 (MpClient) '
description: 用來查詢靜態 (（例如嚴重性和類別）) 或當地語系化的 (例如類別描述和建議) 特定威脅的相關資訊。
ms.assetid: A06854B2-8444-46A4-A53F-FD5FEAFF47B7
keywords:
- MpThreatQuery 函式舊版 Windows 環境功能
topic_type:
- apiref
api_name:
- MpThreatQuery
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21d38a3734f9d98f3bd61143d4fe58bd606c7508
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966101"
---
# <a name="mpthreatquery-function"></a>MpThreatQuery 函式

用來查詢靜態 (（例如嚴重性和類別）) 或當地語系化的 (例如類別描述和建議) 特定威脅的相關資訊。

## <a name="syntax"></a>語法


```C++
HRESULT WINAPI MpThreatQuery(
  _In_      MPHANDLE                 hMpHandle,
  _In_      MPTHREAT_ID              ThreatID,
  _Out_     PMPTHREAT_INFO           *ppThreatInfo,
  _Out_opt_ PMPTHREAT_LOCALIZED_INFO *ppThreatLocalizedInfo
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hMpHandle* \[在\]
</dt> <dd>

類型： **MPHANDLE**

惡意程式碼防護管理員介面的控制碼。 [**MpManagerOpen**](mpmanageropen.md)函數會傳回這個控制碼。

</dd> <dt>

*ThreatID* \[在\]
</dt> <dd>

類型： **MPTHREAT \_ 識別碼**

要求資訊的威脅識別碼。

</dd> <dt>

*ppThreatInfo* \[擴展\]
</dt> <dd>

類型： **PMPTHREAT \_ INFO \** _

傳回威脅資訊結構的指標 [_ *MPTHREAT \_ 資訊* *](mpthreat-info.md)。 結構包含威脅識別碼、名稱和嚴重性等資訊。

</dd> <dt>

*ppThreatLocalizedInfo* \[out、optional\]
</dt> <dd>

類型： **PMPTHREAT \_ 當地語系化 \_ 的 \* 資訊* _

傳回結構的指標，其中包含有關威脅的當地語系化資訊。 如果您對威脅的當地語系化資訊不感興趣，您可以傳遞 _ *Null**。 請參閱 [**MPTHREAT \_ 當地語系化 \_ 資訊**](mpthreat-localized-info.md)。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

如果函式成功，則傳回值為 **S \_ OK**。

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

[**MpManagerOpen**](mpmanageropen.md)
</dt> <dt>

[**MPTHREAT \_ 資訊**](mpthreat-info.md)
</dt> <dt>

[**MPTHREAT \_ 當地語系化的 \_ 資訊**](mpthreat-localized-info.md)
</dt> </dl>

 

 





