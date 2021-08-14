---
description: Windows 錯誤報告問題步驟收錄程式
ms.assetid: ce5db84a-53b6-4a7f-bee4-d198d8a6781e
title: Windows 錯誤報告問題步驟收錄程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ba90b76b3d486dc0708e0803609539fda6d6141d0a6f3ab100ba0ce198846fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118328080"
---
# <a name="windows-error-reporting-problem-steps-recorder"></a>Windows 錯誤報告問題步驟收錄程式

## <a name="affected-platforms"></a>受影響的平臺

**用戶端**– Windows 7  
**伺服器**– Windows Server 2008 R2  


## <a name="description"></a>Description

在 Windows 7 之前，Windows 錯誤報告 (WER) 收集到的錯誤報表指出需要修復的問題。 這些錯誤報表包含實用的資訊，描述問題的一般本質，但無法判斷其根本原因的資訊。 針對這一點，開發人員需要一個工具來重現當機/停止回應案例以進行偵錯工具。

新的應用程式問題步驟收錄程式 (PSR.exe) ）會在 Windows 7 的所有組建上寄出。 這項功能可讓使用者在遇到損毀時，收集使用者所執行的動作，讓測試人員和開發人員可以重現分析和偵測的情況。

## <a name="usage"></a>使用方式

目前，Windows 錯誤報告服務開發人員必須要求應用程式的 PSR 啟用;Microsoft 支援組織也會在與終端使用者進行疑難排解時使用此工具。 方案已備妥 Windows 品質線上服務提供的 PSR (Winqual) Windows 7 發行之後。

**注意：** 針對應用程式啟用 PSR 之後，應用程式可能會看到效能降低的情況。

## <a name="links-to-other-resources"></a>其他資源的連結

-   [Windows 錯誤報告的 blog 專案](/archive/blogs/wer/)
-   [Windows優質線上服務 (Winqual) ](https://winqual.microsoft.com)

 

 
