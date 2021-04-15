---
title: 'MpScanControl 函式 (MpClient) '
description: 允許透過 MpScanStart 以非同步方式起始的掃描控制。
ms.assetid: 00855686-8C46-4B58-829C-AEAB53888704
keywords:
- MpScanControl 函式舊版 Windows 環境功能
topic_type:
- apiref
api_name:
- MpScanControl
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce74736c4ca8c589e2ffa5570f2b6666838d820f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465161"
---
# <a name="mpscancontrol-function"></a>MpScanControl 函式

允許透過 [**MpScanStart**](mpscanstart.md)以非同步方式起始的掃描控制。

## <a name="syntax"></a>語法


```C++
HRESULT WINAPI MpScanControl(
  _In_ MPHANDLE  hScanHandle,
  _In_ MPCONTROL ScanControl
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hScanHandle* \[在\]
</dt> <dd>

類型： **MPHANDLE**

非同步掃描操作的控制碼。 [**MpScanStart**](mpscanstart.md)函數會傳回這個控制碼。 此參數也可以設定為 [**MpManagerOpen**](mpmanageropen.md) 函式所傳回的 malware protection manager 介面控制碼，以控制系統起始的掃描，在這種情況下，呼叫端必須具有系統管理許可權。

</dd> <dt>

*ScanControl* \[在\]
</dt> <dd>

類型： **mpcontrol.log**

指定掃描控制選項。 此參數必須是下列其中一個控制項選項：



| 值                                                                                                                                                                  | 意義                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <span id="MPCONTROL_ABORT"></span><span id="mpcontrol_abort"></span><dl> <dt>**MPCONTROL.LOG \_ 中止**</dt> </dl>    | 中止掃描工作。<br/>         |
| <span id="MPCONTROL_PAUSE"></span><span id="mpcontrol_pause"></span><dl> <dt>**MPCONTROL.LOG \_ 暫停**</dt> </dl>    | 暫停掃描工作。<br/>         |
| <span id="MPCONTROL_RESUME"></span><span id="mpcontrol_resume"></span><dl> <dt>**MPCONTROL.LOG \_ RESUME**</dt> </dl> | 繼續暫停的掃描工作。<br/> |



 

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

[**MpScanStart**](mpscanstart.md)
</dt> </dl>

 

 





