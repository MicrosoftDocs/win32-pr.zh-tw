---
description: 可由 DXGI 函數傳回的狀態碼。
ms.assetid: dd7480b4-8218-4716-ab9f-74a9955b8aa7
title: 'DXGI_STATUS (DXGI. h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b39c402880ccdcbda009402d56127e70a61543d0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106993876"
---
# <a name="dxgi_status"></a>DXGI \_ 狀態

可由 DXGI 函數傳回的狀態碼。



| 常數/值                                                                                                                                                                                                                                                                                      | Description                                                                                                                                                                                                                                                                                              |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DXGI_STATUS_OCCLUDED"></span><span id="dxgi_status_occluded"></span><dl> <dt>**DXGI \_狀態 \_ pixels occluded**</dt> <dt>0x087A0001</dt> </dl>                                                 | 視窗內容是不可見的。 收到此狀態時，應用程式可能會停止轉譯，並使用 DXGI \_ 目前的 \_ 測試來判斷何時要繼續轉譯。 \_ \_ 如果您要使用翻轉模型交換鏈，您將不會收到 DXGI 狀態 pixels occluded。<br/>                                                                                                                           |
| <span id="DXGI_STATUS_MODE_CHANGED"></span><span id="dxgi_status_mode_changed"></span><dl> <dt>**DXGI \_狀態 \_ 模式 \_ 已變更**</dt> <dt>0x087A0007</dt> </dl>                                    | 桌面顯示模式已變更，可能有色彩轉換/延展。 應用程式應該呼叫 [**IDXGISwapChain：： ResizeBuffers**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-resizebuffers) ，以符合新的顯示模式。<br/>                                                                       |
| <span id="DXGI_STATUS_MODE_CHANGE_IN_PROGRESS"></span><span id="dxgi_status_mode_change_in_progress"></span><dl> <dt>**DXGI \_狀態 \_ 模式 \_ 變更 \_ \_ 進行中**</dt> <dt>0x087A0008</dt> </dl> | 如果呼叫任一個 API 時， [**IDXGISwapChain：： ResizeTarget**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-resizetarget)和 [**IDXGISwapChain：： SETFULLSCREENSTATE**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-setfullscreenstate)會傳回 DXGI \_ 狀態 \_ 模式 \_ 變更 \_ \_ 進行中。<br/> |



## <a name="remarks"></a>備註

每個 **DXGI \_ 狀態值** 的 **HRESULT** 值都是由 DXGItype 中定義的這個宏所決定：


```
#define _FACDXGI    0x87a
#define MAKE_DXGI_STATUS(code)  MAKE_HRESULT(0, _FACDXGI, code)
```



例如，已將 **DXGI \_ 狀態 \_ Pixels occluded** 定義為 **0x087A0001**：


```
#define DXGI_STATUS_OCCLUDED                    MAKE_DXGI_STATUS(1)
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-----------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>DXGI。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[DXGI 常數](d3d10-graphics-reference-dxgi-constants.md)
</dt> </dl>

 

 




