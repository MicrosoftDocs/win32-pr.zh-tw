---
title: 取得系統時間
description: 取得系統時間
ms.assetid: 33dfcd56-11d9-45b9-b983-8354526101a7
keywords:
- 多媒體計時器，系統時間
- 計時器，系統時間
- 系統時間
- timeGetTime 函式
- timeGetSystemTime 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45460078776732234510d7308bd1e8f490e3871334bdf950bcedd77943b430e6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119806468"
---
# <a name="obtaining-the-system-time"></a>取得系統時間

通常，在應用程式開始使用多媒體計時器服務之前，它會先抓取目前的 *系統時間*。 系統時間是從 Microsoft Windows 作業系統開始的時間（以毫秒為單位）。 您可以使用 [**timeGetTime**](/windows/desktop/api/TimeAPI/nf-timeapi-timegettime) 或 [**timeGetSystemTime**](/windows/desktop/api/TimeAPI/nf-timeapi-timegetsystemtime) 函數來取得系統時間。 這兩個函數非常類似： **timeGetTime** 會傳回系統時間，而 **timeGetSystemTime** 會以系統時間填滿 [**MMTIME**](/previous-versions//dd757347(v=vs.85)) 結構。

 

 