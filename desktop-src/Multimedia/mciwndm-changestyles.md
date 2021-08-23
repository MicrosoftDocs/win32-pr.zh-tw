---
title: 'MCIWNDM_CHANGESTYLES 訊息 (Vfw .h) '
description: MCIWNDM \_ CHANGESTYLES 訊息會變更 MCIWnd 視窗所使用的樣式。 您可以使用 MCIWndChangeStyles 宏明確地傳送此訊息。
ms.assetid: 9074c21a-e49f-4089-a6d2-af8d513cb632
keywords:
- MCIWNDM_CHANGESTYLES 訊息 Windows 多媒體
topic_type:
- apiref
api_name:
- MCIWNDM_CHANGESTYLES
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5525066f4c377cc093e1e7a0dedd4edf7463792c136214a519da9744917cbc89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119525508"
---
# <a name="mciwndm_changestyles-message"></a>MCIWNDM \_ CHANGESTYLES 訊息

**MCIWNDM \_ CHANGESTYLES** 訊息會變更 MCIWnd 視窗所使用的樣式。 您可以使用 [**MCIWndChangeStyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndchangestyles) 宏明確地傳送此訊息。


```C++
MCIWNDM_CHANGESTYLES 
wParam = (WPARAM) (UINT) mask; 
lParam = (LPARAM) (LONG) value; 
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="mask"></span><span id="MASK"></span>*面具*
</dt> <dd>

識別可變更之樣式的遮罩。 這個遮罩是將允許變更之所有樣式的位 OR 運算子。

</dd> <dt>

<span id="value"></span><span id="VALUE"></span>*價值*
</dt> <dd>

視窗的新樣式設定。 針對此參數指定零，以關閉遮罩中識別的所有樣式。 如需可用樣式的清單，請參閱 [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) 函數。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回零。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                       |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                             |
| 標頭<br/>                   | <dl> <dt>Vfw。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea)
</dt> <dt>

[**MCIWndChangeStyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndchangestyles)
</dt> </dl>

 

 





