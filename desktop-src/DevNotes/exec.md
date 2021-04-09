---
description: HKLM \\ Software \\ Microsoft \\ Internet Explorer \\ Extensions \\ {e2e2dd38-d088-4134-82b7-f2ba38496583}。
ms.assetid: a0d9e959-d8fd-4546-9529-1dc42fa0bdd6
title: Exec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2711b2c8882f9af12de2f060810ccd4219faa5ec
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689056"
---
# <a name="exec"></a>Exec

**HKLM \\ Software \\ Microsoft \\ Internet Explorer \\ Extensions \\ {e2e2dd38-d088-4134-82b7-f2ba38496583}**



| 資料類型 | 範圍                    | 預設值 |
|-----------|--------------------------|---------------|
| REG \_ SZ   | *可執行檔的路徑* |               |



 

## <a name="browser-integration-steps"></a>瀏覽器整合步驟

1.  使用 [**RegOpenKeyEx**](/windows/win32/api/winreg/nf-winreg-regopenkeyexa) 函數來判斷是否已安裝網路診斷。 如果已安裝，則會出現 **{e2e2dd38-d088-4134-82b7-f2ba38496583}** 機碼。
2.  您可以使用 [**RegQueryValueEx**](/windows/win32/api/winreg/nf-winreg-regqueryvalueexa) 函式，從 **Exec** 專案取出網路診斷可執行檔的路徑。
3.  如果系統上已安裝診斷，則會顯示新的錯誤頁面。
4.  建立瀏覽器延伸模組，以建立標準工具列專案（如果系統上已安裝診斷）。
5.  使用步驟2中取出的路徑執行網路診斷可執行檔。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[網路診斷工具功能總覽](https://www.microsoft.com/technet/prodtechnol/winxppro/maintain/netdiag.mspx)
</dt> </dl>

 

 
