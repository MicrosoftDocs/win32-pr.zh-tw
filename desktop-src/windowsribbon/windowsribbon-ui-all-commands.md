---
title: 'UI_ALL_COMMANDS (Uiribbon) '
description: 指定常數，識別標記資源檔中所宣告的命令集合。
ms.assetid: b0046d8c-bb54-4231-90f0-c0b2c8790b1a
topic_type:
- apiref
api_name:
- UI_ALL_COMMANDS
api_location:
- Uiribbon.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24767f2d3839b94ee83c6a9a527b2e80dcf8c1960e877f65a0e7e96fff4e3ec4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118705957"
---
# <a name="ui_all_commands"></a>UI \_ 所有 \_ 命令

指定常數，識別標記資源檔中所宣告的命令集合。

## <a name="remarks"></a>備註

**UI \_當 \_** 需要在所有命令中存取類似的屬性時，所有命令都很有用。 例如，您可以透過查詢主機應用程式的新屬性值，將 **\_ 所有 \_ 命令** 都傳遞給 [**IUIFramework：： InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) ，以使所有功能區命令失效並重新整理。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 7、Windows vista （含 SP2）和僅適用于 Windows Vista \[ 桌面應用程式的平臺更新\]<br/>                          |
| 最低支援的伺服器<br/> | Windowsserver 2008 R2、Windows server 2008 SP2 和平臺更新，適用于 Windows Server 2008 \[ desktop 應用程式\]<br/> |
| 標頭<br/>                   | <dl> <dt>Uiribbon。h</dt> </dl>                                             |
| IDL<br/>                      | <dl> <dt>Uiribbon .idl</dt> </dl>                                           |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[常數和列舉](windowsribbon-reference-enumerations.md)
</dt> </dl>

 

