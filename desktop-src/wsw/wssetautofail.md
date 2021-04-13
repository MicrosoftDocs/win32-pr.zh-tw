---
title: 'WsSetAutoFail 函式 (WebServicesDebug) '
description: 設定下一個插入失敗的點。 這是僅限 DEBUG 函數。
ms.assetid: b453dbc5-01ff-486d-8767-254b74cc5b6e
keywords:
- 適用于 Windows 的 WsSetAutoFail 函式 Web 服務
topic_type:
- apiref
api_name:
- WsSetAutoFail
api_location:
- WebServicesDebug.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ba10b8b038f270f764b064fac1cb81e675f5239
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509083"
---
# <a name="wssetautofail-function"></a>WsSetAutoFail 函式

設定下一個插入失敗的點。 這是僅限 DEBUG 函數。

## <a name="syntax"></a>語法


```C++
HRESULT WINAPI  WsSetAutoFail(
  _In_     ULONG     count,
  _In_opt_ WS_ERROR* error
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*計數* \[在\]
</dt> <dd>

指定失敗前的作業開始發生的次數。

</dd> <dt>

*錯誤* \[在中，選擇性\]
</dt> <dd>

[WS \_ ERROR](ws-error.md)物件的指標，如果函式失敗，則應儲存錯誤的其他相關資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果此函式成功，則會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 R2 \[ desktop 應用程式\]<br/>                                       |
| 標頭<br/>                   | <dl> <dt>WebServicesDebug。h</dt> </dl> |



 

 





