---
title: 'EM_GETPAGEROTATE 訊息 (Richedit .h) '
description: 取得 Microsoft Rich Edit 控制項的文字版面配置。
ms.assetid: 0efb112e-ad51-4ebb-9037-3aee3ab9ad1d
keywords:
- EM_GETPAGEROTATE message Windows 控制項
topic_type:
- apiref
api_name:
- EM_GETPAGEROTATE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad7bc7cd3c77ae88cd4c8710e14b4472e57407ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466560"
---
# <a name="em_getpagerotate-message"></a>EM \_ GETPAGEROTATE 訊息

\[**EM \_GETPAGEROTATE** 可用於 [需求] 區段中指定的作業系統。 它在後續版本中可能會變更或無法使用。\]

取得 Microsoft Rich Edit 控制項的文字版面配置。

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

取得目前的文字版面配置。 如需可能的文字版面配置值清單，請參閱 [**EM \_ SETPAGEROTATE**](em-setpagerotate.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 Windows XP （含 SP1） \[ 桌面應用程式\]<br/>                                  |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Richedit。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**EM \_ SETPAGEROTATE**](em-setpagerotate.md)
</dt> </dl>

 

 





