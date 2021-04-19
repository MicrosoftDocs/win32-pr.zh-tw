---
description: 停用 rollback 時，安裝程式會設定 RollbackDisabled 屬性。
ms.assetid: 72215b0f-2fc4-49aa-abf8-3206bdfc765f
title: RollbackDisabled 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f50c8e344ed4291210afb1714ce97d90b590999
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982565"
---
# <a name="rollbackdisabled-property"></a>RollbackDisabled 屬性

停用 rollback 時，安裝程式會設定 **RollbackDisabled** 屬性。 **RollbackDisabled** 可供需要確認安裝程式未停用復原的封裝作者使用。 **RollbackDisabled** 屬性可以在條件運算式中使用，以在設定 **RollbackDisabled** 屬性時有效拒絕繼續安裝。

## <a name="default-value"></a>預設值

預設會啟用復原。

## <a name="remarks"></a>備註

由於 [rollback](rollback-custom-actions.md) 和 [commit](commit-custom-actions.md) 在停用回復時不會執行，因此安裝程式無法在安裝期間正確地安裝在交易中使用這些自訂動作類型的封裝。 在此情況下，套件的作者應包含使用 DisableRollback 的條件，以防止在停用復原時繼續安裝。

系統管理員可以設定 DisableRollback 原則值，作為指派系統策略的一部分。 除非必要，否則建議系統管理員不要停用復原。 如需 DisableRollback 原則值的詳細資訊，請參閱 [系統原則](system-policy.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer。 如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[屬性](properties.md)
</dt> <dt>

[復原安裝](rollback-installation.md)
</dt> <dt>

[系統原則](system-policy.md)
</dt> <dt>

[復原自訂動作](rollback-custom-actions.md)
</dt> <dt>

[認可自訂動作](commit-custom-actions.md)
</dt> </dl>

 

 




