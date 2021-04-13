---
title: 'MpHandleClose 函式 (MpClient) '
description: 關閉 MpManagerOpen、MpScanStart、MpThreatOpen 或 MpUpdateStart 所傳回的控制碼。
ms.assetid: 335776E2-7598-4DC1-92AB-B49B35222EF6
keywords:
- MpHandleClose 函式舊版 Windows 環境功能
topic_type:
- apiref
api_name:
- MpHandleClose
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43c937548c8e1d3b98aa2e3d10d7577f8c69c1c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509227"
---
# <a name="mphandleclose-function"></a>MpHandleClose 函式

關閉 [**MpManagerOpen**](mpmanageropen.md)、 [**MpScanStart**](mpscanstart.md)、 [**MpThreatOpen**](mpthreatopen.md)或 [**MpUpdateStart**](mpupdatestart.md)所傳回的控制碼。

## <a name="syntax"></a>語法


```C++
HRESULT WINAPI MpHandleClose(
  _In_ MPHANDLE hMpHandle
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hMpHandle* \[在\]
</dt> <dd>

類型： **MPHANDLE**

要關閉的控制碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

如果函式成功，則傳回值為 **S \_ OK**。

如果函式失敗，則傳回值會是失敗的 **HRESULT** 程式碼。 呼叫端可以使用 [**MpErrorMessageFormat**](mperrormessageformat.md) 函數來取得錯誤訊息的一般描述。

函數可以傳回下列特定的錯誤：

| 傳回碼             | Description                      |
|-------------------------|----------------------------------|
| E \_ WIN \_ 不正確 \_ 控制碼 | 指定的控制碼無效。 |



 

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

[**MpScanStart**](mpscanstart.md)
</dt> <dt>

[**MpThreatOpen**](mpthreatopen.md)
</dt> </dl>

 

 





