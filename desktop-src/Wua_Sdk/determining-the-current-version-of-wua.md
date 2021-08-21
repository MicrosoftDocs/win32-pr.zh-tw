---
description: 使用之前，請先判斷 Windows Update 代理程式 (WUA) 的版本。
ms.assetid: fc915535-f87d-43fb-8755-fa6c80fedea5
title: 判斷 WUA 的目前版本
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa8d8e013f4e8189c71b9e4510fdaebcdf1e2f749e3d8dfffd6256128e214ce4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119049496"
---
# <a name="determining-the-current-version-of-wua"></a>判斷 WUA 的目前版本

如需更新 WUA 的一般資訊，包括逐步指示，以程式設計方式在應用程式中判斷電腦上執行的 WUA 版本是否符合您的需求，請參閱[更新 Windows Update 代理程式](updating-the-windows-update-agent.md)。

在 Windows 7 和 Windows Server 2008 R2 之前的 Windows 版本上，您應該先判斷已安裝的 Windows Update 代理程式版本 (WUA) 再使用它。 目前的 WUA 版本取決於 \\ 目前 Windows 安裝的 System32 子目錄中執行的 Wuaueng.dll 版本。 如果 Wuaueng.dll 的版本是5.4.3790.1000 版或更新版本，則會安裝 WUA。 早于5.4.3790.1000 的版本表示安裝了 (SUS) 1.0 的軟體更新服務。

使用 WUA API 對 su 1.0 進行呼叫時，  \_ \_ \_ 會傳回 WU E AU LEGACYSERVER 的 HRESULT。

您也可以使用 [**IWindowsUpdateAgentInfo：： GetInfo**](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsupdateagentinfo-getinfo) 方法來取得電腦上正在執行之 Wuapi.dll 的目前檔案版本。 在 WUA 1.0 中不支援 [**IWindowsUpdateAgentInfo**](/windows/desktop/api/Wuapi/nn-wuapi-iwindowsupdateagentinfo) 介面。
