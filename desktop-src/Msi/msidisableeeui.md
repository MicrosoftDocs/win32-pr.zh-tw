---
description: 若要停用 MsiEmbeddedUI 資料表中定義之安裝的內嵌使用者介面，請在命令列上將 MSIDISABLEEEUI 屬性設定為1。
ms.assetid: c5ada690-c5dd-455f-babe-8c09750525c4
title: MSIDISABLEEEUI 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb1e599ed0786c7d2c55644eb5759db3917757d3b41f6107161d72a3cc559484
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039948"
---
# <a name="msidisableeeui-property"></a>MSIDISABLEEEUI 屬性

若要停用 [MsiEmbeddedUI 資料表](msiembeddedui-table.md)中定義之安裝的內嵌使用者介面，請在命令列上將 MSIDISABLEEEUI 屬性設定為1。

**[Windows Installer 4.0 及更早版本](not-supported-in-windows-installer-4-0.md)：** 不支援。 早于 Windows Installer 4.5 的版本會忽略 MSIDISABLEEEUI 屬性。

## <a name="remarks"></a>備註

在多套件安裝中，子封裝通常應該使用父封裝的使用者介面，而不會初始化它自己的內嵌 UI。 如果未在父封裝內設定 MSIDISABLEEEUI 屬性，則子封裝預設會使用父封裝的內嵌 UI，並忽略子封裝內的 MSIDISABLEEEUI 屬性。

MSIDISABLEEEUI 屬性會停用單一封裝的內嵌使用者介面。 您可以使用 [MsiDisableEmbeddedUI](msidisableembeddedui.md) 原則來停用電腦上所有封裝的內嵌使用者介面。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | WindowsWindows Server 2012、Windows 8 Windows Server 2008 R2 或 Windows 7 上的安裝程式5.0。 WindowsWindows Server 2008、Windows Vista、Windows Server 2003 和 Windows XP 上的安裝程式4.5。 如需 Windows Installer 版本所需的最低 Windows service pack 相關資訊，請參閱[Windows Installer Run-Time 需求](windows-installer-portal.md)。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[屬性](properties.md)
</dt> </dl>

 

 




