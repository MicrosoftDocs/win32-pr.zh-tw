---
title: GetVolumeOperation. GetResults 方法
description: 傳回 GetVolumeAsync 啟動的非同步作業結果。
ms.assetid: 71DC4D76-4CC2-4D40-960F-AF56E1F33557
keywords:
- GetResults 方法媒體串流 API
- GetResults 方法媒體串流 API，GetVolumeOperation 介面
- GetVolumeOperation 介面媒體串流 API，GetResults 方法
topic_type:
- apiref
api_name:
- GetVolumeOperation.GetResults
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 444eaf590e5afc5d4f5185bcd3793698d6fe4535
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "106969705"
---
# <a name="getvolumeoperationgetresults-method"></a>GetVolumeOperation. GetResults 方法

傳回 [**GetVolumeAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getvolumeasync)啟動的非同步作業結果。

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

磁片區。 介於0與100之間的值。 0表示最小磁片區，100表示最大磁片區。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回 **HRESULT**。 可能的值包括 (但不限於) 下表中的這些值。



| 傳回碼                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl> | 此方法已成功。<br/> |



 

## <a name="remarks"></a>備註

**GetResults** 方法通常是由設定 [**Completed**](getvolumeoperation-completed.md)屬性所註冊的事件處理常式所呼叫。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**GetVolumeOperation**](getvolumeoperation.md)
</dt> </dl>

 

