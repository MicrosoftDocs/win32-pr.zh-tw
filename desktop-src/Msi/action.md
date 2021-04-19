---
description: ACTION 屬性可以設定為下列值。
ms.assetid: f2c436b6-ebd9-4ac4-8609-f54129023ca7
title: ACTION 屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 901061f953ffaed030ff6d3a94f440eada25fc59
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984123"
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
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer。 如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[屬性](properties.md)
</dt> </dl>

 

 




