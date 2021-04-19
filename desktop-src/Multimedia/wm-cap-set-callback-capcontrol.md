---
title: 'WM_CAP_SET_CALLBACK_CAPCONTROL 訊息 (Vfw .h) '
description: WM \_ CAP \_ SET \_ 回呼 \_ CAPCONTROL 訊息會在應用程式中設定回呼函式，以提供精確的錄製控制項。 您可以使用 capSetCallbackOnCapControl 宏明確地傳送此訊息。
ms.assetid: 1e93ed7b-8205-45fe-bdcf-efe3f709f728
keywords:
- WM_CAP_SET_CALLBACK_CAPCONTROL message Windows 多媒體
topic_type:
- apiref
api_name:
- WM_CAP_SET_CALLBACK_CAPCONTROL
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7fda38bbc79461b7c5ccaf9b3a32c2c3a0f9e3e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969177"
---
# <a name="wm_cap_set_callback_capcontrol-message"></a>WM \_ CAP \_ 設定 \_ 回呼 \_ CAPCONTROL 訊息

**WM \_ CAP \_ SET \_ 回呼 \_ CAPCONTROL** 訊息會在應用程式中設定回呼函式，以提供精確的錄製控制項。 您可以使用 [**capSetCallbackOnCapControl**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackoncapcontrol) 宏明確地傳送此訊息。


```C++
WM_CAP_SET_CALLBACK_CAPCONTROL 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (fpProc); 
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*
</dt> <dd>

回呼函數的指標，其類型為 [**capControlCallback**](/windows/desktop/api/Vfw/nc-vfw-capcontrolcallback)。 針對此參數指定 **Null** ，以停用先前安裝的回呼函數。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回 **TRUE** ; 如果串流處理捕獲或單一框架捕獲會話正在進行中，則傳回 **FALSE** 。

## <a name="remarks"></a>備註

單一回呼函式可用來讓應用程式精確地控制串流處理的開始和完成時間。 捕捉視窗會先呼叫 *nState* 設定為 CONTROLCALLBACK 預先處理的程式 \_ ，然後再配置所有緩衝區，並完成所有其他的捕獲準備工作。 如此一來，應用程式就可以預先產生影片來源，從回呼函式在確切的錄音開始時傳回。 回呼函式中 **TRUE** 的傳回值會繼續捕捉，並傳回 **FALSE** 中止捕捉的傳回值。 開始 capture 之後，會經常呼叫此回呼函式，並將 *nState* 設定為 CONTROLCALLBACK capture，藉 \_ 由傳回 **FALSE** 來允許應用程式結束捕捉。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                       |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                             |
| 標頭<br/>                   | <dl> <dt>Vfw。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[影片捕獲](video-capture.md)
</dt> <dt>

[影片捕獲訊息](video-capture-messages.md)
</dt> </dl>

 

 





