---
title: 'LB_ADDFILE 訊息 (Winuser .h) '
description: 將指定的檔案名加入包含目錄清單的清單方塊中。
ms.assetid: 60426293-779b-4a4b-95a2-4901b5f6a13b
keywords:
- LB_ADDFILE 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- LB_ADDFILE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8077bda3015fef36d6383f37f272ddaf25469fcb6930bb38bd0fa8122efc5b55
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119434478"
---
# <a name="lb_addfile-message"></a>LB \_ ADDFILE 訊息

將指定的檔案名加入包含目錄清單的清單方塊中。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

不使用這個參數。

</dd> <dt>

*lParam* 
</dt> <dd>

緩衝區的指標，指定要加入的檔案名。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值是已加入之檔案的以零為起始的索引，如果發生錯誤，則為 LB \_ ERR。

## <a name="remarks"></a>備註

*LParam* 要加入的清單方塊必須已由 [**DlgDirList**](/windows/desktop/api/Winuser/nf-winuser-dlgdirlista)函數填滿。

[**LB \_ INITSTORAGE**](lb-initstorage.md)訊息有助於加速初始化具有大量專案 (超過 100) 的清單方塊。 它會保留指定的記憶體數量，讓後續的 **LB \_ ADDFILE** 訊息能以最短的時間進行。 您可以使用 *wParam* 和 *lParam* 參數的估計值。 如果您高估值，則會配置額外的記憶體;如果您低估了，一般配置會用於超出要求數量的專案。

若為 ANSI 應用程式，系統會使用 CP ACP 將清單方塊中的文字轉換成 Unicode \_ 。 這可能會造成問題。 例如，日文 Windows 的非 Unicode 清單方塊中有重音的羅馬字元，將會出現混亂。 若要修正此問題，請將應用程式編譯為 Unicode 或使用主控描繪清單方塊。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含 Windows .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**DlgDirList**](/windows/desktop/api/Winuser/nf-winuser-dlgdirlista)
</dt> <dt>

[**LB \_ ADDSTRING**](lb-addstring.md)
</dt> </dl>

 

 





