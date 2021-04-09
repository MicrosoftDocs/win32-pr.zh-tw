---
title: 'TB_ADDBITMAP 訊息 (Commctrl .h) '
description: 將一或多個影像新增至適用于工具列的按鈕影像清單。
ms.assetid: 9040ab84-a5f3-4e4b-bc90-590b2ceeaa5a
keywords:
- TB_ADDBITMAP message Windows 控制項
topic_type:
- apiref
api_name:
- TB_ADDBITMAP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d83cba4b4dec9b490a3e8f41db9cc7721dd23b08
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686663"
---
# <a name="tb_addbitmap-message"></a>TB \_ ADDBITMAP 訊息

將一或多個影像新增至適用于工具列的按鈕影像清單。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

點陣圖中的按鈕影像數目。 如果 *lParam* 指定系統定義的點陣圖，則會忽略這個參數。

</dd> <dt>

*lParam* 
</dt> <dd>

[**TBADDBITMAP**](/windows/win32/api/commctrl/ns-commctrl-tbaddbitmap)結構的指標，其中包含點陣圖資源的識別碼，以及包含點陣圖資源之可執行檔的模組實例控制碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回第一個新影像的索引，否則傳回-1。

## <a name="remarks"></a>備註

如果工具列是使用 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) 函式所建立，您必須先將 [**tb \_ BUTTONSTRUCTSIZE**](tb-buttonstructsize.md) 訊息傳送至工具列，然後再傳送 **tb \_ ADDBITMAP**。

## <a name="examples"></a>範例

下列範例會從資源建立點陣圖 (.IDB \_ BITMAP1) 、在此) 案例中，將背景色彩對應 (黑色，然後將其新增至工具列。


```C++
DWORD backgroundColor = GetSysColor(COLOR_BTNFACE);
COLORMAP colorMap;
colorMap.from = RGB(0, 0, 0);
colorMap.to = backgroundColor;
HBITMAP hbm = CreateMappedBitmap(g_hInst, IDB_BITMAP1, 0, &colorMap, 1);
TBADDBITMAP tb;
tb.hInst = NULL;
tb.nID = (UINT_PTR)hbm;

// hWndToolbar is the window handle of the toolbar.
// Do not forget to send TB_BUTTONSTRUCTSIZE if the toolbar was 
// created by using CreateWindowEx.
int index = SendMessage (hWndToolbar, TB_ADDBITMAP, 0, (LPARAM)&tb);
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

