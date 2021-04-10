---
title: 'EM_GETELLIPSISMODE 訊息 (Richedit .h) '
description: 抓取目前的省略號模式。
ms.assetid: 01A755F3-6C6E-4974-9866-76BF15E0F3AD
keywords:
- EM_GETELLIPSISMODE message Windows 控制項
topic_type:
- apiref
api_name:
- EM_GETELLIPSISMODE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09b7273cbfd6e87b4591c00267860c9a164aad5e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103787"
---
# <a name="em_getellipsismode-message"></a>EM \_ GETELLIPSISMODE 訊息

抓取目前的省略號模式。 啟用時，會針對不符合顯示視窗的文字顯示省略號 ( ) 。 只有當控制項不在使用中時，才會使用省略號。 使用中時，捲軸會用來顯示不符合顯示視窗的文字。


```C++
#define EM_GETELLIPSISMODE       (WM_USER + 305)
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

未使用;必須為零。

</dd> <dt>

*lParam* 
</dt> <dd>

接收下列其中一個值的 DWORD 指標。



| 值                                                                                                                                                         | 意義                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <span id="ELLIPSIS_NONE"></span><span id="ellipsis_none"></span><dl> <dt>**省略號 \_ 無**</dt> </dl> | 不使用省略號。<br/>                |
| <span id="ELLIPSIS_END"></span><span id="ellipsis_end"></span><dl> <dt>**省略號 \_ 結束**</dt> </dl>    | 結束時的省略號 (強制中斷) 。<br/> |
| <span id="ELLIPSIS_WORD"></span><span id="ellipsis_word"></span><dl> <dt>**省略號 \_ 單字**</dt> </dl> | 尾端的省略號 (斷詞) 。<br/>   |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

如果 wparam 為0，而 lparam 不是 Null，則傳回值等於 TRUE;否則，傳回值等於 FALSE。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>                                            |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Richedit。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**EM \_ SETELLIPSISMODE**](em-setellipsismode.md)
</dt> <dt>

[**EM \_ GETELLIPSISSTATE**](em-getellipsisstate.md)
</dt> </dl>

 

 





