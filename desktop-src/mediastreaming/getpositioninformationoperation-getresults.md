---
title: GetPositionInformationOperation. GetResults 方法
description: 傳回 GetPositionInformationAsync 啟動的非同步作業結果。
ms.assetid: 1DC7CD65-1F0F-44A5-9836-C77A5C23F91E
keywords:
- GetResults 方法媒體串流 API
- GetResults 方法媒體串流 API，GetPositionInformationOperation 介面
- GetPositionInformationOperation 介面媒體串流 API，GetResults 方法
topic_type:
- apiref
api_name:
- GetPositionInformationOperation.GetResults
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6e924227c37318a788f9c30aea5e5125a40c69175ac7c4449a54ebcc4cf61326
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119721058"
---
# <a name="getpositioninformationoperationgetresults-method"></a>GetPositionInformationOperation. GetResults 方法

傳回 [**GetPositionInformationAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getpositioninformationasync)啟動的非同步作業結果。

## <a name="syntax"></a>語法


```C++
HRESULT GetResults(
  [out, retval] PositionInformation *value
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*值* \[退出，retval\]
</dt> <dd>

[**PositionInformation**](/previous-versions/windows/desktop/api/windows.media.streaming/ns-windows-media-streaming-positioninformation)結構的參考，其中包含作業的結果。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回 **HRESULT**。 可能的值包括 (但不限於) 下表中的這些值。



| 傳回碼                                                                          | 描述                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl> | 此方法已成功。<br/> |



 

## <a name="remarks"></a>備註

**GetResults** 方法通常是由設定 [**Completed**](getpositioninformationoperation-completed.md)屬性所註冊的事件處理常式所呼叫。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**GetPositionInformationOperation**](getpositioninformationoperation.md)
</dt> </dl>

 

