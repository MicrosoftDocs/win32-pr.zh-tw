---
title: 'LB_GETTEXTLEN 訊息 (Winuser .h) '
description: 取得清單方塊中字串的長度。
ms.assetid: 866730bc-ffd4-42fd-9cea-5d326e129189
keywords:
- LB_GETTEXTLEN message Windows 控制項
topic_type:
- apiref
api_name:
- LB_GETTEXTLEN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1f76bf3574b09b76d5f1010dcb59c8245555dc3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094432"
---
# <a name="lb_gettextlen-message"></a>LB \_ GETTEXTLEN 訊息

取得清單方塊中字串的長度。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

字串之以零為起始的索引。

Windows 95/Windows 98/Windows Millennium Edition (Windows Me) ： *wParam* 參數限制為16位值。 這表示清單方塊不能包含超過32767個專案。 雖然限制專案數目，但清單方塊中專案的總大小（以位元組為單位）只受限於可用的記憶體。

</dd> <dt>

*lParam* 
</dt> <dd>

不使用這個參數。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值是字串的長度（在 **TCHAR** s 中），不包括結束的 null 字元。 在某些情況下，這個值實際上可能大於文字的長度。 如需詳細資訊，請參閱接下來的＜備註＞一節。

如果 *wParam* 參數未指定有效的索引，則傳回值為 LB \_ ERR。

## <a name="remarks"></a>備註

在某些情況下，傳回值大於文字的實際長度。 這種情況會發生在 ANSI 和 Unicode 的特定混合中，而且是因為作業系統允許在文字內的 (DBCS) 字元中存在雙位元組字元集。 不過，傳回值一律會至少與文字的實際長度一樣大：因此，您可以一律使用它來引導緩衝區配置。 當應用程式同時使用 ANSI 函式和使用 Unicode 的通用對話時，就可能會發生這種行為。

若要取得文字的確切長度，請使用 [**WM \_ GETTEXT**](/windows/desktop/winmsg/wm-gettext)、 [**LB \_ GETTEXT**](lb-gettext.md)或 [**CB \_ GETLBTEXT**](cb-getlbtext.md) 訊息或 [**GetWindowText**](/windows/desktop/api/winuser/nf-winuser-getwindowtexta) 函數。

如果清單方塊有擁有者繪製的樣式，而不是 [**磅 \_ HASSTRINGS**](list-box-styles.md) 樣式，則傳回值一律為 **DWORD** 的大小（以位元組為單位）。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**CB \_ GETLBTEXT**](cb-getlbtext.md)
</dt> <dt>

[**LB \_ GETTEXT**](lb-gettext.md)
</dt> <dt>

**其他資源**
</dt> <dt>

[**GetWindowText**](/windows/desktop/api/winuser/nf-winuser-getwindowtexta)
</dt> <dt>

[**WM \_ GETTEXT**](/windows/desktop/winmsg/wm-gettext)
</dt> </dl>

 

