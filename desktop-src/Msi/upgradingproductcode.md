---
description: 當升級移除應用程式時，Windows Installer 會設定 UPGRADINGPRODUCTCODE 屬性。
ms.assetid: 903e4c22-e7ae-47bd-989b-d8c922de8d1a
title: UPGRADINGPRODUCTCODE 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7a256ade7f03275752ad4d176e64cd9d0fa12ae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984064"
---
# <a name="upgradingproductcode-property"></a>UPGRADINGPRODUCTCODE 屬性

當升級移除應用程式時，Windows Installer 會設定 **UPGRADINGPRODUCTCODE** 屬性。 當安裝程式執行 [RemoveExistingProducts 動作](removeexistingproducts-action.md)時，會設定此屬性。 使用主控台中的 [新增或移除程式] 移除應用程式，就不會設定這個屬性。 應用程式會藉由檢查 **UPGRADINGPRODUCTCODE**，來判斷升級或新增或移除程式是否正在移除。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer。 如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[屬性](properties.md)
</dt> </dl>

 

 




