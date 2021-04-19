---
description: 安裝程式會將 MsiRestartManagerSessionKey 屬性的值設定為重新啟動管理員會話的工作階段金鑰。
ms.assetid: efbf11f2-38ab-4509-aa01-23fa8cfdaa60
title: MsiRestartManagerSessionKey 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 489095e0af617c7ae403811f0eab800c5502e3bd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995996"
---
# <a name="msirestartmanagersessionkey-property"></a>MsiRestartManagerSessionKey 屬性

安裝程式會將 **MsiRestartManagerSessionKey** 屬性的值設定為 [重新開機管理員](../rstmgr/restart-manager-portal.md) 會話的工作階段金鑰。 自訂動作可以使用工作階段金鑰加入 [重新開機管理員](../rstmgr/restart-manager-portal.md) 會話。

## <a name="remarks"></a>備註

安裝程式會在初始化時設定 **MsiRestartManagerSessionKey** 屬性的值，然後在 [InstallValidate](installvalidate-action.md) 動作期間清除此值。 需要 **MsiRestartManagerSessionKey** 屬性值的自訂動作必須位於動作順序中的 InstallValidate 動作之前。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 如需 Windows Installer 版本所需的最低 service pack 資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[屬性](properties.md)
</dt> <dt>

[Windows Installer 3.1 及更早版本不支援](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 
