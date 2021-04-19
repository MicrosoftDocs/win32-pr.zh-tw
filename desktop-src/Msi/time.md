---
description: Time 屬性是以小時、分鐘和秒為單位的目前時間（以小時、分鐘和秒為單位），格式為 HH： MM： SS （使用24小時制）的常值文字。
ms.assetid: 6f487e46-e178-4d41-b6fa-7c16aa1c46fd
title: Time 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10c3456063842c8dd89fadf5860733b5c5aecbef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984329"
---
# <a name="time-property"></a>Time 屬性

**Time** 屬性是以小時、分鐘和秒為單位的目前時間（以小時、分鐘和秒為單位），格式為 HH： MM： SS （使用24小時制）的常值文字。 例如，時間 6:57 p.m。 以 "18:57:00" 表示。 值的格式取決於使用者的地區設定，而是使用 [**GetTimeFormat**](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata) 函數搭配 time \_ FORCE24HOURFORMAT \| time NOTIMEMARKER 選項取得的格式 \_ 。 這個屬性的值是由 Windows Installer 所設定，而不是封裝作者。

## <a name="remarks"></a>備註

因為這是文字字串，所以不能用在條件運算式中。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer。 如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[屬性](properties.md)
</dt> </dl>

 

 
