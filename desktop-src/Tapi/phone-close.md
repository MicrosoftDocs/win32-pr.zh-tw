---
description: '\_當已在資源回收中強制關閉開啟的電話裝置時，就會傳送 TAPI 電話關閉訊息。 傳送此訊息之後，裝置控制碼已不再有效。'
ms.assetid: 84650abf-235e-4792-a67d-2f0f08b85a32
title: 'PHONE_CLOSE 訊息 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d9a7641b437a10098806fc7ad52aa64200ca015
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993383"
---
# <a name="phone_close-message"></a>電話 \_ 關閉訊息

當已在資源回收中強制關閉開啟的電話裝置時，就會傳送 TAPI **電話 \_ 關閉** 訊息。 傳送此訊息之後，裝置控制碼已不再有效。


```C++
            
```



## <a name="parameters"></a>參數

<dl> <dt>

*hPhone* 
</dt> <dd>

已關閉之 open phone 裝置的控制碼。 傳送此訊息之後，控制碼已不再有效。

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

開啟手機裝置時提供的應用程式回呼實例。

</dd> <dt>

*dwParam1* 
</dt> <dd>

未使用的。

</dd> <dt>

*dwParam2* 
</dt> <dd>

未使用的。

</dd> <dt>

*dwParam3* 
</dt> <dd>

未使用的。

</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="remarks"></a>備註

只有在已強制關閉開啟的電話之後，才會將 **電話 \_ 關閉** 訊息傳送至應用程式。 這麼做是為了防止單一應用程式將手機裝置獨佔太長的時間。 是否可以在強制關閉之後立即重新開啟電話，即裝置特定。

在使用者修改該電話的設定或其驅動程式之後，也可以強制關閉開啟的電話裝置。 如果使用者想要讓設定變更立即生效 (而不是在下一次系統重新開機) 之後，而這些變更會影響應用程式目前的裝置視圖 (例如裝置功能) 的變更，則服務提供者可以強制關閉電話裝置。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 2.0 或更新版本<br/>                                             |
| 標頭<br/>       | <dl> <dt>Tapi</dt> </dl> |



 

 




