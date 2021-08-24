---
title: 'EM_GETTEXTEX 訊息 (Richedit .h) '
description: 取得 rich edit 控制項中的文字。
ms.assetid: 46431563-fde1-4407-ab7a-b2248c0e12b8
keywords:
- EM_GETTEXTEX 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- EM_GETTEXTEX
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b116ea27aaff217f949fbd6286a7d8278075486f14f9b9fcec21cf49af2edfd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118006600"
---
# <a name="em_gettextex-message"></a>EM \_ GETTEXTEX 訊息

取得 rich edit 控制項中的文字。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

[**GETTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-gettextex)結構的指標，此結構表示如何在將文字放入輸出緩衝區之前將文字轉譯。

</dd> <dt>

*lParam* 
</dt> <dd>

要接收文字之緩衝區的指標。 這個緩衝區的大小（以位元組為單位）是由 [**GETTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-gettextex)結構的 **cb** 成員所指定。 使用 [**EM \_ GETTEXTLENGTHEX**](em-gettextlengthex.md) 訊息來取得所需的緩衝區大小。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值是複製到輸出緩衝區的 **TCHAR** 數，包括 null 結束字元。

## <a name="remarks"></a>備註

如果輸出緩衝區的大小小於控制項中文字的大小，則編輯控制項會從開頭複製文字，並將它放在緩衝區中，直到緩衝區已滿為止。 終止的 null 字元仍會放置在緩衝區的結尾。

如果要求 ANSI 文字， **EM \_ GETTEXTEX** 會使用 [**WideCharToMultiByte**](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte) 函數將 Unicode 字元轉譯為 ansi。 它可讓您使用特定字碼頁，從 Unicode 移至 ANSI。 [**GETTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-gettextex)結構包含 (**lpDefaultChar** 和 **lpUsedDefChar**) 的成員，這些成員會用於從 Unicode 翻譯為 ANSI。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Richedit。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**EM \_ SETTEXTEX**](em-settextex.md)
</dt> <dt>

[**GETTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-gettextex)
</dt> <dt>

**其他資源**
</dt> <dt>

[**WideCharToMultiByte**](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte)
</dt> <dt>

[**WM \_ SETTEXT**](/windows/desktop/winmsg/wm-settext)
</dt> </dl>

 

