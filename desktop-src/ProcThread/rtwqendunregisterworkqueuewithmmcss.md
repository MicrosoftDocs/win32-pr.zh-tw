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
ms.openlocfilehash: b55386b2a018b0e311a1d4dbb2084b136d49c2f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849620"
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
| 最低支援的用戶端<br/> | \[僅 Windows 8.1 桌面應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 R2 \[ desktop 應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>None</dt> </dl>        |
| 程式庫<br/>                  | <dl> <dt>Rtworkq .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RTWorkQ.dll</dt> </dl> |



 

 
