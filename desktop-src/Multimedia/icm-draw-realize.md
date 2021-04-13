---
title: 'ICM_DRAW_REALIZE 訊息 (Vfw .h) '
description: ICM \_ DRAW 的 \_ 認識訊息會通知轉譯驅動程式，以在繪製時實現其繪圖調色板。 您可以使用 ICDrawRealize 宏明確地傳送此訊息。
ms.assetid: 501540cd-41e2-4f80-abf8-2ec2179970a9
keywords:
- ICM_DRAW_REALIZE message Windows 多媒體
topic_type:
- apiref
api_name:
- ICM_DRAW_REALIZE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd054c16caae55cba25c30098337e54b0ec4b681
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384486"
---
# <a name="icm_draw_realize-message"></a>ICM \_ 繪圖 \_ 實現訊息

**ICM \_ DRAW 的 \_ 認識** 訊息會通知轉譯驅動程式，以在繪製時實現其繪圖調色板。 您可以使用 [**ICDrawRealize**](/windows/desktop/api/Vfw/nf-vfw-icdrawrealize) 宏明確地傳送此訊息。


```C++
ICM_DRAW_REALIZE 
wParam = (DWORD_PTR) (UINT_PTR) (HDC) hdc; 
lParam = (DWORD_PTR) (BOOL) fBackground; 
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="hdc"></span><span id="HDC"></span>*hdc*
</dt> <dd>

用來實現調色板的 DC 控點。

</dd> <dt>

<span id="fBackground"></span><span id="fbackground"></span><span id="FBACKGROUND"></span>*fBackground*
</dt> <dd>

背景旗標。 指定 **TRUE** 以將選擇區視為背景工作，或使用 **FALSE** 來實現前景中的調色板。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果已實現繪圖選擇區，則會傳回 ICERR \_ OK; \_ 如果已實現與解壓縮資料相關聯的元件，則會 ICERR 不支援此選項。

## <a name="remarks"></a>備註

只有當繪圖選擇區與解壓縮的調色板不同時，驅動程式才需要回應此訊息。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                       |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                             |
| 標頭<br/>                   | <dl> <dt>Vfw。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[影片壓縮管理員](video-compression-manager.md)
</dt> <dt>

[影片壓縮訊息](video-compression-messages.md)
</dt> </dl>

 

 





