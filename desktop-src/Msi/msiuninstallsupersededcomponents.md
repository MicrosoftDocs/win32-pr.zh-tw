---
description: 在屬性資料表或命令列中，將 MSIUNINSTALLSUPERSEDEDCOMPONENTS 屬性設定為1。
ms.assetid: ba9b1b2d-1667-48c8-8f1a-9958a1d170da
title: MSIUNINSTALLSUPERSEDEDCOMPONENTS 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcc930a258d8faebe71480f466f2b097fe1eda68
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106979508"
---
# <a name="msiuninstallsupersededcomponents-property"></a>MSIUNINSTALLSUPERSEDEDCOMPONENTS 屬性

在 [屬性資料表](property-table.md)或命令列中，將 **MSIUNINSTALLSUPERSEDEDCOMPONENTS** 屬性設定為1。 當這個屬性設定為1時，安裝程式會判斷是否有任何已取代修補程式中的元件變成多餘的。 安裝程式可以取消註冊並卸載多餘的元件，以防止在電腦上留下孤立的元件。

設定此屬性會影響所有修補程式中所取代的元件。 若要為單一元件啟用這項功能，請使用 [元件資料表](component-table.md)中的 **msidbComponentAttributesUninstallOnSupersedence** 屬性。

**[Windows Installer 4.0 及更早版本](not-supported-in-windows-installer-4-0.md)：** 不支援。 早于 Windows Installer 4.5 的版本會忽略 **MSIUNINSTALLSUPERSEDEDCOMPONENTS** 屬性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Vista、Windows XP、Windows Server 2003 和 Windows Server 2008 上的 Windows Installer 4.5 或 Windows Installer 4.5。 如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[屬性](properties.md)
</dt> </dl>

 

 




