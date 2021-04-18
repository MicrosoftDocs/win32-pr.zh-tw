---
description: 設定 MSINODISABLEMEDIA 屬性，以防止安裝程式設定 DISABLEMEDIA 屬性。 設定 DISABLEMEDIA 屬性可防止安裝程式將任何媒體來源（例如 CD-ROM）註冊為產品的有效來源。
ms.assetid: 4e1450aa-bf89-4d44-b463-4016660f5508
title: MSINODISABLEMEDIA 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93510263cbe182c66305dcc08c10d908709e1259
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976153"
---
# <a name="msinodisablemedia-property"></a>MSINODISABLEMEDIA 屬性

設定 **MSINODISABLEMEDIA** 屬性，以防止安裝程式設定 [**DISABLEMEDIA**](-disablemedia.md) 屬性。 設定 **DISABLEMEDIA** 屬性可防止安裝程式將任何媒體來源（例如 cd-rom）註冊為產品的有效來源。

如果未設定 **MSINODISABLEMEDIA** ，安裝程式可能會在執行 [系統管理安裝](administrative-installation.md)時，將 [**DISABLEMEDIA**](-disablemedia.md)新增至系統管理屬性資料流程。 這可防止從系統管理映射安裝的使用者從媒體安裝，例如 CD-ROM。

-   執行系統管理安裝時，如果 [[**頁面計數摘要**](page-count-summary.md)] 屬性小於150，則安裝程式只會將 [**DISABLEMEDIA**](-disablemedia.md)新增至系統管理屬性串流。

如果 [**DISABLEMEDIA**](-disablemedia.md) 列在 [**AdminProperties**](adminproperties.md) 屬性中，則設定 **MSINODISABLEMEDIA** 會防止在系統管理安裝期間設定 **DISABLEMEDIA** 。 在此情況下，安裝程式可能會註冊媒體來源，如果原始系統管理安裝映射稍後無法使用，則使用者可以選擇從媒體來源重新安裝。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003、Windows XP 及 Windows 2000 上的 Windows Installer。 如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[屬性](properties.md)
</dt> </dl>

 

 




