---
description: 如果以應用程式傳送的安裝套件不是客戶所收到 CD-ROM 的根目錄，則必須在命令列上將 MEDIAPACKAGEPATH 屬性設定為 CD-ROM 上應用程式的相對路徑。例如，如果媒體上封裝的路徑是 E： \\ MyPath \\My.msi，則使用 MEDIAPACKAGEPATH =&\# 0034; \\MyPath \\ & \# 0034;。系統管理員可以從系統管理安裝點建立 CD-ROMs。 如果在新的 CD-ROM 上變更安裝根目錄的位置，則必須將 MEDIAPACKAGEPATH 屬性設為要從此媒體安裝的新路徑。 CD-ROM 上的位置與套件中指定的來源不同，無法使用。 不過，在從運送媒體建立系統管理安裝點時，並不需要使用此屬性。
ms.assetid: 18b3b19d-28e9-4311-9cc9-3e4224b4ddfe
title: MEDIAPACKAGEPATH 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 140afc253e27b3c861f941e88b55f84ad49f43984fcc3a5aaf82d06fe414e6a3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119926878"
---
# <a name="mediapackagepath-property"></a>MEDIAPACKAGEPATH 屬性

如果以應用程式傳送的安裝套件不是客戶所收到 CD-ROM 的根目錄，則必須在命令列上將 **MEDIAPACKAGEPATH** 屬性設定為 cd-rom 上應用程式的相對路徑。

例如，如果媒體上封裝的路徑是 E： \\ MyPath \\My.msi，則使用 MEDIAPACKAGEPATH = " \\ MyPath \\ "。

系統管理員可以從系統管理安裝點建立 CD-ROMs。 如果在新的 CD-ROM 上變更安裝根目錄的位置，則必須將 **MEDIAPACKAGEPATH** 屬性設為要從此媒體安裝的新路徑。 CD-ROM 上的位置與套件中指定的來源不同，無法使用。 不過，在從運送媒體建立系統管理安裝點時，並不需要使用此屬性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | WindowsWindows Server 2012、Windows 8 Windows Server 2008 R2 或 Windows 7 上的安裝程式5.0。 WindowsWindows Server 2008 或 Windows Vista 上的安裝程式4.0 或 Windows Installer 4.5。 WindowsWindows Server 2003 或 Windows XP 上的安裝程式。 如需 Windows Installer 版本所需的最低 Windows service pack 相關資訊，請參閱[Windows Installer Run-Time 需求](windows-installer-portal.md)。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[屬性](properties.md)
</dt> </dl>

 

 




