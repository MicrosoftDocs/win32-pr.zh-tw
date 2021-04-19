---
title: 'CDM_GETFOLDERPATH 訊息 (Commdlg .h) '
description: 抓取 Explorer 樣式 [開啟] 或 [另存新檔] 對話方塊中目前開啟之資料夾或目錄的路徑。
ms.assetid: 7c3d4598-b45d-46c1-ad0d-cb0ecd20b3eb
keywords:
- CDM_GETFOLDERPATH 訊息對話方塊
topic_type:
- apiref
api_name:
- CDM_GETFOLDERPATH
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fdd6a824892b1a3a31339e36e6a783bb00c08534
ms.sourcegitcommit: 8e083a10b3a480dec8a8d74dbd5889f49dea15e4
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/17/2021
ms.locfileid: "107590935"
---
# <a name="cdm_getfolderpath-message"></a>CDM \_ GETFOLDERPATH 訊息

\[從 Windows Vista 開始，[[一般專案] 對話方塊](/windows/win32/shell/common-file-dialog)已取代 [**開啟**] 和 [**另存** 新檔] 對話方塊。 我們建議您從通用對話方塊程式庫使用通用專案對話方塊 API，而不是這些對話方塊。\]

抓取 Explorer 樣式 [ **開啟** ] 或 [ **另存** 新檔] 對話方塊中目前開啟之資料夾或目錄的路徑。 您必須使用 **OFN \_ EXPLORER** 旗標建立對話方塊; 否則，訊息會失敗。


```C++
#define WM_USER                  0x0400
#define CDM_FIRST               (WM_USER + 100)
#define CDM_GETFOLDERPATH       (CDM_FIRST + 0x0002)
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

*LParam* 緩衝區的大小（以字元為單位）。

</dd> <dt>

*lParam* 
</dt> <dd>

接收路徑之緩衝區的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果訊息成功，傳回值就是路徑字串的大小（以字元為單位），包括結束的 null 字元。 這是複製到緩衝區的位元組數或字元數，如果緩衝區太小，則為所需的緩衝區大小。

如果發生錯誤，則傳回值小於零。

## <a name="remarks"></a>備註

對應的宏如下所示：

``` syntax
int CommDlg_OpenSave_GetFolderPath(hwnd, lparam, wparam); 
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

 

