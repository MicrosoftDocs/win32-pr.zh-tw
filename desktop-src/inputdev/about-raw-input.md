---
title: 關於原始輸入
description: 本主題討論裝置的使用者輸入，例如操作杆、觸控式螢幕和麥克風。
ms.assetid: 013ed309-f667-47ed-ade0-5e7ca5a0997a
keywords:
- 使用者輸入，原始輸入
- 捕獲使用者輸入，原始輸入
- 原始輸入
- 註冊原始輸入
- 讀取原始輸入
- 搖桿原始輸入
- 觸控式螢幕原始輸入
- 麥克風原始輸入
- 人性化介面裝置 (HID)
- " (人體介面裝置) 的 HID"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3535e5601ec63a254c76060611999a1a2f08aeb
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104023469"
---
# <a name="about-raw-input"></a>關於原始輸入

傳統鍵盤和滑鼠旁邊有許多使用者輸入的裝置。 例如，使用者輸入可以來自搖桿、觸控式螢幕、麥克風或其他裝置，以在使用者輸入方面有很大的彈性。 這些裝置統稱為人類介面裝置， (HIDs) 。 原始輸入 API 提供穩定且健全的方式，讓應用程式接受來自任何 HID 的原始輸入，包括鍵盤和滑鼠。

本節包含下列主題：

-   [原始輸入模型](#raw-input-model)
-   [原始輸入的註冊](#registration-for-raw-input)
-   [讀取原始輸入](#reading-raw-input)

## <a name="raw-input-model"></a>原始輸入模型

之前，鍵盤和滑鼠通常會產生輸入資料。 系統會將來自這些裝置的資料，以消除未經處理之資訊的裝置特定詳細資料的方式來解讀。 例如，鍵盤會產生裝置特定的掃描碼，但系統會提供具有虛擬金鑰碼的應用程式。 除了隱藏原始輸入的詳細資料之外，「視窗管理員」並不支援所有的新 HIDs。 若要從不支援的 HIDs 取得輸入，應用程式必須執行許多工作：開啟裝置、管理共用模式、定期讀取裝置或設定 i/o 完成埠等等。 原始輸入模型和相關聯的 Api 的開發目的，是為了讓您能夠從所有輸入裝置（包括鍵盤和滑鼠）中輕鬆存取原始輸入。

原始輸入模型與鍵盤和滑鼠的原始 Windows 輸入模型不同。 在原始輸入模型中，應用程式會以傳送或張貼至其 windows 的訊息形式（例如 [**wm \_ CHAR**](wm-char.md)、 [**WM \_ MOUSEMOVE**](wm-mousemove.md)和 [**wm \_ APPCOMMAND**](wm-appcommand.md)）接收與裝置無關的輸入。 相反地，對於原始輸入，應用程式必須註冊要從中取得資料的裝置。 此外，應用程式也會透過 [**WM \_ 輸入**](wm-input.md) 訊息取得原始輸入。

原始輸入模型有幾個優點：

-   應用程式不需要偵測或開啟輸入裝置。
-   應用程式會直接從裝置取得資料，並處理資料以滿足其需求。
-   應用程式即使是來自相同類型的裝置，也可以區別輸入的來源。 例如，兩個滑鼠裝置。
-   應用程式會從裝置集合或僅指定特定裝置類型的資料，來管理資料流量。
-   您可以使用 HID 裝置，因為它們在 marketplace 中可供使用，而不需要等候新的訊息類型或更新的 OS 在 [**WM \_ APPCOMMAND**](wm-appcommand.md)中有新的命令。

請注意， [**WM \_ APPCOMMAND**](wm-appcommand.md) 確實提供某些 HID 裝置。 不過， **wm \_ APPCOMMAND** 是較高層級的裝置獨立輸入事件，而 [**wm \_ 輸入**](wm-input.md) 會傳送裝置特定的原始、低層級資料。

## <a name="registration-for-raw-input"></a>原始輸入的註冊

依預設，沒有任何應用程式會接收原始輸入。 若要接收來自裝置的原始輸入，應用程式必須註冊裝置。

若要註冊裝置，應用程式會先建立 [**RAWINPUTDEVICE**](/windows/win32/api/winuser/ns-winuser-rawinputdevice) 結構的陣列，以指定其所要裝置的 [最上層集合](/windows-hardware/drivers/hid/top-level-collections) (TLC) 。 TLC 是由 () 裝置類別的 [使用方式頁面](/windows-hardware/drivers/hid/hid-usages#usage-page) 所定義，) 中 (裝置的 [使用識別碼](/windows-hardware/drivers/hid/hid-usages#usage-id) 。 例如，若要取得鍵盤 TLC，請設定 UsagePage = 0x01 和 UsageID = 0x06。 應用程式會呼叫 [**RegisterRawInputDevices**](/windows/win32/api/winuser/nf-winuser-registerrawinputdevices) 來註冊裝置。

請注意，應用程式可以註冊目前未連接到系統的裝置。 連接此裝置時，Windows 管理員會自動將原始輸入傳送至應用程式。 為了取得系統上的原始輸入裝置清單，應用程式會呼叫 [**GetRawInputDeviceList**](/windows/win32/api/winuser/nf-winuser-getrawinputdevicelist)。 使用此呼叫中的 *hDevice* ，應用程式會呼叫 [**GetRawInputDeviceInfo**](/windows/win32/api/winuser/nf-winuser-getrawinputdeviceinfoa) 來取得裝置資訊。

透過 [**RAWINPUTDEVICE**](/windows/win32/api/winuser/ns-winuser-rawinputdevice)的 **dwFlags** 成員，應用程式可以選取要接聽的裝置，以及想要忽略的裝置。 例如，應用程式可以要求所有電話語音裝置的輸入，但無法接聽電腦。 如需範例程式碼，請參閱 [註冊原始輸入](using-raw-input.md)。

請注意，滑鼠和鍵盤也會 HIDs，因此來自這些資料的資料可能會同時通過 HID 訊息 [**WM \_ 輸入**](wm-input.md) 和傳統的訊息。 應用程式可以藉由在 [**RAWINPUTDEVICE**](/windows/win32/api/winuser/ns-winuser-rawinputdevice)中適當地選取旗標來選取任一種方法。

若要取得應用程式的註冊狀態，請在任何時間呼叫 [**GetRegisteredRawInputDevices**](/windows/win32/api/winuser/nf-winuser-getregisteredrawinputdevices) 。

## <a name="reading-raw-input"></a>讀取原始輸入

應用程式會從其 [最上層集合](/windows-hardware/drivers/hid/top-level-collections) (TLC) 符合註冊中 TLC 的任何隱藏專案接收原始輸入。 當應用程式收到未經處理的輸入時，它的訊息佇列會取得 [**WM \_ 輸入**](wm-input.md) 訊息，並將佇列狀態旗標設定為 **QS \_ RAWINPUT** (**QS \_ 輸入** 也包含此旗標) 。 當應用程式在前景以及在背景時，可以接收資料。

有兩種方式可以讀取原始資料：未緩衝的 (或標準) 方法和緩衝處理的方法。 未緩衝處理的方法會一次取得一 [**RAWINPUT**](/windows/win32/api/winuser/ns-winuser-rawinput) 結構的原始資料，而且適用于許多 HIDs。 在此，應用程式會呼叫 [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) 來取得 [**WM \_ 輸入**](wm-input.md) 訊息。 然後，應用程式會使用包含在 **WM \_ 輸入** 中的 **RAWINPUT** 控制碼來呼叫 [**GetRawInputData**](/windows/win32/api/winuser/nf-winuser-getrawinputdata) 。 如需範例，請參閱 [執行原始輸入的標準讀取](using-raw-input.md)。

相反地，經過緩衝處理的方法會一次取得 [**RAWINPUT**](/windows/win32/api/winuser/ns-winuser-rawinput) 結構的陣列。 這是針對可能產生大量原始輸入的裝置而提供。 在這個方法中，應用程式會呼叫 [**GetRawInputBuffer**](/windows/win32/api/winuser/nf-winuser-getrawinputbuffer) 來取得 **RAWINPUT** 結構的陣列。 請注意， [**NEXTRAWINPUTBLOCK**](/windows/win32/api/winuser/nf-winuser-nextrawinputblock) 宏是用來跨越 **RAWINPUT** 結構的陣列。 如需範例，請參閱 [執行原始輸入的緩衝讀取](using-raw-input.md)。

若要解讀原始輸入，需要 HIDs 的詳細資訊。 應用程式會藉由呼叫 [**GetRawInputDeviceInfo**](/windows/win32/api/winuser/nf-winuser-getrawinputdeviceinfoa) 和裝置控制碼來取得裝置資訊。 這個控制碼可以來自 [**WM \_ 輸入**](wm-input.md)或來自 [**RAWINPUTHEADER**](/windows/win32/api/winuser/ns-winuser-rawinputheader)的 **hDevice** 成員。