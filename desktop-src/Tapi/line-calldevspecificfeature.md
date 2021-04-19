---
description: TSPI LINE \_ CALLDEVSPECIFICFEATURE 訊息會傳送至 LINEEVENT 回呼函式，以通知 TAPI 有關線路或位址上發生的裝置特定事件。
ms.assetid: bf470f5b-f7e5-4f98-9b60-12da599ebf26
title: 'LINE_CALLDEVSPECIFICFEATURE 訊息 (Tspi .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2891f019035f53be4dbc0a40de429e5c0d9dc567
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000962"
---
# <a name="line_calldevspecificfeature-message"></a>行 \_ CALLDEVSPECIFICFEATURE 訊息

TSPI **LINE \_ CALLDEVSPECIFICFEATURE** 訊息會傳送至 [**LINEEVENT**](/windows/win32/api/tspi/nc-tspi-lineevent) 回呼函式，以通知 TAPI 有關線路或位址上發生的裝置特定事件。 訊息的意義，以及 *dwParam1* 到 *dwParam3* 參數的解讀是裝置特定的。


```C++
            
```



## <a name="parameters"></a>參數

<dl> <dt>

*htLine* 
</dt> <dd>

線路裝置的 TAPI 不透明物件控制碼。

</dd> <dt>

*htCall* 
</dt> <dd>

呼叫裝置的 TAPI 不透明物件控制碼。

</dd> <dt>

*dwMsg* 
</dt> <dd>

值行 \_ CALLDEVSPECIFICFEATURE。

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

## <a name="remarks"></a>備註

服務提供者會搭配 [**TSPI \_ lineDevSpecificFeature**](/windows/win32/api/tspi/nf-tspi-tspi_linedevspecificfeature)函式使用 **LINE \_ CALLDEVSPECIFICFEATURE** 訊息。 其意義是裝置特定的。

TAPI 會將 [**\_ DEVSPECIFICFEATURE**](/previous-versions/windows/desktop/legacy/ms725227(v=vs.85)) 訊息傳送至應用程式，以回應從服務提供者接收此訊息。 *HtLine* 和 *htCall* 參數會轉譯為適當的 *hCall* ，作為 TAPI 層級的 *hDevice* 參數。 *DwParam1*、 *dwParam2* 和 *dwParam3* 參數會透過未修改的傳遞。

在 TAPI 層級沒有直接對應的訊息，但這則訊息與行 DEVSPECIFICFEATURE 非常類似 \_ 。 在 TSPI 層級，裝置專屬的功能訊息會在這些報表事件的行和位址之間進行分割，以及在呼叫上進行報告事件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 2.0 或更新版本<br/>                                             |
| 標頭<br/>       | <dl> <dt>Tspi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**行 \_ DEVSPECIFICFEATURE**](/previous-versions/windows/desktop/legacy/ms725227(v=vs.85))
</dt> <dt>

[**TSPI \_ lineDevSpecificFeature**](/windows/win32/api/tspi/nf-tspi-tspi_linedevspecificfeature)
</dt> </dl>

 

