---
description: 當檔案管理員載入 DLL 時，傳送至擴充 DLL。
ms.assetid: 9d673ab8-c468-4b46-b96e-1adfaa9f85fb
title: 'FMEVENT_LOAD 訊息 (Wfext .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMEVENT_LOAD
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.openlocfilehash: de7a950e3f17c9b2cee2b66a047d289ca29b6b56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104973225"
---
# <a name="fmevent_load-message"></a>FMEVENT \_ 載入訊息

當檔案管理員載入 DLL 時，傳送至擴充 DLL。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

必須為零。

</dd> <dt>

*lpfmsld* 
</dt> <dd>

[**FMS \_ 載入**](fms-load.md)結構的位址，指定功能表項目差異值。

</dd> </dl>

## <a name="return-value"></a>傳回值

延伸模組 DLL 必須傳回 **TRUE** ，才能繼續載入 DLL。 如果 DLL 傳回 **FALSE**，則 [檔案管理員] 會呼叫 [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) 函式，並結束與延伸模組 DLL 的任何通訊。

## <a name="remarks"></a>備註

應用程式應該填滿 [**FMS \_ 載入**](fms-load.md)結構中的 **DwSize**、 **szMenuName** 和 **hMenu** 成員。 它也應該儲存 **wMenuDelta** 成員的值，並在修改功能表時使用它來識別功能表項目。

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

 

 
