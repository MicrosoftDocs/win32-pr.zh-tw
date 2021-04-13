---
title: 'MpUpdateControl 函式 (MpClient) '
description: 允許透過 MpUpdateStart 以非同步方式啟動的簽章更新作業控制。
ms.assetid: 2780E472-6E8D-4839-88EE-46E3448C6BF5
keywords:
- MpUpdateControl 函式舊版 Windows 環境功能
topic_type:
- apiref
api_name:
- MpUpdateControl
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91ea28c6ace349fd04fb9241d7eddbe7c1e5fbbe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465933"
---
# <a name="mpupdatecontrol-function"></a>MpUpdateControl 函式

允許透過 [**MpUpdateStart**](mpupdatestart.md)以非同步方式啟動的簽章更新作業控制。 呼叫此函式需要系統管理員許可權，因為它允許取消整個系統的簽章更新。

## <a name="syntax"></a>語法


```C++
HRESULT WINAPI MpUpdateControl(
  _In_ MPHANDLE  hUpdateHandle,
  _In_ MPCONTROL UpdateControl
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hUpdateHandle* \[在\]
</dt> <dd>

類型： **MPHANDLE**

非同步簽名更新作業的控制碼。 [**MpScanStart**](mpscanstart.md)函數會傳回這個控制碼。

</dd> <dt>

*UpdateControl* \[在\]
</dt> <dd>

類型： **mpcontrol.log**

指定 signature update control 選項。 它必須是下列值：



| 值                                                                                                                                                               | 意義                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span id="MPCONTROL_ABORT"></span><span id="mpcontrol_abort"></span><dl> <dt>**MPCONTROL.LOG \_ 中止**</dt> </dl> | 中止簽章更新作業。<br/> |



 

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

[**MpScanStart**](mpscanstart.md)
</dt> </dl>

 

 





