---
title: 'MpErrorMessageFormat 函式 (MpClient) '
description: 根據錯誤碼傳回格式化的錯誤訊息。
ms.assetid: C125FCE4-3BB0-4608-BBF3-E7FEF17D0807
keywords:
- MpErrorMessageFormat 函式舊版 Windows 環境功能
topic_type:
- apiref
api_name:
- MpErrorMessageFormat
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 124bf9e2c5c2ecc18f286b99f0c3b93695abd3f6a40853fcc47de580edef5db4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117883505"
---
# <a name="mperrormessageformat-function"></a>MpErrorMessageFormat 函式

根據錯誤碼傳回格式化的錯誤訊息。

## <a name="syntax"></a>語法


```C++
HRESULT WINAPI MpErrorMessageFormat(
  _In_  MPHANDLE hMpHandle,
  _In_  HRESULT  hrError,
  _Out_ LPWSTR   *pwszErrorDesc
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hMpHandle* \[在\]
</dt> <dd>

類型： **MPHANDLE**

惡意程式碼防護管理員介面的控制碼。 [**MpManagerOpen**](mpmanageropen.md)函數會傳回這個控制碼。

</dd> <dt>

*hrError* \[在\]
</dt> <dd>

類型： **HRESULT**

以 **HRESULT** 為基礎的錯誤碼。

</dd> <dt>

*pwszErrorDesc* \[擴展\]
</dt> <dd>

類型： **LPWSTR \***

根據 *hrError* 傳回格式化的錯誤訊息。 您必須使用 [**MpFreeMemory**](mpfreememory.md)來釋放這個字串。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

如果函式成功，則傳回值為 **S \_ OK**。

如果函式失敗，則傳回值會是失敗的 **HRESULT** 程式碼。

## <a name="remarks"></a>備註

除了惡意程式碼防護函式所傳回的特定錯誤碼之外，此函數還能夠格式化系統錯誤碼。 惡意程式碼防護功能特定的 **HRESULT** 錯誤碼有0x50 的功能。 以下是可由各種惡意程式碼防護功能傳回的惡意程式碼防護特定錯誤碼的清單。 使用 **\_ 來自 \_ MP \_ 狀態** 的宏 HRESULT，可將下列錯誤碼轉換成 **HRESULT**。 另請參閱 [Forefront Client Security 反惡意程式碼引擎錯誤碼](https://support.microsoft.com/kb/939359) ，以取得其他可能錯誤碼的清單。



| 錯誤碼                              | 描述                                                                                                                 |
|-----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| 錯誤 \_ MP \_ NOENGINE                     | 未在反惡意程式碼服務中載入引擎以執行要求的操作。                                              |
| 錯誤 \_ MP \_ 沒有 \_ 記憶體                   | 反惡意程式碼引擎發生記憶體不足的情況。                                                               |
| 錯誤 \_ MP \_ 移除 \_ 失敗               | 特定威脅的移除作業失敗。                                                                              |
| 錯誤 \_ MP \_ 隔離 \_ 失敗           | 特定威脅的隔離操作失敗。                                                                          |
| \_ \_ \_ \_ 找不到錯誤 MP 威脅           | 系統中已不再有特定威脅。                                                                         |
| \_ \_ \_ 不支援錯誤 MP \_ 移除       | 不支援對容器類型內的特定威脅進行移除操作。                                          |
| 錯誤 \_ MP \_ 移除 \_ 不可變的 \_ 容器 | 由於引擎原則，不支援在已封鎖容器內的特定威脅移除作業。  (Mail 封存。 )  |
| 錯誤 \_ MP \_ BADDB \_ OLDENGINE             | 簽章更新要求 (s) ，提供了較舊的引擎或簽章檔案。                                                    |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[僅限桌面應用程式\]<br/>                                              |
| 最低支援的伺服器<br/> | Windows Server 2012 \[僅限桌面應用程式\]<br/>                                    |
| 標頭<br/>                   | <dl> <dt>MpClient。h</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>MpClient.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MpFreeMemory**](mpfreememory.md)
</dt> <dt>

[**MpManagerOpen**](mpmanageropen.md)
</dt> <dt>

[Forefront Client Security 反惡意程式碼引擎錯誤碼](https://support.microsoft.com/kb/939359)
</dt> </dl>

 

 





