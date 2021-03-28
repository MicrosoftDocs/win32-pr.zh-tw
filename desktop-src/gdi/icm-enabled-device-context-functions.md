---
description: Microsoft 影像色彩管理 (ICM) 可確保色彩影像、圖形或文字物件在任何裝置上都能盡可能地轉譯為其原始意圖，儘管裝置之間的映射技術和色彩功能有所差異。
ms.assetid: eced18cf-be5a-4c61-b0e5-36d607daa6ff
title: ICM-Enabled 裝置內容函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95a0b49e62d0b4d05e0690d2aee0d3c5f0f530cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972664"
---
# <a name="icm-enabled-device-context-functions"></a>ICM-Enabled 裝置內容函式

Microsoft 影像色彩管理 (ICM) 可確保色彩影像、圖形或文字物件在任何裝置上都能盡可能地轉譯為其原始意圖，儘管裝置之間的映射技術和色彩功能有所差異。  (需詳細資訊，請參閱 [Windows Color System](/previous-versions//dd372446(v=vs.85)). ) 

圖形裝置介面中有各種不同的函式 (使用或操作色彩資料的 GDI) 。 下列裝置內容函式已啟用以搭配 ICM 使用：

-   [**CreateCompatibleDC**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatibledc)
-   [**CreateDC**](/windows/desktop/api/Wingdi/nf-wingdi-createdca)
-   [**GetDCBrushColor**](/windows/desktop/api/WinGdi/nf-wingdi-getdcbrushcolor)
-   [**GetDCPenColor**](/windows/desktop/api/WinGdi/nf-wingdi-getdcpencolor)
-   [**ResetDC**](/windows/desktop/api/Wingdi/nf-wingdi-resetdca)
-   [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject)
-   [**SetDCBrushColor**](/windows/desktop/api/Wingdi/nf-wingdi-setdcbrushcolor)
-   [**SetDCPenColor**](/windows/desktop/api/Wingdi/nf-wingdi-setdcpencolor)

 

 
