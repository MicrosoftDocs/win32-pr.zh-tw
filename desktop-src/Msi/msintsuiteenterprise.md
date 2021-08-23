---
description: 在 Windows 2000 和更新版本的作業系統上，如果已安裝 Windows 2000 Advanced Server，安裝程式會將 MsiNTSuiteEnterprise 屬性設定為1。
ms.assetid: f5384467-3791-4b0b-a70e-b5343c70db46
title: MsiNTSuiteEnterprise 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 242bf1c95db7d4101362a7b72b4cfa99009a93cc2fa399d1b4b81d93aabbd16c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118944651"
---
# <a name="msintsuiteenterprise-property"></a>MsiNTSuiteEnterprise 屬性

在 Windows 2000 和更新版本的作業系統上，如果已安裝 Windows 2000 Advanced Server，安裝程式會將 **MsiNTSuiteEnterprise** 屬性設定為1。 只有當 VER \_ SUITE \_ ENTERPRISE 旗標設定于 [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) 結構中時，安裝程式才會將這個屬性設定為1。 否則，安裝程式不會設定這個屬性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | WindowsWindows Server 2012、Windows 8 Windows Server 2008 R2 或 Windows 7 上的安裝程式5.0。 WindowsWindows Server 2008 或 Windows Vista 上的安裝程式4.0 或 Windows Installer 4.5。 WindowsWindows Server 2003 或 Windows XP 上的安裝程式。 如需 Windows Installer 版本所需的最低 Windows service pack 相關資訊，請參閱[Windows Installer Run-Time 需求](windows-installer-portal.md)。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[屬性](properties.md)
</dt> </dl>

 

 
