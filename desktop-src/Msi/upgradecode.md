---
description: UpgradeCode 屬性是 GUID，代表一組相關的產品。 UpgradeCode 可用於升級資料表中，以搜尋已安裝之產品的相關版本。RegisterProduct 動作會使用這個屬性。
ms.assetid: 6cdee5d8-8aa0-4fad-9338-152ee33b8077
title: UpgradeCode 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac1e5493ad651e609f6ef9d7ae14e07c0c15b5b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977718"
---
# <a name="upgradecode-property"></a>UpgradeCode 屬性

**UpgradeCode** 屬性是 GUID，代表一組相關的產品。 **UpgradeCode** 可用於 [升級資料表](upgrade-table.md)中，以搜尋已安裝之產品的相關版本。

[RegisterProduct 動作](registerproduct-action.md)會使用這個屬性。

## <a name="remarks"></a>備註

強烈建議安裝套件的作者為其應用程式指定 **UpgradeCode** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer。 如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[屬性](properties.md)
</dt> <dt>

[修補和升級](patching-and-upgrades.md)
</dt> <dt>

[準備應用程式以進行未來的主要升級](preparing-an-application-for-future-major-upgrades.md)
</dt> </dl>

 

 




