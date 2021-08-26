---
description: 如果目前安裝的目標磁片區沒有足夠的磁碟空間可容納安裝，安裝程式會將 OutOfDiskSpace 屬性設定為 TRUE。
ms.assetid: fb1e3be7-12dd-4036-b657-b91b480fca4a
title: OutOfDiskSpace 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a99146d08722038bbc2d9b1e0d7b32fd8b587126b0fc942e14823909a2aef79
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120042578"
---
# <a name="outofdiskspace-property"></a>OutOfDiskSpace 屬性

如果目前安裝的目標磁片區沒有足夠的磁碟空間可容納安裝，安裝程式會將 **OutOfDiskSpace** 屬性設定為 TRUE。 如果所有磁片區有足夠的空間，此值會是 FALSE。 選取解決動作會使用這個值來取消安裝並產生對話方塊。

此屬性在 [CostFinalize 動作](costfinalize-action.md) 執行之後隨時都有效。 [**OutOfNoRbDiskSpace**](outofnorbdiskspace.md)屬性狀態會在重新計算總安裝成本時動態更新 (例如，任何功能的安裝狀態透過 [選取](selection-dialog.md)對話方塊) 變更時。

## <a name="remarks"></a>備註

任何依賴 **OutOfDiskSpace** 屬性來判斷是否要顯示對話方塊的對話方塊都必須設定對話方塊的 [TrackDiskSpace 對話方塊樣式位](trackdiskspace-dialog-style-bit.md) ，以動態更新目標磁片區上的空間。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | WindowsWindows Server 2012、Windows 8 Windows Server 2008 R2 或 Windows 7 上的安裝程式5.0。 WindowsWindows Server 2008 或 Windows Vista 上的安裝程式4.0 或 Windows Installer 4.5。 WindowsWindows Server 2003 或 Windows XP 上的安裝程式。 如需 Windows Installer 版本所需的最低 Windows service pack 相關資訊，請參閱[Windows Installer Run-Time 需求](windows-installer-portal.md)。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[屬性](properties.md)
</dt> </dl>

 

 




