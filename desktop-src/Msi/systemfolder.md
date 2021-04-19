---
description: 安裝程式會將 SystemFolder 屬性設定為系統資料夾的完整路徑。
ms.assetid: 23883638-8d3d-4c2a-8ebf-0c306cf01e05
title: SystemFolder 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2abce6e4aa91289ef17134ab3cb878a665d3097c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106985778"
---
# <a name="systemfolder-property"></a>SystemFolder 屬性

安裝程式會將 **SystemFolder** 屬性設定為系統資料夾的完整路徑。

## <a name="remarks"></a>備註

安裝程式會設定這個屬性。 例如，在32位 Windows 上，值可能是 C： \\ Windows \\ System32。 在64位的 Windows 上，此值可能是 C： \\ Windows \\ SysWow64。

此資料夾通常是 Windows 資料夾的子目錄。 不過，它會在設定共用視窗時位於伺服器上。

這是本機資料夾，即使是針對共用視窗進行設定亦同。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer。 如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[屬性](properties.md)
</dt> </dl>

 

 




