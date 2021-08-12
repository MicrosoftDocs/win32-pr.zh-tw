---
title: 'BM_SETIMAGE 訊息 (Winuser .h) '
description: 將新影像 (圖示或點陣圖) 與按鈕產生關聯。
ms.assetid: bf05e684-63d0-4583-960b-f329edafb151
keywords:
- BM_SETIMAGE 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- BM_SETIMAGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b8948c73c04d3b01230a47ab91529764c9e20281e4f45803f71d82f59dedb14
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118674811"
---
# <a name="bm_setimage-message"></a>BM \_ SETIMAGE 訊息

將新影像 (圖示或點陣圖) 與按鈕產生關聯。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

要與按鈕相關聯的影像類型。 這個參數可以是下列其中一個值：

-   影像 \_ 點陣圖
-   影像 \_ 圖示

</dd> <dt>

*lParam* 
</dt> <dd>

 (**HICON** 或) **HBITMAP** 的控制碼，以與按鈕相關聯的影像。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值是先前與按鈕相關聯之影像的控制碼（如果有的話）。否則，它會是 **Null**。

## <a name="remarks"></a>備註

按鈕控制項上的文字、圖示或兩者的外觀取決於 [**BS \_ 圖示**](button-styles.md) 和 [**BS \_ 點陣圖**](button-styles.md) 樣式，以及是否呼叫 **BM \_ SETIMAGE** 訊息。 可能的結果如下所示：



| BS \_ 圖示或 BS \_ 點陣圖集合？ | \_呼叫 BM SETIMAGE？ | 結果              |
|-----------------------------|----------------------|---------------------|
| 是                         | 是                  | 僅顯示圖示。     |
| 否                          | 是                  | 顯示圖示和文字。 |
| 是                         | 否                   | 只顯示文字。     |
| 否                          | 否                   | 只顯示文字      |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含 Windows .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**BM \_ GETIMAGE**](bm-getimage.md)
</dt> </dl>

 

 





