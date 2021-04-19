---
description: 如果任何以安裝目標為目標的磁片區都沒有足夠的磁碟空間可容納安裝，安裝程式會將 OutOfNoRbDiskSpace 屬性設定為 True。
ms.assetid: 910d6c1d-38d3-4680-b256-2bf30689ce11
title: OutOfNoRbDiskSpace 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8fa9cdd7c1d444e141103ca148344dd26ea1d2a5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990708"
---
# <a name="outofnorbdiskspace-property"></a>OutOfNoRbDiskSpace 屬性

如果任何以安裝目標為目標的磁片區都沒有足夠的磁碟空間可容納安裝，安裝程式會將 **OutOfNoRbDiskSpace** 屬性設定為 True。 在此情況下，即使已停用 rollback， **OutOfNoRbDiskSpace** 屬性也會設定為 True。 如果所有磁片區有足夠的空間，此值會是 False。

當 [**OutOfDiskSpace**](outofdiskspace.md) 屬性為 True，而且 **OutOfNoRbDiskSpace** 屬性為 False 時，安裝封裝的開發人員可以處理這種情況，方法是撰寫使用者介面，讓使用者可以選擇停用復原並繼續安裝。 如需有條件地顯示對話方塊的詳細資訊，請參閱 [ControlEvent 總覽](controlevent-overview.md)。 如需停用回復的詳細資訊，請參閱 [EnableRollback ControlEvent](enablerollback-controlevent.md)。

**OutOfNoRbDiskSpace** 屬性在 [CostFinalize 動作](costfinalize-action.md)執行之後的任何時間都有效。 **OutOfNoRbDiskSpace** 屬性狀態會在重新計算總安裝成本時動態更新 (例如，任何功能的安裝狀態透過 [選取對話方塊](selection-dialog.md)) 變更時。 選取解決動作會使用這個值來取消安裝並產生對話方塊。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer。 如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[屬性](properties.md)
</dt> <dt>

[ControlEvent 總覽](controlevent-overview.md)
</dt> <dt>

[**OutOfDiskSpace 屬性**](outofdiskspace.md)
</dt> <dt>

[EnableRollback ControlEvent](enablerollback-controlevent.md)
</dt> <dt>

[CostFinalize 動作](costfinalize-action.md)
</dt> <dt>

[選取對話方塊](selection-dialog.md)
</dt> </dl>

 

 




