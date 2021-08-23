---
description: MSIRMSHUTDOWN 屬性會決定如何關閉目前使用受更新影響之檔案的應用程式或服務，以啟用更新的安裝。
ms.assetid: 6763a490-8d1a-42d2-a8cb-0743b7ba6866
title: MSIRMSHUTDOWN 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac31a924727217ac86937f4f7ac553717138461e0668a7e79916ffab796f8bd7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012876"
---
# <a name="msirmshutdown-property"></a>MSIRMSHUTDOWN 屬性

**MSIRMSHUTDOWN** 屬性會決定如何關閉目前使用受更新影響之檔案的應用程式或服務，以啟用更新的安裝。

## <a name="value"></a>值



| 值                                                                        | 意義                                                                                                                                                                                                                                                                 |
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | 目前使用受更新影響之檔案的處理常式或服務會關閉。<br/>                                                                                                                                                                   |
| <dl> <dt>1</dt> </dl> | 如果處理常式或服務目前使用受更新影響的檔案，而且沒有回應 [重新開機管理員](../rstmgr/restart-manager-portal.md)，則會強制關閉。<br/>                                                                                       |
| <dl> <dt>2</dt> </dl> | 目前使用受更新影響之檔案的處理常式或服務，只有在已註冊重新開機時才會關閉。 如果有任何進程或服務尚未註冊進行重新開機，則不會關閉任何進程或服務。<br/> |



 

## <a name="remarks"></a>備註

如果 [重新開機管理員](../rstmgr/restart-manager-portal.md)無法使用或停用，則會忽略 **MSIRMSHUTDOWN** 屬性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | WindowsWindows Server 2012、Windows 8 Windows Server 2008 R2 或 Windows 7 上的安裝程式5.0。 WindowsWindows Server 2008 或 Windows Vista 上的安裝程式4.0 或 Windows Installer 4.5。 如需 Windows Installer 版本所需的最低 service pack 資訊，請參閱[Windows Installer Run-Time 需求](windows-installer-portal.md)。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[屬性](properties.md)
</dt> <dt>

[Windows Installer 3.1 及更早版本不支援](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 
