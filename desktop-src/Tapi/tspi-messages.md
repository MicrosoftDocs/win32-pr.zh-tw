---
description: 本節包含電話語音服務提供者介面 (TSPI) 中的訊息清單。
ms.assetid: 3d8bf980-81d6-49db-954f-af72458365dc
title: TSPI 訊息
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f5772a1ccb0c07f03b2a17348ecf5e4834bb97a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978359"
---
# <a name="tspi-messages"></a>TSPI 訊息

本節包含電話語音服務提供者介面 (TSPI) 中的訊息清單。 這些訊息是用來通知 TAPI 出現在服務提供者內出現的非同步事件。 服務提供者會藉由呼叫 [**LINEEVENT**](/windows/win32/api/tspi/nc-tspi-lineevent) 或 [**PHONEEVENT**](/windows/desktop/api/tspi/nc-tspi-phoneevent) 回呼函式，將這些事件傳遞至 TAPI，視服務提供者是否線上路、電話或電話裝置上報告事件而定。 使用 [**TSPI \_ lineOpen**](/windows/win32/api/tspi/nf-tspi-tspi_lineopen)函式開啟行時，會提供服務提供者給服務提供者的報告事件所發生的 **LINEEVENT** 程式。 在手機上進行報告事件的 **PHONEEVENT** 程式是由 [**TSPI \_ phoneOpen**](/windows/win32/api/tspi/nf-tspi-tspi_phoneopen) 函式提供。

這些自發事件是由 TAPI 要求，因為它們不是直接回應任何要求。 這些事件會與報告完成 TAPI 發出要求的事件相對比。 這類完成事件會透過 [**非同步 \_ 完成**](/windows/win32/api/tspi/nc-tspi-async_completion) 回呼函數報告。

自發事件程式的參數設定檔包含參數，這些參數會識別要向其報告事件的相關物件， (電話、行或呼叫) 。 識別的形式為不透明的控制碼，其確切的轉譯不是由 TSPI 所發行。 TAPI 會在內部判斷這些不透明的控制碼，以及它用來代表裝置的任何資料結構之間的關聯性。

自發事件程式的參數設定檔也包含可識別訊息型別的訊息參數。 每個訊息類型都有對應的定義，可決定所包含的控制碼，以及其他參數和其意義。 出現在 TSPI 層級的訊息與出現在 TAPI 層級的訊息之間有很強的對應關係。 以下是對應的一般規則：

-   這組訊息幾乎完全相同。 訊息對應的位置，會在 TSPI 層級使用相同的訊息名稱和值。
-   在 TSPI 層級顯示的控制碼是 TSPI 規格所定義的不透明類型。 這些類型 (與其轉譯) 與 TAPI 層級不同，但它們參考的裝置類別相同。 例如，在 TAPI 訊息包含 HLINE 控制碼的情況下，對應的 TSPI 訊息通常會包含 [**HTAPILINE**](htapiline.md) 控制碼。
-   沒有任何 *dwCallbackInstance* 資料會傳遞至回呼。
-   *DwParam1*、 *dwParam2* 和 *dwParam3* 參數通常與 TAPI 訊息的對應參數相同。
-   行導向和呼叫導向的訊息會傳遞至與電話導向訊息不同的回呼程式。

針對每個訊息，此區段會列出下列專案：

-   訊息的用途
-   傳遞此訊息的回呼程式
-   訊息參數的描述
-   使用訊息的選擇性批註
-   其他函式、訊息和資料結構的選擇性參考
-   將此訊息與 TAPI 介面比較的選擇性批註

某些訊息是用來通知 TAPI 有關物件狀態的變更。 這些訊息提供 TAPI 不透明的物件控制碼，以及指出哪些狀態專案已變更。 TAPI 接著可以呼叫物件的適當「取得狀態」功能，以取得物件的完整狀態。

當事件發生時，訊息可能會或可能不會傳送至 TAPI。 針對某些事件種類（例如狀態變更），TAPI 會指定一組感興趣的狀態變更。 建議服務提供者將它報告的狀態變更訊息事件限制為包含在此集合中的事件。 服務提供者不需要遵守此限制。 換句話說，它可能會報告比絕對必要更多的變更。 不過，它應該會基於效能考慮而嘗試觀察限制。

行 \_ 回復訊息不會在 TSPI 層級使用。 非同步要求的完成會使用 [**非同步 \_ 完成**](/windows/win32/api/tspi/nc-tspi-async_completion) 回呼來回報。

電話 \_ 回復訊息不會在 TSPI 層級使用。 非同步要求的完成會使用 [**非同步 \_ 完成**](/windows/win32/api/tspi/nc-tspi-async_completion) 回呼來回報。

如需詳細資訊，請參閱下列主題：

-   [TSPI 線路裝置訊息](tspi-line-device-messages.md)
-   [TSPI Phone 裝置訊息](tspi-phone-device-messages.md)

 

 
