---
title: GetStreamPropertiesOperation. GetResults 方法
description: 傳回 GetStreamPropertiesAsync 啟動的非同步作業結果。
ms.assetid: D09DCDF5-2B9E-4E03-908B-AEEC7DC228C1
keywords:
- GetResults 方法媒體串流 API
- GetResults 方法媒體串流 API，GetStreamPropertiesOperation 介面
- GetStreamPropertiesOperation 介面媒體串流 API，GetResults 方法
topic_type:
- apiref
api_name:
- GetStreamPropertiesOperation.GetResults
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b3520cc44919e9c606c6625c75193b5f1ab54f4005cc098316bd8769ad0e0fe7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118735819"
---
# <a name="getstreampropertiesoperationgetresults-method"></a>GetStreamPropertiesOperation. GetResults 方法

傳回 [**GetStreamPropertiesAsync**](/previous-versions/windows/desktop/legacy/hh829001(v=vs.85))啟動的非同步作業結果。

## <a name="syntax"></a>語法


```C++
HRESULT GetResults(
  [out, retval] UINT32 *value
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*值* \[退出，retval\]
</dt> <dd></dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回 **HRESULT**。 可能的值包括 (但不限於) 下表中的這些值。



| 傳回碼                                                                          | 描述                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl> | 此方法已成功。<br/> |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**GetStreamPropertiesOperation**](getstreampropertiesoperation.md)
</dt> </dl>

 

