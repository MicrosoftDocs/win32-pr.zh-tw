---
description: 如果每一電腦的系統原則設定為1，則系統上沒有套件會取得元件資料表中 msidbComponentAttributesShared 屬性所啟用的共用元件功能。
ms.assetid: 28181f8c-8c03-4962-a142-c35d0dd88940
title: DisableSharedComponent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de7576406e14b0f9ac48a26735b984302c2d765b784484022a85ec50244ee8df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118143099"
---
# <a name="disablesharedcomponent"></a>DisableSharedComponent

如果每一電腦的 [系統原則](system-policy.md)設定為1，則系統上沒有套件會取得 [元件資料表](component-table.md)中 **msidbComponentAttributesShared** 屬性所啟用的共用元件功能。 預設值為0，可針對所有封裝中標示為 **msidbComponentAttributesShared** 的元件啟用共用元件功能。

**[Windows Installer 4.0 及更早版本](not-supported-in-windows-installer-4-0.md)：** 不支援。 從 Windows Installer 4.5 開始，可以使用此函數。

## <a name="registry-key"></a>登錄金鑰

**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **原則** \\ **Microsoft** \\ **Windows** \\ **安裝程式**

## <a name="data-type"></a>資料類型

**REG \_ DWORD**

 

 



