---
title: 'EM_SETELLIPSISMODE 訊息 (Richedit .h) '
description: 這則訊息會設定目前的省略號模式。
ms.assetid: C77263E8-424B-4EDE-ACBF-BA85248FC31F
keywords:
- EM_SETELLIPSISMODE message Windows 控制項
topic_type:
- apiref
api_name:
- EM_SETELLIPSISMODE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81ae3b51dc80ed11d71f4af9c292657b2cf16728
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025386"
---
# <a name="em_setellipsismode-message"></a>EM \_ SETELLIPSISMODE 訊息

這則訊息會設定目前的省略號模式。 啟用時，會針對不符合顯示視窗的文字顯示省略號 ( ) 。 只有當控制項不在作用中時，才會使用省略號。 使用中時，捲軸會用來顯示不符合顯示視窗的文字。


```C++
#define EM_SETELLIPSISMODE       (WM_USER + 306)
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

未使用;必須為零。

</dd> <dt>

*lParam* 
</dt> <dd>

接受下列其中一個值的 DWORD。



| 值                                                                                                                                                         | 意義                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <span id="ELLIPSIS_NONE"></span><span id="ellipsis_none"></span><dl> <dt>**省略號 \_ 無**</dt> </dl> | 不使用省略號。<br/>                |
| <span id="ELLIPSIS_END"></span><span id="ellipsis_end"></span><dl> <dt>**省略號 \_ 結束**</dt> </dl>    | 結束時的省略號 (強制中斷) 。<br/> |
| <span id="ELLIPSIS_WORD"></span><span id="ellipsis_word"></span><dl> <dt>**省略號 \_ 單字**</dt> </dl> | 尾端的省略號 (斷詞) 。<br/>   |



 

這些值的位都符合 **省略號 \_ 遮罩** 的大小。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果 wparam 為0，而 lparam 是上表中的其中一個值，則傳回值等於 TRUE;否則，傳回值等於 FALSE。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>                                            |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Richedit。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**EM \_ GETELLIPSISMODE**](em-getellipsismode.md)
</dt> <dt>

[**EM \_ GETELLIPSISSTATE**](em-getellipsisstate.md)
</dt> </dl>

 

 





