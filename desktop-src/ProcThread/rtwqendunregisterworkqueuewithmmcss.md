---
description: 完成非同步要求，以利用多媒體類別排程器服務將工作佇列取消註冊 (MMCSS) 工作。
ms.assetid: 0E8F9BF6-AC1E-4FC0-BFAE-F292C4859F1F
title: RtwqEndUnregisterWorkQueueWithMMCSS 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtwqEndUnregisterWorkQueueWithMMCSS
api_type:
- DllExport
api_location:
- RTWorkQ.dll
ms.openlocfilehash: 083f0ca787bb842850320b9dd1d320ef4d5b172ee0b6d9b117296e58b991bd0d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117793398"
---
# <a name="rtwqendunregisterworkqueuewithmmcss-function"></a>RtwqEndUnregisterWorkQueueWithMMCSS 函式

完成非同步要求，以利用多媒體類別排程器服務將工作佇列取消註冊 (MMCSS) 工作。

## <a name="syntax"></a>語法


```C++
HRESULT WINAPI RtwqEndUnregisterWorkQueueWithMMCSS(
    IMFAsyncResult  *pResult 
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pResult* 
</dt> <dd>

[**IMFAsyncResult**](/windows/win32/api/mfobjects/nn-mfobjects-imfasyncresult)介面的指標。 傳入您的回呼物件在 [**IRtwqAsyncCallback：： Invoke**](/windows/win32/api/rtworkq/nf-rtworkq-irtwqasynccallback-invoke) 方法中收到的相同指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果此函式成功，則會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8.1 \[僅限桌面應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | Windows Server 2012\[僅限 R2 desktop 應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>None</dt> </dl>        |
| 程式庫<br/>                  | <dl> <dt>Rtworkq .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RTWorkQ.dll</dt> </dl> |



 

 
