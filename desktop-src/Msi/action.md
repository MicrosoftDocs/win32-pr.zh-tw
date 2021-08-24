---
description: ACTION 屬性可以設定為下列值。
ms.assetid: f2c436b6-ebd9-4ac4-8609-f54129023ca7
title: ACTION 屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14b4f17c7bd08b2e366fa23a55ad2b8044ce845ac4df04d0164ba34ad6dff32b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145991"
---
# <a name="action-property"></a>ACTION 屬性

**ACTION** 屬性可以設定為下列值。

## <a name="value"></a>值



| 值                                                                                                                                            | 意義                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="INSTALL"></span><span id="install"></span><dl> <dt>**安裝**</dt> </dl>       | [安裝動作](install-action.md)<br/>     |
| <span id="ADVERTISE"></span><span id="advertise"></span><dl> <dt>**做廣告**</dt> </dl> | [通告動作](advertise-action.md)<br/> |
| <span id="ADMIN"></span><span id="admin"></span><dl> <dt>**管理**</dt> </dl>             | [管理動作](admin-action.md)<br/>         |



 

如果將 Null 動作名稱提供給 [**MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona)或 [**dataadapter.doaction 方法**](session-doaction.md)，則 [**動作**] 屬性會決定要執行的動作。 如果未針對 **ACTION** 屬性定義任何值，則安裝程式會呼叫 [安裝動作](install-action.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | WindowsWindows Server 2012、Windows 8 Windows Server 2008 R2 或 Windows 7 上的安裝程式5.0。 WindowsWindows Server 2008 或 Windows Vista 上的安裝程式4.0 或 Windows Installer 4.5。 WindowsWindows Server 2003 或 Windows XP 上的安裝程式。 如需 Windows Installer 版本所需的最低 Windows service pack 相關資訊，請參閱[Windows Installer Run-Time 需求](windows-installer-portal.md)。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[屬性](properties.md)
</dt> </dl>

 

 




