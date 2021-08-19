---
title: 'LBSELCHSTRING message (Commdlg) '
description: '[開啟] 或 [另存新檔] 對話方塊會在對話方塊的任何清單方塊或下拉式方塊中選取的專案變更時，將已註冊的 LBSELCHSTRING 訊息傳送至您的勾點程式。'
ms.assetid: 3a8ebc63-b324-43ed-bb6f-34779f6043e7
keywords:
- LBSELCHSTRING 訊息對話方塊
topic_type:
- apiref
api_name:
- LBSELCHSTRING
- LBSELCHSTRINGA
- LBSELCHSTRINGW
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea804e1bd5ad35b5ad5d5ee98cf77f97d54e4e93f438e6e32ad7478e10d7b9ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118985398"
---
# <a name="lbselchstring-message"></a>LBSELCHSTRING 訊息

\[從 Windows Vista 開始，[[一般專案] 對話方塊](../shell/common-file-dialog.md)已取代 [**開啟**] 和 [**另存** 新檔] 對話方塊。 我們建議您從通用對話方塊程式庫使用通用專案對話方塊 API，而不是這些對話方塊。\]

[ **開啟** ] 或 [ **另存** 新檔] 對話方塊會在對話方塊的任何清單方塊或下拉式方塊中選取的專案變更時，將已註冊的 **LBSELCHSTRING** 訊息傳送至您的勾點程式。


```C++
#define LBSELCHSTRING TEXT("commdlg_LBSelChangedNotify")
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

選取範圍變更之清單方塊或下拉式方塊的識別碼。

</dd> <dt>

*lParam* 
</dt> <dd>

低序位字組會在清單方塊或下拉式方塊中指定選取之字串的專案編號。 高序位字組指定選取範圍變更的類型。 此參數可以是下列其中一個值。



| 值                                                                                                                                                                                                                       | 意義                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="CD_LBSELCHANGE"></span><span id="cd_lbselchange"></span><dl> <dt>**CD \_LBSELCHANGE**</dt> <dt>0</dt> </dl>     | 專案是單一選取清單方塊中唯一選取的專案。<br/>      |
| <span id="CD_LBSELADD"></span><span id="cd_lbseladd"></span><dl> <dt>**CD \_LBSELADD**</dt> <dt>2</dt> </dl>              | 專案是在多重選取清單方塊中選取的其中一個專案。<br/> |
| <span id="CD_LBSELSUB"></span><span id="cd_lbselsub"></span><dl> <dt>**CD \_LBSELSUB**</dt> <dt>1</dt> </dl>              | 在多重選取清單方塊中，不會再選取該專案。<br/>        |
| <span id="CD_LBSELNOITEMS"></span><span id="cd_lbselnoitems"></span><dl> <dt>**CD \_LBSELNOITEMS**</dt> <dt>-1</dt> </dl> | 多重選取清單方塊中沒有任何專案存在。<br/>                        |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

此訊息沒有傳回值。

## <a name="remarks"></a>備註

攔截程式必須在 [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)函數的呼叫中指定 **LBSELCHSTRING** 常數，以取得對話方塊所傳送之訊息的識別碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                               |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Commdlg (包含 Windows .h) </dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **LBSELCHSTRINGW** (Unicode) 和 **LBSELCHSTRINGA** (ANSI) <br/>                                    |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**CDN \_SELCHANGE**](cdn-selchange.md)
</dt> <dt>

[**CDN \_TYPECHANGE**](cdn-typechange.md)
</dt> <dt>

[**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

**概念**
</dt> <dt>

[通用對話方塊程式庫](common-dialog-box-library.md)
</dt> </dl>

