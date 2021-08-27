---
title: 'HDM_GETORDERARRAY 訊息 (Commctrl .h) '
description: 取得標題控制項中專案的目前由左到右的順序。 您可以明確地傳送此訊息，或使用標頭 \_ GetOrderArray 宏。
ms.assetid: b287d3c1-ae61-41a4-a884-dc008eb24ad8
keywords:
- HDM_GETORDERARRAY 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- HDM_GETORDERARRAY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f374424fe3f1d84c4919c26948486a9bae1660072975556aecaac4b08b85b33b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062828"
---
# <a name="hdm_getorderarray-message"></a>HDM \_ GETORDERARRAY 訊息

取得標題控制項中專案的目前由左到右的順序。 您可以明確地傳送此訊息，或使用 [**標頭 \_ GetOrderArray**](/windows/desktop/api/Commctrl/nf-commctrl-header_getorderarray) 宏。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

*LParam* 可保存的整數元素數目。 這個值必須等於控制項中的專案數 (請參閱 [**HDM \_ GETITEMCOUNT**](hdm-getitemcount.md)) 。

</dd> <dt>

*lParam* 
</dt> <dd>

整數陣列的指標，可接收標頭中專案的索引值。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則會傳回非零，而 *lParam* 的緩衝區會接收標題控制項中每個專案的專案編號（依其出現的順序，由左至右排列）。 否則，訊息會傳回零。

## <a name="remarks"></a>備註

*LParam* 中的元素數目是在 *wParam* 中指定，而且必須等於控制項中的專案數。 例如，下列程式碼片段會保留足夠的記憶體來保存索引值。


```
int iItems,

    *lpiArray;



// Get memory for buffer.

(iItems = SendMessage(hwndHD, HDM_GETITEMCOUNT, 0,0))!=-1)

    if(!(lpiArray = calloc(iItems,sizeof(int))))

MessageBox(hwnd, "Out of memory.","Error", MB_OK);
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





