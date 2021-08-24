---
title: 'MCI_OVLY_WINDOW_PARMS 結構 (Mciapi .h) '
description: MCI \_ OVLY \_ WINDOW \_ PARMS 結構包含適用于影片重迭裝置之 mci \_ 視窗命令的視窗顯示資訊。
ms.assetid: 1189f31e-6e54-4279-a23d-b4e21c6cd276
keywords:
- MCI_OVLY_WINDOW_PARMS 結構 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_OVLY_WINDOW_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd19580dacdc819f35bc36ed8f0070a5fc1b9fc4b745c78711c4fc312611e3c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118138282"
---
# <a name="mci_ovly_window_parms-structure"></a>MCI \_ OVLY \_ 視窗 \_ PARMS 結構

**Mci \_ OVLY \_ WINDOW \_ PARMS** 結構包含適用于影片重迭裝置之 [**mci \_ 視窗**](mci-window.md)命令的視窗顯示資訊。

## <a name="syntax"></a>語法


```C++
typedef struct {
  DWORD_PTR dwCallback;
  HWND      hWnd;
  UINT      nCmdShow;
  LPCTSTR   lpstrText;
} MCI_OVLY_WINDOW_PARMS;
```



## <a name="members"></a>成員

<dl> <dt>

**dwCallback**
</dt> <dd>

低序位字組指定用於 MCI 通知旗標的視窗控制碼 \_ 。

</dd> <dt>

**hWnd**
</dt> <dd>

顯示視窗的控點。

</dd> <dt>

**nCmdShow**
</dt> <dd>

視窗-顯示命令。

</dd> <dt>

**lpstrText**
</dt> <dd>

視窗標題。

</dd> </dl>

## <a name="remarks"></a>備註

將資料指派給此結構的成員時，請在 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85))函數的 *fdwCommand* 參數中設定對應的旗標，以驗證成員。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Mciapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MCI**](mci.md)
</dt> <dt>

[**MCI 結構**](mci-structures.md)
</dt> <dt>

[**MCI \_ 視窗**](mci-window.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

