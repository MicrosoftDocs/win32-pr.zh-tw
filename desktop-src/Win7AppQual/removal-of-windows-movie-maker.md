---
description: 移除 Windows Movie Maker
ms.assetid: af55e570-0f24-4376-905a-3b879d5f3a1c
title: 移除 Windows Movie Maker
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36df5ffe4498e05de9fcbbaadf49f8fc32c91b0f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116266"
---
# <a name="removal-of-windows-movie-maker"></a>移除 Windows Movie Maker

## <a name="affected-platforms"></a>受影響的平臺

**客戶** 端-Windows 7  
**伺服器** -Windows Server 2008 R2  









## <a name="feature-impact"></a>功能影響

 **嚴重性** -高  
**頻率** -中型  


## <a name="description"></a>Description

Microsoft 淘汰和移除 Windows Movie Maker 公用程式。 這包括：

-   Windows Movie Maker 的所有進入點 (例如，[開始] 功能表、[開始] > 執行) 
-   Windows Movie Maker 所使用的所有二進位檔 (% ProgramFiles% Movie Maker 中的所有內容 \\) 

但是，使用者的 Movie Maker 專案檔會保留在系統上，並可供其他支援此檔案格式的應用程式存取。

## <a name="manifestation"></a>表現

移除 Windows Movie Maker 會導致下列情況：

-   任何使用命令列引數啟動 Windows Movie Maker 的嘗試都會失敗
-   已安裝以啟用新轉換和動畫的任何外掛程式都會保持安裝，但不會向使用者公開

## <a name="solution"></a>解決方法

若要在未來擁有這類功能，使用者將需要安裝 Microsoft 或其他軟體提供者的類似應用程式。

 

 



