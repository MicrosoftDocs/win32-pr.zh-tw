---
title: '透過乙太網路連接的點對點通訊協定 (PPP) '
description: Windows伺服器2003、Windows XP 及更新版本的作業系統提供透過乙太網路點對點通訊協定 (PPP) 的支援 (PPPoE) 。 針對 PPPoE 連接，在 RASENTRY 結構中設定下列值。
ms.assetid: abdbf22c-abeb-4363-bfa6-e0002d1637f4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92703bac13d129ed29cee1c22328825de67325239c1906c1728b96d53398647b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117789808"
---
# <a name="point-to-point-protocol-over-ethernet-connections"></a>透過乙太網路連接的點對點通訊協定 (PPP) 

Windows伺服器2003、Windows XP 及更新版本的作業系統提供透過乙太網路點對點通訊協定 (PPP) 的支援 (PPPoE) 。 針對 PPPoE 連接，在 [**RASENTRY**](/previous-versions/windows/desktop/legacy/aa377274(v=vs.85)) 結構中設定下列值。



| 成員                      | 值             |
|-----------------------------|-------------------|
| RASENTRY. dwType             | RASET \_ 寬頻  |
| RAENTRY.szDeviceType        | RASDT \_ PPPoE      |
| RASENTRY.szLocalPhoneNumber | 服務名稱。 |



 

您可以使用 [**RasSetEntryProperties**](/windows/desktop/api/Ras/nf-ras-rassetentrypropertiesa) 函數來設定這些值。

您也可以使用 [**RasEntryDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasentrydlga)和 RASENTRYDLG 的 RASEDFLAG \_ NewBroadbandEntry 旗 [](/windows/desktop/api/Rasdlg/nf-rasdlg-rasentrydlga)標，顯示建立 PPPoE 電話簿專案的 wizard。

 

 