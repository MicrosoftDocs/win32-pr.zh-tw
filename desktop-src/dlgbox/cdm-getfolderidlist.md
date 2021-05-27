---
title: 'CDM_GETFOLDERIDLIST 訊息 (Commdlg .h) '
description: 抓取對應于目前開啟之 [Explorer 樣式開啟] 或 [另存新檔] 對話方塊之資料夾的專案識別碼清單位址。
ms.assetid: 9d2d2c35-ff1d-43de-ab0b-c96e0f1e9e24
keywords:
- CDM_GETFOLDERIDLIST 訊息對話方塊
topic_type:
- apiref
api_name:
- CDM_GETFOLDERIDLIST
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb3ffff4f80dc21ed685e589ed4780b43592c2d2
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549703"
---
# <a name="cdm_getfolderidlist-message"></a>CDM \_ GETFOLDERIDLIST 訊息

\[從 Windows Vista 開始，[[一般專案] 對話方塊](../shell/common-file-dialog.md)已取代 [**開啟**] 和 [**另存** 新檔] 對話方塊。 我們建議您從通用對話方塊程式庫使用通用專案對話方塊 API，而不是這些對話方塊。\]

抓取對應于目前開啟之 [Explorer 樣式 **開啟** ] 或 [ **另存** 新檔] 對話方塊之資料夾的專案識別碼清單位址。 您必須使用 **OFN \_ EXPLORER** 旗標建立對話方塊; 否則，訊息會失敗。


```C++
#define WM_USER                  0x0400
#define CDM_FIRST               (WM_USER + 100)
#define CDM_GETFOLDERIDLIST     (CDM_FIRST + 0x0003)
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

*LParam* 緩衝區的大小（以位元組為單位）。

</dd> <dt>

*lParam* 
</dt> <dd>

接收專案識別碼清單的緩衝區指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果訊息成功，則傳回值是專案識別碼清單的大小（以位元組為單位）。 這是複製到緩衝區的位元組數目，如果緩衝區太小，則為所需的緩衝區大小。

如果發生錯誤，則傳回值小於零。

## <a name="remarks"></a>備註

對應的宏如下所示：

``` syntax
int CommDlg_OpenSave_GetFolderIDList(hwnd, lparam, wparam); 
```

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                               |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Commdlg (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**GetOpenFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[**GetSaveFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

**概念**
</dt> <dt>

[通用對話方塊程式庫](common-dialog-box-library.md)
</dt> </dl>

