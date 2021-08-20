---
title: 'TB_ADDSTRING 訊息 (Commctrl .h) '
description: 將新字串加入至工具列的字串集區。
ms.assetid: e22ee2cc-6443-49d3-aea6-a4ab256d4538
keywords:
- TB_ADDSTRING 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- TB_ADDSTRING
- TB_ADDSTRINGA
- TB_ADDSTRINGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0556add41addb4a58d5734ab900af4a43c2018b533723145ed4f9c8272e3890
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119078372"
---
# <a name="tb_addstring-message"></a>TB \_ ADDSTRING 訊息

將新字串加入至工具列的字串集區。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

具有包含字串資源之可執行檔的模組實例控制碼。 如果 *lParam* 改為指向具有一或多個字串的字元陣列，請將此參數設定為 **Null**。

</dd> <dt>

*lParam* 
</dt> <dd>

字串資源的資源識別碼，或 TCHAR 陣列的指標。 請參閱＜備註＞。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回第一個新字串的索引，否則傳回-1。

## <a name="remarks"></a>備註

如果 *wParam* 為 **Null**，則 *lParam* 會指向具有一或多個以 Null 終止之字串的字元陣列。 陣列中的最後一個字串必須以兩個 null 字元做為結束。

如果 *wParam* 為應用程式的 HINSTANCE，或包含字串資源的其他模組，則 *lParam* 是字串的資源識別碼。 字串中的每個專案都必須以任意分隔字元開頭，且字串必須以兩個這類字元結尾。 例如，三個按鈕的文字可能會以 "/New/Open/Save//" 形式出現在字串資料表中。 訊息會在工具列的字串集區中傳回 "New" 的索引，而其他專案則是在連續的位置。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **TB \_ADDSTRINGW** (Unicode) 和 **TB \_ ADDSTRINGA** (ANSI) <br/>                 |



 

 





