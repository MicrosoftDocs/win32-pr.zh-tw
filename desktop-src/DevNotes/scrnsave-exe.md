---
description: HKCU \\ 主控台 \\ Desktop。
ms.assetid: e18ea3c8-ddac-4214-83be-106c28c3c327
title: SCRNSAVE.EXE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e1ac7c0f2ee9d87911c0db195df89e2c27dcf1b19c0e9dac70d1517b0ad30ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119571348"
---
# <a name="scrnsaveexe"></a>SCRNSAVE.EXE

**HKCU \\ 主控台 \\ Desktop**



| 資料類型 | 範圍       | 預設值 |
|-----------|-------------|---------------|
| REG \_ SZ   | *檔案名稱* | (無)        |



 

## <a name="description"></a>描述

指定螢幕保護裝置可執行檔的名稱。

## <a name="change-method"></a>變更方法

若要變更這個專案的值，請在主控台按兩下 [ **顯示**] 中，按一下 [ **螢幕保護裝置** ] 索引標籤，然後從 [ **螢幕保護裝置** ] 清單中選取螢幕保護裝置。

您也可以使用應用程式開發介面來變更此專案， (API) 函式 **InstallScreenSaver**（由 Desk.cpl 匯出）。 您可以使用命令列 **rundll32.exe desk.cpl InstallScreenSaver** 檔來存取此函式，其中 *file* 是螢幕保護裝置可 *執行檔的* 名稱。

## <a name="activation-method"></a>啟用方法

當系統下次啟動畫面保護時，對此專案所做的變更就會變得有效。 當螢幕保護裝置正在執行時對此專案所做的變更，不會影響執行中的螢幕保護裝置。

## <a name="notes"></a>備註

-   當您在主控台中使用 [**顯示**] 來選取螢幕保護裝置時，Windows 作業系統會將此專案新增至登錄。 如果您從 [螢幕保護裝置程式] 清單中選擇 **([無])** 來停用所有螢幕保護裝置，則作業系統會從登錄中刪除這個專案，並呼叫 [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) 函式，其 *UiAction* 等於 SPI \_ SETSCREENSAVEACTIVE， *uiParam* 等於 **FALSE**。
-   在支援群組原則的系統上，群組原則設定會取代此專案。 啟用 **螢幕保護裝置可執行檔名稱** 群組原則設定時，系統會忽略此專案。 此原則設定的設定會儲存在 **SCRNSAVE.EXE** 專案中，該專案位於 **原則** 子機碼中。

 

 
