---
description: 如果系統的 IShellLink 介面支援安裝程式描述項解析，則 ShellAdvtSupport 屬性是由安裝程式設定。
ms.assetid: 8c3503c5-2a9c-43ad-8cc5-ea10df39b24d
title: ShellAdvtSupport 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df0040aef3b53352a9da8a31bf97f14e8df3791e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977391"
---
# <a name="shelladvtsupport-property"></a>ShellAdvtSupport 屬性

如果系統的 [**IShellLink**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishelllinka)介面支援安裝程式描述項解析，則 **ShellAdvtSupport** 屬性是由安裝程式設定。

## <a name="remarks"></a>備註

如果設定此屬性，則系統的 [**IShellLink**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishelllinka) 介面支援安裝程式描述項解析。 Windows 2000 和執行 Internet Explorer 4.01 的系統都支援此功能。 如果未設定此屬性，安裝程式會在安裝期間建立非公告功能的預設行為，不論是在本機或從來源執行。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer。 如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[屬性](properties.md)
</dt> <dt>

[廣告的平臺支援](platform-support-of-advertisement.md)
</dt> </dl>

 

 
