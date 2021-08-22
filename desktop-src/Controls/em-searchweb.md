---
title: 'EM_SEARCHWEB 訊息 (Commctrl .h) '
description: 開啟瀏覽器，並使用選取的文字做為搜尋字詞來執行 web 搜尋。
ms.assetid: 1b1ff5e7-e0b8-40c1-8b7e-7003e9ef959b
keywords:
- EM_SEARCHWEB 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- EM_SEARCHWEB
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21523df67acf91b8a44f59ea40b012f1af7c287185b7ac64b5dc1288005dfb17
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118673174"
---
# <a name="em_searchweb-message"></a>EM \_ SEARCHWEB 訊息

開啟瀏覽器，並使用選取的文字做為搜尋字詞來執行 web 搜尋。

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

此訊息不會傳回值。

## <a name="remarks"></a>備註

如果使用 [**EM \_ ENABLESEARCHWEB**](em-enablesearchweb.md) 訊息停用「搜尋 web」功能，則此訊息不會有任何作用。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10， \[ 僅限 1809 desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2019 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**EM \_ ENABLESEARCHWEB**](em-enablesearchweb.md)
</dt> </dl>

 

 





