---
description: 在 Windows 2000 和更新版本的作業系統上，如果已安裝 Microsoft Small Business Server，安裝程式會將 MsiNTSuiteSmallBusiness 屬性設定為1。
ms.assetid: 9ac578b9-316f-413c-aae0-4f414109583b
title: MsiNTSuiteSmallBusiness 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1e0dab7d024753a30d6a640cefd1652de137b5cd230a772a5041927dc0e725e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082738"
---
# <a name="msintsuitesmallbusiness-property"></a>MsiNTSuiteSmallBusiness 屬性

在 Windows 2000 和更新版本的作業系統上，如果已安裝 Microsoft Small Business Server，安裝程式會將 **MsiNTSuiteSmallBusiness** 屬性設定為1。 只有在 \_ \_ [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) 結構中設定了 VER SUITE SMALLBUSINESS 旗標時，安裝程式才會將這個屬性設定為1。 否則，安裝程式不會設定這個屬性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | WindowsWindows Server 2012、Windows 8 Windows Server 2008 R2 或 Windows 7 上的安裝程式5.0。 WindowsWindows Server 2008 或 Windows Vista 上的安裝程式4.0 或 Windows Installer 4.5。 WindowsWindows Server 2003 或 Windows XP 上的安裝程式。 如需 Windows Installer 版本所需的最低 Windows service pack 相關資訊，請參閱[Windows Installer Run-Time 需求](windows-installer-portal.md)。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[屬性](properties.md)
</dt> </dl>

 

 
