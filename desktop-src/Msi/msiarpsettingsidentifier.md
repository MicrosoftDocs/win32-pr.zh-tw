---
description: MSIARPSETTINGSIDENTIFIER 屬性包含以分號分隔的登錄位置清單，應用程式會在其中儲存使用者的設定和喜好設定。
ms.assetid: 524ba004-d3a2-4619-8c98-362761a3ae7a
title: MSIARPSETTINGSIDENTIFIER 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a32c979237e6443bec5451f36e36ef49ae4a1f59
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999455"
---
# <a name="msiarpsettingsidentifier-property"></a>MSIARPSETTINGSIDENTIFIER 屬性

**MSIARPSETTINGSIDENTIFIER** 屬性包含以分號分隔的登錄位置清單，應用程式會在其中儲存使用者的設定和喜好設定。 在作業系統升級期間，安裝程式可以使用這項資訊來改善正在遷移應用程式之使用者的體驗。

**MSIARPSETTINGSIDENTIFIER** 屬性的值為常值文字，其中包含應用程式儲存其設定的登錄位置清單。 值可以指定多個可能的登錄位置。 使用分號分隔多個登錄位置。 應用程式設定通常會以下列格式儲存在 **HKCU** 或 **HKLM** 登錄 hive 中： *公司 \\ 應用程式 \\ 版本*。 下列範例是 **MSIARPSETTINGSIDENTIFIER** 屬性的可能值。

*MyCompany \\ AppSuite \\ 1.0;MyCompany \\ App1 \\ 1.0;MyCompany \\ App2 \\ 1。0*

這個屬性是選擇性的，可以在 [屬性](property-table.md) 表中設定。 如果這個屬性出現在屬性工作表中，則此值不得設定為 **Null**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer 4.5。 如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[屬性](properties.md)
</dt> <dt>

[Windows Installer 3.1 及更早版本不支援](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




