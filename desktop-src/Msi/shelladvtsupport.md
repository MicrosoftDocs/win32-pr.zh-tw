---
description: 如果系統的 IShellLink 介面支援安裝程式描述項解析，則 ShellAdvtSupport 屬性是由安裝程式設定。
ms.assetid: 8c3503c5-2a9c-43ad-8cc5-ea10df39b24d
title: ShellAdvtSupport 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfacc34bfffdde9ce34841030f38c443a243c9923cb70749a27615cccc1c676e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119628438"
---
# <a name="shelladvtsupport-property"></a>ShellAdvtSupport 屬性

如果系統的 [**IShellLink**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishelllinka)介面支援安裝程式描述項解析，則 **ShellAdvtSupport** 屬性是由安裝程式設定。

## <a name="remarks"></a>備註

如果設定此屬性，則系統的 [**IShellLink**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishelllinka) 介面支援安裝程式描述項解析。 Windows 2000 和執行 Internet Explorer 4.01 的系統都支援此功能。 如果未設定此屬性，安裝程式會在安裝期間建立非公告功能的預設行為，不論是在本機或從來源執行。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | WindowsWindows Server 2012、Windows 8 Windows Server 2008 R2 或 Windows 7 上的安裝程式5.0。 WindowsWindows Server 2008 或 Windows Vista 上的安裝程式4.0 或 Windows Installer 4.5。 WindowsWindows Server 2003 或 Windows XP 上的安裝程式。 如需 Windows Installer 版本所需的最低 Windows service pack 相關資訊，請參閱[Windows Installer Run-Time 需求](windows-installer-portal.md)。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[屬性](properties.md)
</dt> <dt>

[廣告的平臺支援](platform-support-of-advertisement.md)
</dt> </dl>

 

 
