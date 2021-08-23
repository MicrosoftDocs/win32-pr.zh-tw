---
description: 針對要用於轉送呼叫的影像處理篩選設定新的應用程式回呼。
ms.assetid: 25b86f1d-96c8-4150-9147-13be9b1dd50c
title: 'IWiaImageFilter：： SetNewCallback 方法 (Wia .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaImageFilter.SetNewCallback
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: abb279faba1c5174fc39ebdfe30a4a8cde8cabf86e8b86599f8d3ab9cc3247cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119450488"
---
# <a name="iwiaimagefiltersetnewcallback-method"></a>IWiaImageFilter：： SetNewCallback 方法

針對要用於轉送呼叫的影像處理篩選設定新的應用程式回呼。

## <a name="syntax"></a>語法


```C++
HRESULT SetNewCallback(
  [in] IWiaTransferCallback pWiaTransferCallback
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pWiaTransferCallback* \[在\]
</dt> <dd>

類型： **[ **IWiaTransferCallback**](-wia-iwiatransfercallback.md)**

指定應用程式 [**IWiaTransferCallback**](-wia-iwiatransfercallback.md) 介面的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

請勿直接從您的應用程式呼叫這個方法。

需要有影像處理篩選，才能在設定新的回呼之前釋放先前儲存的應用程式回呼介面。

如果 *pWiaTransferCallback* 為 **Null**，則影像處理篩選器應該只釋出舊的應用程式回呼，並傳回 S \_ OK。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Wia</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Wia .idl</dt> </dl> |



 

 




