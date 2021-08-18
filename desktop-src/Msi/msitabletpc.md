---
description: 如果目前的作業系統 Windows XP Tablet PC Edition，則安裝程式會將 MsiTabletPC 屬性設定為非零值。
ms.assetid: b178a98e-b6f8-4ff8-b554-e47c3b39f892
title: MsiTabletPC 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac47dd0d8db3c0e882a965685bb1507dc0103f3e965dfbcb8f4857ada19e17ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145606"
---
# <a name="msitabletpc-property"></a>MsiTabletPC 屬性

如果目前的作業系統 Windows XP Tablet PC Edition，則安裝程式會將 **MsiTabletPC** 屬性設定為非零值。 安裝程式會將 [**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) 函式與 **SM \_ 平板** 使用者搭配使用，而屬性則會接收此函式所傳回的非零值。 如果目前的系統不是 Windows XP Tablet PC Edition， **GetSystemMetrics** 函式會傳回零，而且安裝程式不會設定這個屬性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | WindowsWindows Server 2012、Windows 8 Windows Server 2008 R2 或 Windows 7 上的安裝程式5.0。 WindowsWindows Server 2008 或 Windows Vista 上的安裝程式4.0 或 Windows Installer 4.5。 WindowsWindows Server 2003 或 Windows XP 上的安裝程式4.5。 如需 Windows Installer 版本所需的最低 Windows service pack 相關資訊，請參閱[Windows Installer Run-Time 需求](windows-installer-portal.md)。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[屬性](properties.md)
</dt> <dt>

[Windows Installer 3.1 及更早版本不支援](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 
