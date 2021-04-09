---
title: 'EM_GETEDITSTYLEEX 訊息 (Richedit .h) '
description: 抓取目前的擴充編輯樣式旗標。
ms.assetid: 3E81F7BB-404D-4465-982A-3CF6FD9359DA
keywords:
- EM_GETEDITSTYLEEX message Windows 控制項
topic_type:
- apiref
api_name:
- EM_GETEDITSTYLEEX
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb4077abaedd0c5ec720603d6b23e77950fd5307
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843684"
---
# <a name="em_geteditstyleex-message"></a>EM \_ GETEDITSTYLEEX 訊息

抓取目前的擴充編輯樣式旗標。


```C++
#define EM_GETEDITSTYLEEX       (WM_USER + 276)
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

未使用;必須為零。

</dd> <dt>

*lParam* 
</dt> <dd>

未使用;必須為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回擴充編輯樣式旗標，其中可包含下列一或多個值。



| 傳回碼                                                                                                | Description                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**SE \_ EX \_ HANDLEFRIENDLYURL**</dt> </dl>  | 如果未使用暫時格式，或使用文字 autocolor (預設值： 0) ，請以相同的文字色彩和底線來顯示易記名稱連結。<br/>                                                                       |
| <dl> <dt>**SE \_ EX 多點 \_ 觸控**</dt> </dl>         | 在 Rich Edit 中啟用觸控支援。 這包括選取專案、插入點位置和內容功能表叫用。 如果未設定此旗標，則觸控是由滑鼠命令模擬，而不會將觸控模式詳細資訊納入考慮 (預設值： 0) 。 <br/>      |
| <dl> <dt>**SE \_ EX \_ NOACETATESELECTION**</dt> </dl> | 使用傳統的 Windows 選取文字和背景色彩來顯示選取的文字，而非背景 acetate 色彩 (預設： 0) 。 <br/>                                                                                                               |
| <dl> <dt>**SE \_ EX \_ NOMATH**</dt> </dl>             | 停用插入數學區域 (預設： 1) 。 若要啟用數學編輯和顯示，請將 *wParam* 設定為0的 [**EM \_ SETEDITSTYLEEX**](em-seteditstyleex.md)訊息，並將 *lParam* 設定為 [ **SES \_ EX \_ NOMATH**]。 <br/>                              |
| <dl> <dt>**\_ \_ 值得注意的 SES**</dt> </dl>            | 停用資料表的插入。 [**EM \_ INSERTTABLE**](em-inserttable.md)訊息會傳回 **E \_ 失敗**，而 RTF 資料表會略過 (預設值： 0) 。 <br/>                                                                                                  |
| <dl> <dt>**SE \_ EX \_ USESINGLELINE**</dt> </dl>      | 啟用多行控制項，其作用就像單行控制項一樣，可以在單行高度大於視窗高度 (預設值： 0) 時垂直捲動。 <br/>                                                                   |
| <dl> <dt>**SE \_ HIDETEMPFORMAT**</dt> </dl>         | 隱藏使用 **tomApplyTmp** 呼叫 [**ITextFont**](/windows/desktop/api/Tom/nf-tom-itextfont-reset)時所建立的暫時格式。 例如，拼寫檢查程式會使用這類格式，在可能拼錯的單字底下顯示彎曲的底線。<br/> |
| <dl> <dt>**SE \_ EX \_ USEMOUSEWPARAM**</dt> </dl>     | 處理 [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove)訊息時，請使用 *wParam* ，而不要呼叫 [**GetAsyncKeyState**](/windows/desktop/api/winuser/nf-winuser-getasynckeystate)。<br/>                                                                                              |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>                                            |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Richedit。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**EM \_ SETEDITSTYLEEX**](em-seteditstyleex.md)
</dt> </dl>

 

