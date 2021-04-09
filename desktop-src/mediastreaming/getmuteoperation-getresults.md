---
title: GetMuteOperation. GetResults 方法
description: 傳回 GetMuteAsync 啟動的非同步作業結果。
ms.assetid: 5B6DB1B3-54D4-486D-AA03-5FEEC92304B0
keywords:
- GetResults 方法媒體串流 API
- GetResults 方法媒體串流 API，GetMuteOperation 介面
- GetMuteOperation 介面媒體串流 API，GetResults 方法
topic_type:
- apiref
api_name:
- GetMuteOperation.GetResults
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 33c43dc7fee228b1808ff4f607ee6a72faf1e770
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104092668"
---
# <a name="getmuteoperationgetresults-method"></a>GetMuteOperation. GetResults 方法

傳回 [**GetMuteAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getmuteasync)啟動的非同步作業結果。

## <a name="syntax"></a>語法


```C++
HRESULT GetResults(
  [out, retval] boolean *value
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*值* \[退出，retval\]
</dt> <dd>

靜音值。 值為 true 表示音訊目前為靜音。 值為 false 表示音訊未靜音。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回 **HRESULT**。 可能的值包括 (但不限於) 下表中的這些值。



| 傳回碼                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl> | 此方法已成功。<br/> |



 

## <a name="remarks"></a>備註

**GetResults** 方法通常是由設定 [**Completed**](getmuteoperation-completed.md)屬性所註冊的事件處理常式所呼叫。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**GetMuteOperation**](getmuteoperation.md)
</dt> </dl>

 

