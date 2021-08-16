---
description: MSIPATCHREMOVE 屬性會指定要在安裝期間移除的修補程式清單。
ms.assetid: 76f8daa9-d32c-4845-85bc-52b728f53d1f
title: MSIPATCHREMOVE 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1259e42bebdbf44473fb92c666cdb764580c2f54321e7f14d0293b1fa9928103
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118944506"
---
# <a name="msipatchremove-property"></a>MSIPATCHREMOVE 屬性

**MSIPATCHREMOVE** 屬性會指定要在安裝期間移除的修補程式清單。 清單中的個別修補程式會以分號分隔，並且可由 patch 程式碼 GUID 或修補程式的完整路徑來表示。 [**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa)函式和 [安裝程式](installer-object.md)物件的 [**RemovePatches**](installer-removepatches.md)方法會設定 **MSIPATCHREMOVE** 屬性。

您可以在命令列上設定 **MSIPATCHREMOVE** 屬性，如下所示來移除修補程式。

**msiexec/i A： \\Example.msi MSIPATCHREMOVE = c： \\ 修補程式 \\ qfe1 .msp; {0BBB87F1-3186-409C-8CDD-C88AA2A4A7E0};{A86B443B-E3BF-4009-ADED-F716FC735858}/qb**

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | WindowsWindows Server 2012、Windows 8 Windows Server 2008 R2 或 Windows 7 上的安裝程式5.0。 WindowsWindows Server 2008 或 Windows Vista 上的安裝程式4.0 或 Windows Installer 4.5。 WindowsWindows Server 2003 或 Windows XP 上的安裝程式3.0 或更新版本。 如需 Windows Installer 版本所需的最低 Windows service pack 相關資訊，請參閱[Windows Installer Run-Time 需求](windows-installer-portal.md)。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[屬性](properties.md)
</dt> <dt>

[Windows Installer 2.0 及更早版本不支援](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




