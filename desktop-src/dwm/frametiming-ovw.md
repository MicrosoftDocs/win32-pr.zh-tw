---
title: 存取及控制 DWM 框架資料
description: 本主題討論用於排程和媒體簡報的桌面視窗管理員 (DWM) Api。
ms.assetid: e5d010ea-8411-4537-b9f8-6dc84841087a
keywords:
- 桌面視窗管理員 (DWM) 、排程和媒體呈現 Api
- DWM (桌面視窗管理員) 、排程和媒體呈現 Api
- 排程和媒體簡報 Api
- 桌面視窗管理員 (DWM) ，存取畫面格資料
- DWM (桌面視窗管理員) ，存取畫面格資料
- 存取畫面格資料
- 桌面視窗管理員 (DWM) ，控制框架資料
- DWM (桌面視窗管理員) ，控制框架資料
- 控制框架資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a577847dc20883c84af680d1c39e285a6085e70
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301019"
---
# <a name="accessing-and-controlling-dwm-frame-data"></a>存取及控制 DWM 框架資料

本主題討論用於排程和媒體簡報的桌面視窗管理員 (DWM) Api。

## <a name="dwm-frame-timing-api"></a>DWM 框架計時 API

排程和媒體呈現 Api 可讓您更詳細地控制桌面映射的組成和呈現時間。 這通常是針對 DWM 以其本身的呈現排程以非同步方式執行的媒體和影片播放應用程式所需要，如果未受到嚴格控制，則可能會導致取樣構件。

排程和媒體展示功能包含下列各項。 在這些頁面上可以找到其使用的詳細資料。

-   [**DwmEnableMMCSS**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablemmcss)。 通知 DWM 在呼叫進程保持運作時，啟用多媒體類別排程服務 (MMCSS) 排程。
-   [**DwmGetCompositionTimingInfo**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetcompositiontiminginfo)。 抓取目前的組合計時資訊。
-   [**DwmModifyPreviousDxFrameDuration**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmmodifypreviousdxframeduration)。 變更將顯示上一個畫面格的重新整理次數。
-   [**DwmSetDxFrameDuration**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetdxframeduration)。 設定要在其中顯示所呈現畫面格的重新整理次數。
-   [**DwmSetPresentParameters**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetpresentparameters)。 設定框架組合的目前參數。

 

 




