---
description: '\_當指定的線路裝置已強制關閉時，就會傳送 TAPI 線路關閉訊息。 一旦傳送此訊息之後，行裝置控制碼或該行的任何呼叫控制碼將不再有效。'
ms.assetid: f254e331-d574-4fa7-8447-6e4535d3d773
title: 'LINE_CLOSE 訊息 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68fec993987bfc3ca36099d90eed2beadde9a749f965a36ebb6c513c210f387b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119682398"
---
# <a name="line_close-message"></a>行 \_ 關閉訊息

當指定的線路裝置已強制關閉時，就會傳送 TAPI **線路 \_ 關閉** 訊息。 一旦傳送此訊息之後，行裝置控制碼或該行的任何呼叫控制碼將不再有效。


```C++
            
```



## <a name="parameters"></a>參數

<dl> <dt>

*hDevice* 
</dt> <dd>

已關閉之線路裝置的控制碼。 這個控制碼已不再有效。

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

開啟行時所提供的回呼實例。

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

只有在 TAPI 服務提供者 (TSP) 強制關閉開啟行後，才會將 **行 \_ 關閉** 訊息傳送至任何應用程式。 是否可以在強制關閉之後立即重新開啟行，就是裝置特定的。

造成的狀況可能是狀態的重大變更、硬體錯誤、伺服器的連線中斷，或甚至可能防止單一應用程式獨佔線路裝置的時間太長。 在使用者修改該行或其驅動程式的設定之後，也可以強制關閉線路裝置。 如果使用者想要讓設定變更立即生效 (而不是在下一次系統重新開機) 後，它們會影響應用程式目前的裝置視圖 (例如裝置功能) 的變更，則服務提供者可以強制關閉線路裝置。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 2.0 或更新版本<br/>                                             |
| 標頭<br/>       | <dl> <dt>Tapi</dt> </dl> |



 

 




