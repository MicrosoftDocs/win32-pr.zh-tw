---
description: 若要在處理 WM DEVICECHANGE 訊息時判斷裝置事件種類 \_ ，請檢查 wParam 參數。
ms.assetid: 17078548-879d-4a11-a268-27d1f30180ab
title: 裝置事件種類
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f4d807cd7524d1906e86113c546306e08051ea80770900d42c1233364430e22
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119636638"
---
# <a name="device-event-types"></a>裝置事件種類

若要在處理 [**WM \_ DEVICECHANGE**](wm-devicechange.md) 訊息時判斷裝置事件種類，請檢查 *wParam* 參數。 *WParam* 的值會決定 *lParam* 參數中事件特定資料的意義。 一般而言，事件特定的資料會識別裝置，並提供事件的其他詳細資料。 這項資料的格式取決於裝置類型，但前幾個位元組的格式一律與 [**開發 \_ 廣播 \_ HDR**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) 結構相同。 若要判斷資料的格式，請檢查 **dbch \_ devicetype** 成員。

系統會廣播 [DBT (\_ DEVICEARRIVAL](dbt-devicearrival.md)類型的裝置事件，也就是每次插入裝置並可供使用時， *wParam* 設定為 DBT DEVICEARRIVAL) 的 [**WM \_ DEVICECHANGE**](wm-devicechange.md)訊息 \_ 。 應用程式通常會檢查裝置類型，並在適用時立即開始使用裝置。

系統會廣播 [DBT \_ DEVICEQUERYREMOVE](dbt-devicequeryremove.md) 裝置事件，以要求移除裝置的許可權。 若要判斷是否需要裝置，應用程式可以顯示對話方塊以提示使用者提供指示。 如果應用程式判斷它需要裝置，則可以拒絕此要求，並藉由傳回廣播查詢拒絕來取消移除 \_ \_ 。 如果應用程式不需要裝置，則必須傳回 **TRUE**。 如果有任何應用程式或驅動程式取消先前的移除裝置要求，系統就會立即傳送 [DBT \_ DEVICEQUERYREMOVEFAILED](dbt-devicequeryremovefailed.md) 訊息。

在移除裝置之前，系統會將 [DBT \_ DEVICEREMOVEPENDING](dbt-deviceremovepending.md) 裝置事件廣播為最後一項警告。 此時，應用程式無法取消移除，所以如果它正在使用裝置，它必須準備移除以防止資料遺失。 這在移除網路連線時特別重要。 應用程式必須判斷其開啟的檔案或管道是否在該連接上。 它可以藉由比較訊息的事件特定資料中的網路資源識別碼與先前為檔案和管道取得的資源識別碼，來達成此目的。 當裝置已移除且無法再使用時，系統會廣播 [DBT \_ DEVICEREMOVECOMPLETE](dbt-deviceremovecomplete.md) 裝置事件。

系統會廣播 [DBT \_ QUERYCHANGECONFIG](dbt-querychangeconfig.md) 裝置事件，以要求 (dock 或取消停駐) 變更目前設定的許可權。 任何應用程式都可以 \_ 傳回 \_ 「廣播查詢拒絕」以拒絕要求，並取消變更。 如果應用程式拒絕要求，系統會傳送 [DBT \_ CONFIGCHANGECANCELED](dbt-configchangecanceled.md) 訊息。 如果目前的設定已變更，由於 dock 或取消停駐，系統會傳送 [DBT \_ CONFIGCHANGED](dbt-configchanged.md) 訊息。

每當發生裝置特定事件時，系統就會廣播 [DBT \_ DEVICETYPESPECIFIC](dbt-devicetypespecific.md) 裝置事件。

驅動程式可以建立自己的自訂事件種類。 自訂事件只會傳送至已在特定裝置上註冊裝置事件通知的應用程式，而且只能由核心模式驅動程式初始化。 如需詳細資訊，請參閱 [DBT \_ CUSTOMEVENT](dbt-customevent.md)。

 

 



