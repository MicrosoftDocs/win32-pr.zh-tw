---
description: TAPI 會將電話 \_ DEVSPECIFIC 訊息傳送至應用程式，以通知應用程式發生在電話上的裝置特定事件。 訊息的意義和參數的解讀是實作為定義。
ms.assetid: e3e803dd-b041-48b7-9acf-a89989370204
title: 'PHONE_DEVSPECIFIC 訊息 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 578ba0960963f85ff597d9a6bc87ff3369a6c837ed58367bd82d62a13341e988
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120072898"
---
# <a name="phone_devspecific-message"></a>電話 \_ DEVSPECIFIC 訊息

TAPI 會將 **電話 \_ DEVSPECIFIC** 訊息傳送至應用程式，以通知應用程式發生在電話上的裝置特定事件。 訊息的意義和參數的解讀是實作為定義。


```C++
            
```



## <a name="parameters"></a>參數

<dl> <dt>

*hPhone* 
</dt> <dd>

手機裝置的控制碼。

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

開啟手機裝置時提供的應用程式回呼實例。

</dd> <dt>

*dwParam1* 
</dt> <dd>

特定裝置。

</dd> <dt>

*dwParam2* 
</dt> <dd>

特定裝置。

</dd> <dt>

*dwParam3* 
</dt> <dd>

特定裝置。

</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 2.0 或更新版本<br/>                                             |
| 標頭<br/>       | <dl> <dt>Tapi</dt> </dl> |



 

 




