---
description: MSIPATCHREMOVE 屬性會指定要在安裝期間移除的修補程式清單。
ms.assetid: 76f8daa9-d32c-4845-85bc-52b728f53d1f
title: MSIPATCHREMOVE 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebf83583c5b15311e175e67a867ff5aca71394b7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976010"
---
# <a name="msipatchremove-property"></a>MSIPATCHREMOVE 屬性

**MSIPATCHREMOVE** 屬性會指定要在安裝期間移除的修補程式清單。 清單中的個別修補程式會以分號分隔，並且可由 patch 程式碼 GUID 或修補程式的完整路徑來表示。 [**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa)函式和 [安裝程式](installer-object.md)物件的 [**RemovePatches**](installer-removepatches.md)方法會設定 **MSIPATCHREMOVE** 屬性。

您可以在命令列上設定 **MSIPATCHREMOVE** 屬性，如下所示來移除修補程式。

**msiexec/i A： \\Example.msi MSIPATCHREMOVE = c： \\ 修補程式 \\ qfe1 .msp; {0BBB87F1-3186-409C-8CDD-C88AA2A4A7E0};{A86B443B-E3BF-4009-ADED-F716FC735858}/qb**

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer 3.0 或更新版本。 如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[屬性](properties.md)
</dt> <dt>

[Windows Installer 2.0 及更早版本不支援](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




