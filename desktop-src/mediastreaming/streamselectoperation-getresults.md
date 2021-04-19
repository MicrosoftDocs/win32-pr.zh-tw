---
title: StreamSelectOperation. GetResults 方法
description: 傳回 SelectBestStreamAsync 啟動的非同步作業結果。
ms.assetid: 2D9887E7-17C8-4161-984F-FA44591D2052
keywords:
- GetResults 方法媒體串流 API
- GetResults 方法媒體串流 API，StreamSelectOperation 介面
- StreamSelectOperation 介面媒體串流 API，GetResults 方法
topic_type:
- apiref
api_name:
- StreamSelectOperation.GetResults
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c52479949413d32ca54654f355a06a2dee70866e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "106968088"
---
# <a name="streamselectoperationgetresults-method"></a>StreamSelectOperation. GetResults 方法

傳回 [**SelectBestStreamAsync**](/previous-versions/windows/desktop/legacy/hh829001(v=vs.85))啟動的非同步作業結果。

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



| 傳回碼                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl> | 此方法已成功。<br/> |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**StreamSelectOperation**](streamselectoperation.md)
</dt> </dl>

 

