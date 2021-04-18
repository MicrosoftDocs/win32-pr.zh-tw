---
description: Intel 屬性是在 Intel 處理器上執行時，由 Windows Installer 設定為數值處理器等級。
ms.assetid: c1190df2-0440-4dd1-bce5-61d899f71437
title: Intel 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab73f35b371d3bf8323fe2a3f3de1608666bc181
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976137"
---
# <a name="intel-property"></a>Intel 屬性

**Intel** 屬性是在 intel 處理器上執行時，由 Windows Installer 設定為數值處理器等級。 這些值與 [**系統 \_ 資訊**](/windows/win32/api/sysinfoapi/ns-sysinfoapi-system_info)結構的 [ *wProcessorLevel* ] 欄位相同。 在 x64 處理器上執行時，Windows Installer 會設定 **Intel** 屬性，以反映由作業系統所報告的 x64 電腦所模擬的 x86 處理器。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer。 如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[屬性](properties.md)
</dt> </dl>

 

 
