---
title: GetTransportInformationOperation GetResults 方法
description: 傳回 GetTransportInformationAsync 啟動的非同步作業結果。
ms.assetid: 8CC6641E-C1E6-4C64-90EC-4120ECB54135
keywords:
- GetResults 方法媒體串流 API
- GetResults 方法媒體串流 API，GetTransportInformationOperation 介面
- GetTransportInformationOperation 介面媒體串流 API，GetResults 方法
topic_type:
- apiref
api_name:
- GetTransportInformationOperation.GetResults
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2bbcc6345a09d0553df240c57e50b4498618be76cc75814f268892aa6e0b4dc2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119100632"
---
# <a name="gettransportinformationoperationgetresults-method"></a>GetTransportInformationOperation：： GetResults 方法

傳回 [**GetTransportInformationAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-gettransportinformationasync)啟動的非同步作業結果。

## <a name="syntax"></a>語法


```C++
HRESULT GetResults(
  [out, retval] TransportInformation *value
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*值* \[退出，retval\]
</dt> <dd>

[**TransportInformation**](/previous-versions/windows/desktop/api/windows.media.streaming/ns-windows-media-streaming-transportinformation)結構的參考，其中包含作業的結果。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回 **HRESULT**。 可能的值包括 (但不限於) 下表中的這些值。



| 傳回碼                                                                          | 描述                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl> | 此方法已成功。<br/> |



 

## <a name="remarks"></a>備註

**GetResults** 方法通常是由設定 [**Completed**](gettransportinformationoperation-completed.md)屬性所註冊的事件處理常式所呼叫。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**GetTransportInformationOperation**](gettransportinformationoperation.md)
</dt> </dl>

 

