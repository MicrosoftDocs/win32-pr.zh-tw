---
description: 在 Windows 2000 和更新版本的作業系統上，如果 Microsoft Small Business Server 是以強制的嚴格用戶端授權安裝，則安裝程式會將 MsiNTSuiteSmallBusinessRestricted 屬性設定為1。
ms.assetid: a7100df4-6fe4-4159-ba94-9b5bd1803107
title: MsiNTSuiteSmallBusinessRestricted 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71d85fa7fe83c0c8c7cd40788453d1078e7a6b94
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977490"
---
# <a name="msintsuitesmallbusinessrestricted-property"></a>MsiNTSuiteSmallBusinessRestricted 屬性

在 Windows 2000 和更新版本的作業系統上，如果 Microsoft Small Business Server 是以強制的嚴格用戶端授權安裝，則安裝程式會將 **MsiNTSuiteSmallBusinessRestricted** 屬性設定為1。 只有在 \_ \_ \_ [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) 結構中設定了 VER SUITE SMALLBUSINESS 限制旗標時，安裝程式才會將這個屬性設定為1。 否則，安裝程式不會設定這個屬性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer。 如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[屬性](properties.md)
</dt> </dl>

 

 
