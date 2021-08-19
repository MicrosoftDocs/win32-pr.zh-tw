---
description: 停止 Miracast 接收模式、關閉可探索性，並取消註冊回呼。
ms.assetid: 38AE60CB-F601-4C03-A725-9B802341B84B
title: 'WFDDisplaySinkStop 函式 (Wfdsink) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WFDStopDisplaySink
api_type:
- DllExport
api_location:
- wifidisplay.dll
ms.openlocfilehash: a5e2da91e29535c1e2fd9553a2b6ec2bb0008e61f33cd55ebcda2746b93eb657
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117797928"
---
# <a name="wfddisplaysinkstop-function"></a>WFDDisplaySinkStop 函式

停止 Miracast 接收模式、關閉可探索性，並取消註冊回呼。 您的應用程式應該在關機時呼叫此一次。

## <a name="syntax"></a>語法


```C++
DWORD WINAPI WFDStopDisplaySink(void);
```



## <a name="parameters"></a>參數

此函式沒有參數。

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為「錯誤 \_ 成功」。

## <a name="remarks"></a>備註

在呼叫 **WFDStopDisplaySink** 之前，您的應用程式應該已解除封鎖任何進行中的回呼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8.1 \[僅限桌面應用程式\]<br/>                                               |
| 最低支援的伺服器<br/> | Windows Server 2012\[僅限 R2 desktop 應用程式\]<br/>                                    |
| 用戶端支援結束<br/>    | Windows 10<br/>                                                                      |
| 伺服器支援結束<br/>    | Windows Server 2016<br/>                                                             |
| 標頭<br/>                   | <dl> <dt>Wfdsink。h</dt> </dl>       |
| 程式庫<br/>                  | <dl> <dt>Wifidisplay .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wifidisplay.dll</dt> </dl> |



 

 




