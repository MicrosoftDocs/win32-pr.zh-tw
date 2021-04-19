---
description: 在 Windows 2000 和更新版本的作業系統上，如果安裝程式是在 Windows Server 2003 的 web 版本上執行，安裝程式會將 MsiNTSuiteWebServer 屬性設定為1。
ms.assetid: de462ba2-4654-4f47-9dd7-3bc9c6f0af0e
title: MsiNTSuiteWebServer 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 082e3ae7f107bf3499f5a48473d53ebb530138a6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995277"
---
# <a name="msintsuitewebserver-property"></a>MsiNTSuiteWebServer 屬性

在 Windows 2000 和更新版本的作業系統上，如果安裝程式是在 Windows Server 2003 的 web 版本上執行，安裝程式會將 **MsiNTSuiteWebServer** 屬性設定為1。 只有當 VER \_ SUITE 分頁 \_ 旗標設定于 [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) 結構中時，安裝程式才會將這個屬性設定為1。 否則，安裝程式不會設定這個屬性。

## <a name="remarks"></a>備註

這個屬性僅適用于 Windows Server 2003 版的安裝程式。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer。 如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[屬性](properties.md)
</dt> <dt>

[Windows Installer 2.0 及更早版本不支援](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 
