---
description: MSIRESTARTMANAGERCONTROL 屬性會指定 Windows Installer 封裝是使用 [重新開機管理員] 或 [FilesInUse] 對話方塊功能。
ms.assetid: fefff18b-892a-440e-9f57-d23aeb99af74
title: MSIRESTARTMANAGERCONTROL 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8d965f1b814ce2969a6253ba227672c54769791
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976189"
---
# <a name="msirestartmanagercontrol-property"></a>MSIRESTARTMANAGERCONTROL 屬性

**MSIRESTARTMANAGERCONTROL** 屬性會指定 Windows Installer 封裝是使用 [[重新開機管理員](../rstmgr/restart-manager-portal.md)] 或 [ [FilesInUse] 對話方塊](filesinuse-dialog.md)功能。

## <a name="value"></a>值



| 值                                                                                        | 意義                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl>                 | 如果未設定屬性，則這是預設值。 Windows Installer 一律會嘗試在 Windows Vista 上使用 [重新開機管理員](../rstmgr/restart-manager-portal.md) 。<br/>                                                                                                                                                                                                       |
| <dl> <dt>停用</dt> </dl>         | 停用 [重新開機管理員](../rstmgr/restart-manager-portal.md)與封裝的互動。 Windows Installer 使用 [ [FilesInUse] 對話方塊](filesinuse-dialog.md)。 <br/>                                                                                                                                                                                                      |
| <dl> <dt>"DisableShutdown"</dt> </dl> | Windows Installer 使用 [ [FilesInUse] 對話方塊](filesinuse-dialog.md)。 這項設定會在安裝未撰寫為使用重新開機管理員的 Windows Installer 套件時，停用 [重新開機管理員](../rstmgr/restart-manager-portal.md) 可減輕重新開機的嘗試。 安裝程式仍會使用重新開機管理員來偵測應用程式所使用的檔案。 <br/> |



 

## <a name="remarks"></a>備註

如果 [重新開機管理員](../rstmgr/restart-manager-portal.md)無法使用或停用，則會忽略 **MSIRESTARTMANAGERCONTROL** 屬性。

您可以使用自訂轉換或升級來修改此屬性的值。 從自訂動作變更這個屬性的值沒有任何作用。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 如需 Windows Installer 版本所需的最低 service pack 資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[屬性](properties.md)
</dt> <dt>

[DisableAutomaticApplicationShutdown](disableautomaticapplicationshutdown.md)
</dt> <dt>

[Windows Installer 3.1 及更早版本不支援](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 
