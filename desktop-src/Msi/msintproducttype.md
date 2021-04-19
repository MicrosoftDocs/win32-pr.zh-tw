---
description: 安裝程式會為 Windows NT、Windows 2000 和更新版本的作業系統設定 MsiNTProductType 屬性。
ms.assetid: 6bbc8283-5911-4fbd-8a0f-09c398280e74
title: MsiNTProductType 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe7fef0791f5842163812b62a7314578d480676c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106980114"
---
# <a name="msintproducttype-property"></a>MsiNTProductType 屬性

安裝程式會為 Windows NT、Windows 2000 和更新版本的作業系統設定 **MsiNTProductType** 屬性。 這個屬性工作表示 Windows 產品類型。

若為 Windows 2000 和更新版本的作業系統，安裝程式會設定下列值。 請注意，值與 [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa)結構的 **wProductType** 欄位相同。



| 值 | 意義                                  |
|-------|------------------------------------------|
| 1     | Windows 2000 Professional 和更新版本      |
| 2     | Windows 2000 網域控制站和更新版本 |
| 3     | Windows 2000 伺服器和更新版本            |



 

若為 Windows 2000 之前的作業系統，安裝程式會設定下列值。



| 值 | 意義                      |
|-------|------------------------------|
| 1     | Windows NT 工作站       |
| 2     | Windows NT 網域控制站 |
| 3     | Windows NT Server            |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer。 如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[屬性](properties.md)
</dt> </dl>

 

 
