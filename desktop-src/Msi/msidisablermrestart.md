---
description: MSIDISABLERMRESTART 屬性會決定目前使用受更新影響之檔案的應用程式或服務如何關閉並重新啟動，以啟用更新的安裝。
ms.assetid: 45c804bf-6d15-416a-b106-d8bb3f4c547d
title: MSIDISABLERMRESTART 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1215822b26bb9bd48fa52ee46806bc288a2986b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998868"
---
# <a name="msidisablermrestart-property"></a>MSIDISABLERMRESTART 屬性

**MSIDISABLERMRESTART** 屬性會決定目前使用受更新影響之檔案的應用程式或服務如何關閉並重新啟動，以啟用更新的安裝。

## <a name="value"></a>值



| 值                                                                        | 意義                                                                                                                                                                                      |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | 已關閉以安裝更新的所有系統服務都會重新開機。 使用 [重新開機管理員](../rstmgr/restart-manager-portal.md) 註冊本身的所有應用程式都會重新開機。<br/> |
| <dl> <dt>1</dt> </dl> | 在安裝更新之後，使用 [重新開機管理員](../rstmgr/restart-manager-portal.md) 關閉的進程不會在套用更新之後重新開機。<br/>                           |



 

## <a name="remarks"></a>備註

如果 [重新開機管理員](../rstmgr/restart-manager-portal.md)無法使用或停用，則會忽略 **MSIDISABLERMRESTART** 屬性。

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

 

 
