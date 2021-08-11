---
title: PlaybackOperation. GetResults 方法
description: 傳回由其中一個 MediaRenderer 播放方法啟動的非同步作業結果。
ms.assetid: EAA5B342-51EF-449A-A7E2-FFBDBE07757C
keywords:
- GetResults 方法媒體串流 API
- GetResults 方法媒體串流 API，PlaybackOperation 介面
- PlaybackOperation 介面媒體串流 API，GetResults 方法
topic_type:
- apiref
api_name:
- PlaybackOperation.GetResults
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9bd3c79164a78e7993eb8a58d0d89a64c7ceb31a0c33eaff2e9c1bc352144088
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118235781"
---
# <a name="playbackoperationgetresults-method"></a>PlaybackOperation. GetResults 方法

傳回由其中一個 [**MediaRenderer**](mediarenderer.md) 播放方法啟動的非同步作業結果。

## <a name="syntax"></a>語法


```C++
HRESULT GetResults(
  [out, retval] UINT32 *value
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*值* \[退出，retval\]
</dt> <dd>

運算的結果。 值為0表示作業已完成。 其他值則會保留。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回 **HRESULT**。 可能的值包括 (但不限於) 下表中的這些值。



| 傳回碼                                                                          | 描述                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl> | 此方法已成功。<br/> |



 

## <a name="remarks"></a>備註

**GetResults** 方法通常是由設定 [**Completed**](playbackoperation-completed.md)屬性所註冊的事件處理常式所呼叫。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**PlaybackOperation**](playbackoperation.md)
</dt> </dl>

 

 





