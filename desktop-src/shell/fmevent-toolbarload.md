---
description: 當檔案管理員載入其工具列時，傳送至擴充 DLL。 此訊息可讓延伸模組 DLL 將按鈕新增至 [檔案管理員] 工具列。
title: 'FMEVENT_TOOLBARLOAD 訊息 (Wfext .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMEVENT_TOOLBARLOAD
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: c5daab49-4ed5-439b-b1b7-a87f70c379f0
ms.openlocfilehash: c4195acedbd696679a2deea2f4d6e268717566d1
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841269"
---
# <a name="fmevent_toolbarload-message"></a>FMEVENT \_ TOOLBARLOAD 訊息

當檔案管理員載入其工具列時，傳送至擴充 DLL。 此訊息可讓延伸模組 DLL 將按鈕新增至 [檔案管理員] 工具列。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lpfmstbl* 
</dt> <dd>

[**FMS \_ TOOLBARLOAD**](fms-toolbarload.md)結構的位址。 如果延伸模組 DLL 將按鈕新增至 [檔案管理員] 中的工具列，則 DLL 應以按鈕的相關資訊填入結構。

</dd> </dl>

## <a name="return-value"></a>傳回值

延伸模組 DLL 必須傳回 **TRUE** ，才能將按鈕加入至工具列。 如果 DLL 傳回 **FALSE**，則 [檔案管理員] 不會加入按鈕。

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

 

 




