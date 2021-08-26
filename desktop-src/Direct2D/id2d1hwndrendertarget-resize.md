---
title: 'ID2D1HwndRenderTarget 調整大小方法 (D2d1 .h) '
description: 將呈現目標的大小變更為指定的圖元大小。
ms.assetid: b8ea2e96-c69b-4018-9572-c9099bf6202d
keywords:
- 調整方法 Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 31ffcae6473924e12ca428fd48927fd1507840dce4fdbce3a18e8f82ffe9fcaf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119917608"
---
# <a name="id2d1hwndrendertargetresize-methods"></a>ID2D1HwndRenderTarget：： Resize 方法

將呈現目標的大小變更為指定的圖元大小。

### <a name="overload-list"></a>多載清單



| 方法                                                                         | 描述                                                                    |
|:-------------------------------------------------------------------------------|:-------------------------------------------------------------------------------|
| [**調整 (D2D1 \_ 大小 \_ U&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1hwndrendertarget-resize(constd2d1_size_u_))  | 將呈現目標的大小變更為指定的圖元大小。 <br/> |
| [**調整 (D2D1 \_ 大小 \_ U \*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1hwndrendertarget-resize(constd2d1_size_u)) | 將呈現目標的大小變更為指定的圖元大小。<br/>  |



## <a name="remarks"></a>備註

呼叫這個方法之後，即使在建立轉譯目標時指定了 [ [**D2D1 \_ 目前的 \_ 選項 \_ 保留 \_ 內容**](/windows/win32/api/d2d1/ne-d2d1-d2d1_present_options) ] 選項，也不會定義轉譯目標的背景緩衝區內容。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D2d1。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>D2d1 .lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ID2D1HwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85))
</dt> </dl>

�

�
