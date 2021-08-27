---
description: 移除 Windows Movie Maker
ms.assetid: af55e570-0f24-4376-905a-3b879d5f3a1c
title: 移除 Windows Movie Maker
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 538032d589439ccc0966bc151568813eed3d1946cd2cb8ea7d9314246edb19ee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120098518"
---
# <a name="removal-of-windows-movie-maker"></a>移除 Windows Movie Maker

## <a name="affected-platforms"></a>受影響的平臺

**客戶** 端-Windows 7  
**伺服器**-Windows Server 2008 R2  









## <a name="feature-impact"></a>功能影響

 **嚴重性** -高  
**頻率** -中型  


## <a name="description"></a>描述

Microsoft 會淘汰和移除 Windows Movie Maker 公用程式。 這包括：

-   所有進入點至 Windows Movie Maker (例如 [開始] 功能表、[開始] > 執行) 
-   Windows Movie Maker 所使用的所有二進位檔 (% ProgramFiles% Movie Maker 中的所有內容 \\) 

但是，使用者的 Movie Maker 專案檔會保留在系統上，並可供其他支援此檔案格式的應用程式存取。

## <a name="manifestation"></a>表現

移除 Windows Movie Maker 會導致下列情況：

-   嘗試以其命令列引數啟動 Windows Movie Maker 將會失敗
-   已安裝以啟用新轉換和動畫的任何外掛程式都會保持安裝，但不會向使用者公開

## <a name="solution"></a>解決方案

若要在未來擁有這類功能，使用者將需要安裝 Microsoft 或其他軟體提供者的類似應用程式。

 

 



