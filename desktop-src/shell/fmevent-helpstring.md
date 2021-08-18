---
description: 當檔案管理員需要功能表或工具列命令專案的說明字串時，傳送至檔案管理員延伸模組 DLL 程式。
title: 'FMEVENT_HELPSTRING 訊息 (Wfext .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMEVENT_HELPSTRING
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 55fb5bfe-2889-40e5-9798-85f63727e31f
ms.openlocfilehash: 06e3c13841c6b4dc85c2a1dcbea7dce18a15ab054ffb2953fa2e3ba2999d5863
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119094153"
---
# <a name="fmevent_helpstring-message"></a>FMEVENT \_ HELPSTRING 訊息

當檔案管理員需要功能表或工具列命令專案的說明字串時，傳送至檔案管理員延伸模組 DLL 程式。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lpfmshs* 
</dt> <dd>

[**FMS \_ HELPSTRING**](fms-helpstring.md)結構的位址，此結構會傳達命令專案說明字串資料。 **FMS \_ HELPSTRING** 結構會識別需要說明字串的命令專案，以及其功能表的控制碼。 然後，應用程式會將適當的說明字串寫入 **FMS \_ HELPSTRING** 結構的 **szHelp** 成員。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果延伸 DLL 程式處理此訊息，則應該傳回零。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                         |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Wfext。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**FMExtensionProc**](fmextensionproc.md)
</dt> <dt>

[**FMEVENT \_ HELPMENUITEM**](fmevent-helpmenuitem.md)
</dt> </dl>

 

 




