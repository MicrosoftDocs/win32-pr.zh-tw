---
description: 每個實體顯示器都會以 HMONITOR 類型的監視器控制碼表示。
ms.assetid: c43c1401-52d3-485e-a418-205df5737040
title: HMONITOR 和裝置內容
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afb727457c388710b19d8f22bef8f65d76e9d8c5c27b0ec7dfcbf55a4acea3b0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119558748"
---
# <a name="hmonitor-and-the-device-context"></a>HMONITOR 和裝置內容

每個實體顯示器都會以 **HMONITOR** 類型的監視器控制碼表示。 有效的 **HMONITOR** 保證為非 Null。 實體顯示器具有相同的 **HMONITOR** ，只要它是桌面的一部分。 傳送 **WM \_ DISPLAYCHANGE** 訊息時，可能會從桌面上移除任何監視器，因此其 **HMONITOR** 會變成無效或其設定已變更。 因此，應用程式應該在傳送此訊息時，檢查所有 **HMONITORS** 是否有效。

任何會傳回顯示裝置內容 (DC) 的函式通常會傳回主要監視的 DC。 若要取得其他監視器的 DC，請使用 [**EnumDisplayMonitors**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaymonitors) 函數。 或者，您可以使用 [**GetMonitorInfo**](/windows/desktop/api/Winuser/nf-winuser-getmonitorinfoa) 函式中的裝置名稱，建立具有 [**CreateDC**](/windows/desktop/api/Wingdi/nf-wingdi-createdca)的 DC。 但是，如果函式（例如 [**GetWindowDC**](/windows/desktop/api/Winuser/nf-winuser-getwindowdc) 或 [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint)）取得跨越多個顯示之視窗的 dc，則 dc 也會橫跨這兩個顯示。

 

 



