---
title: 'MpManagerOpen 函式 (MpClient) '
description: 在本機電腦上建立與惡意程式碼防護管理員的連接。
ms.assetid: 40513A74-AFCC-4E22-9B78-D46FEB575A00
keywords:
- MpManagerOpen 函式舊版 Windows 環境功能
topic_type:
- apiref
api_name:
- MpManagerOpen
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af432cc7d91530fd3d37176592f7f457b31b6314
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686328"
---
# <a name="mpmanageropen-function"></a>MpManagerOpen 函式

在本機電腦上建立與惡意程式碼防護管理員的連接。

## <a name="syntax"></a>語法


```C++
HRESULT WINAPI MpManagerOpen(
  _In_  DWORD     dwReserved,
  _Out_ PMPHANDLE phMpHandle
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*>dwreserved* \[在\]
</dt> <dd>

類型： **DWORD**

保留供未來使用。 必須設定為 0。

</dd> <dt>

*phMpHandle* \[擴展\]
</dt> <dd>

類型： **PMPHANDLE**

惡意程式碼防護管理員介面的控制碼。 您必須使用 [**MpHandleClose**](mphandleclose.md) 函式來關閉此控制碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

如果函式成功，則傳回值為 **S \_ OK**。 即使反惡意程式碼服務不在執行中，此函式呼叫仍會成功。

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

[**MpHandleClose**](mphandleclose.md)
</dt> </dl>

 

 





