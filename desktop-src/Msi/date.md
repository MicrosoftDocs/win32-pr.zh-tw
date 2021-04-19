---
description: Date 屬性是目前的 month、day 和 year 做為常值文字的字串，格式為 MM/DD/YYYY。
ms.assetid: 22c1f9b4-f6c9-4d57-8457-53bb045e2a4d
title: Date 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf1e4e5cfc7d9236228b9e8b419bbbca48052769
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990705"
---
# <a name="date-property"></a>Date 屬性

**Date** 屬性是目前的 month、day 和 year 做為常值文字的字串，格式為 MM/DD/YYYY。 例如，2005年6月22日的日期可以表示為 "06/22/2005"。 值的格式取決於使用者的地區設定，而是使用 [**GetDateFormat**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformata) 與 DATE >shortdate 選項取得的格式 \_ 。 這個屬性的值是由 Windows Installer 所設定，而不是封裝作者。

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

 

