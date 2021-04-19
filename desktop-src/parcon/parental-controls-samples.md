---
description: 家長監護範例
ms.assetid: 19dac95c-2279-4bf9-a58c-dd30177c0c9d
title: 家長監護範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26962f4edd16e1e860883607316d5a7cbf3d9122
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988360"
---
# <a name="parental-controls-samples"></a>家長監護範例

家長監護的範例程式碼可在 [路徑 <installation directory> \\ Windows \\ <version number> \\ 範例 \\ 安全性 \\ ParentalControls] 底下取得。 範例如下所示：

## <a name="utilities"></a>公用程式

適用于基本 COM 管理、SID 字串作業，以及 WMI 讀取和寫入功能的 Helper 功能。 除非另有指定，否則所有其他範例都會相依于這個專案。

## <a name="complianceapi"></a>ComplianceAPI

命令列導向的主控台應用程式，示範如何使用合規性 API 來取得使用者的主要設定子集。

## <a name="complianceapp"></a>ComplianceApp

簡單的主控台應用程式，示範如何使用合規性 API 來檢查所需的記錄和特定的限制。 如果啟用時間限制，應用程式也會等待即將進行的登出事件。

## <a name="uiextensibility"></a>UIExtensibility

命令列導向的主控台應用程式，示範如何使用 WMI Api 和 WPC 架構來列出、查詢、新增、修改和刪除 UI 擴充性連結專案。

範例命令列範例：

"D： \\ WPC \\ Samples \\ Security \\ ParentalControls \\ UIExtensibility \\ debug \\ UIExtensibility" add/g： {FD59BB7F-54AB-11DB-9666-00E08161165F}/c： 0/N： D：/WPC/Samples/Security/ParentalControls/UiExtRC/debug/UiExtRC.dll，-101/S： D：/WPC/Samples/Security/ParentalControls/UiExtRC/debug/UiExtRC.dll，-103/I： D：/WPC/Samples/Security/ParentalControls/UiExtRC/debug/UiExtRC.dll，-104/D： D：/WPC/Samples/Security/ParentalControls/UiExtRC/debug/UiExtRC.dll，-106/e： c： \\ windows \\Notepad.exe

其中 UiExtRC 是簡單的資源 DLL，其中包含識別碼為101和103的字串資源，而24x24 圖元32位具有適用于資源104和106的 Alpha 點陣圖。

## <a name="webextensibility"></a>WebExtensibility

命令列導向的主控台應用程式，示範如何使用 WMI Api 和 WPC 架構來列出、新增和刪除 HTTP 應用程式或 URL 豁免專案，以及使用 FilterID 和 FilterName 屬性來設定和重設 Web 內容篩選覆寫。

不會顯示唯讀 HTTP 應用程式和 URL 豁免清單的存取權，但讀取清單的程式碼與讀取/寫入案例的程式碼相同，除了 WMI 參數的修改之外。

 

 



