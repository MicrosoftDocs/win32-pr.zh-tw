---
description: 如果目前的作業系統是 Windows XP Tablet PC Edition，安裝程式會將 MsiTabletPC 屬性設定為非零值。
ms.assetid: b178a98e-b6f8-4ff8-b554-e47c3b39f892
title: MsiTabletPC 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0bf2878dbaa895e0924a50900d331db0b879edc1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984798"
---
# <a name="msitabletpc-property"></a>MsiTabletPC 屬性

如果目前的作業系統是 Windows XP Tablet PC Edition，安裝程式會將 **MsiTabletPC** 屬性設定為非零值。 安裝程式會將 [**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) 函式與 **SM \_ 平板** 使用者搭配使用，而屬性則會接收此函式所傳回的非零值。 如果目前的系統不是 Windows XP Tablet PC Edition， **GetSystemMetrics** 函式會傳回零，而且安裝程式不會設定這個屬性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer 4.5。 如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[屬性](properties.md)
</dt> <dt>

[Windows Installer 3.1 及更早版本不支援](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 
