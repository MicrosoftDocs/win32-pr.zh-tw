---
description: 當使用者從 [檔案管理員] 功能表列選取擴充功能的功能表時，傳送至擴充 DLL。 延伸模組可以使用此通知來初始化功能表項目。
title: 'FMEVENT_INITMENU 訊息 (Wfext .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMEVENT_INITMENU
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 8074a09f-ad94-4a7a-8c0b-965b0f8f6334
ms.openlocfilehash: 77b9aa668087f0c02042ccb7e5b822f68596404761d53ec682c76ef98d46c18e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118459045"
---
# <a name="fmevent_initmenu-message"></a>FMEVENT \_ INITMENU 訊息

當使用者從 [檔案管理員] 功能表列選取擴充功能的功能表時，傳送至擴充 DLL。 延伸模組可以使用此通知來初始化功能表項目。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*hmenu* 
</dt> <dd>

[檔案管理員] 功能表列的控制碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果延伸模組 DLL 處理此訊息，則應該傳回零。

## <a name="remarks"></a>備註

只有當使用者選取最上層功能表時，擴充 DLL 才會接收此訊息。 如果延伸模組包含子功能表，則必須在初始化最上層功能表時將它們初始化。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                         |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Wfext。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**FMExtensionProc**](fmextensionproc.md)
</dt> </dl>

 

 




