---
title: 工作閒置條件
description: 當電腦進入閒置狀態時，可以透過數種方式來處理工作。 這包括定義閒置觸發程式，或在工作啟動時設定閒置條件。
ms.assetid: 1e480681-b77a-48fe-a732-dd1591eaa08d
keywords:
- 閒置條件工作排程器
- 閒置條件工作排程器、討論
- 建立閒置觸發程式工作排程器
- 閒置觸發程式工作排程器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 501be9b73e3ec355b998697fb5e87c5163224b71
ms.sourcegitcommit: 857e701bbd35004661bb047e1f24622af9ff1dd7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/19/2020
ms.locfileid: "103684199"
---
# <a name="task-idle-conditions"></a>工作閒置條件

當電腦進入閒置狀態時，可以透過數種方式來處理工作。 這包括定義閒置觸發程式，或在工作啟動時設定閒置條件。

## <a name="detecting-the-idle-state"></a>偵測閒置狀態

在 Windows 7 中，工作排程器會每隔15分鐘確認電腦處於閒置狀態。 工作排程器會使用兩個準則檢查閒置狀態：使用者不存在，且缺少資源耗用量。 如果在這段時間內沒有鍵盤或滑鼠輸入，就會將使用者視為不存在。 如果所有處理器和所有磁片都閒置超過上一個偵測間隔的90%，則會將電腦視為閒置。  (設定 ES \_ 顯示所需旗標的任何簡報類型應用程式時，會發生例外狀況 \_ 。 無論使用者活動或資源耗用量為何，此旗標都會強制工作排程不要將系統視為閒置。 ) 

在 Windows 7 中，即使低優先順序執行緒 (執行緒優先順序 < 正常) 執行，工作排程器也會將處理器視為閒置。

在 Windows 7 中，當工作排程器偵測到電腦閒置時，服務只會等待使用者輸入標示閒置狀態的結尾。

在 Windows 8 中，工作排程器會執行相同的一般使用者缺少和資源耗用量檢查。 不過，工作排程器會依賴作業系統電源子系統來偵測使用者的狀態。 依預設，在沒有鍵盤或滑鼠輸入的四分鐘之後，使用者會被視為不存在。 當使用者存在時，資源耗用量驗證時間會縮短為10分鐘間隔。 當使用者離開時，驗證時間會縮短為30秒的間隔。 工作排程器會針對下列事件進行額外的資源耗用量檢查：

-   使用者狀態變更
-   AC/DC 電源來源已變更
-   電池計量 (只有在電池) 上變更

當上述任何事件發生時，工作排程器會在上次驗證時間之後，測試電腦的閒置。 在實務上，這表示如果在上次驗證時間之後已符合其他條件，工作排程器可能會在偵測到使用者不存在的情況下，立即將系統宣告為閒置。

在 Windows 8 中，CPU 和 IO 閾值會設定為80%。

偵測 Windows 8 Server 中的閒置狀態時，工作排程器不會將使用者的目前狀態或缺勤帳戶列入考慮。 為了標示閒置狀態的結尾，工作排程器在90分鐘內修改資源耗用量一次。

## <a name="defining-an-idle-trigger"></a>定義閒置觸發程式

當電腦進入閒置狀態時，您可以藉由定義閒置觸發程式來啟動工作。

閒置觸發程式只會在電腦進入觸發程式的起始界限之後進入閒置狀態時，才會觸發工作動作。

應用程式可以使用 [**IIdleTrigger**](/windows/win32/api/taskschd/nn-taskschd-iidletrigger) 介面來定義閒置觸發程式。

如果讀取或寫入 XML，閒置觸發程式是由工作排程器架構的 [**IdleTrigger**](taskschedulerschema-idletrigger-triggergroup-element.md) 元素所指定。

## <a name="task-settings-for-idle-conditions"></a>閒置條件的工作設定

工作設定可以用來定義當電腦進入閒置狀態時，工作排程器處理工作的方式。

下圖提供三個可能的時程表，顯示這些不同的閒置條件如何相互關聯。 請注意，當工作觸發程式啟動時，或工作視需要啟動時，就會啟動圖例 (而不會要求 [忽略現有的工作限制](/windows/win32/api/taskschd/ne-taskschd-task_run_flags)) 。

> [!NOTE]
> *持續時間* 和 *WaitTimeout* 設定已淘汰。 它們仍然存在於工作排程器的使用者介面中，而且其介面方法可能仍會傳回有效值，但不再使用這些值。

![閒置條件時間軸](images/idle-conditions2.png)

下列清單說明閒置條件。
- 閒置開始：電腦進入閒置狀態的時間。
- 閒置結束：電腦轉換為閒置狀態的時間。 請注意，電腦處於閒置狀態的時間量與先前所述的閒置持續時間時間無關。

閒置等候和閒置持續時間已淘汰。
- 閒置等候：當工作觸發程式啟動之後，或在視需要啟動工作之後，工作排程器將等待閒置狀態發生的時間量。
- 閒置持續時間：您希望電腦在啟動工作之前閒置的時間長度。

例如，如果工作設定為 [只有在電腦閒置30分鐘的時間才會啟動]，且工作等候電腦閒置10分鐘，則只有在啟動觸發程式之前，電腦已閒置25分鐘，工作才會在5分鐘內啟動。 如果電腦在啟動觸發程式後進入閒置狀態5分鐘，工作將不會啟動。

依預設，task [**DisallowStartIfOnBatteries**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_disallowstartifonbatteries) 屬性設定為 true，這表示工作排程器服務將不會執行閒置觸發程式所觸發的工作 (或具有閒置條件的觸發程式) 當電腦以電池電源執行時。 您可以藉由將 **DisallowStartIfOnBatteries** 屬性設定為 false，來變更此行為。

如果工作是由閒置觸發程式觸發，則會忽略 [**IIdleSettings**](/windows/desktop/api/taskschd/nn-taskschd-iidlesettings)介面 ([**IdleSettings**](idlesettings.md)的腳本) 的 [**WaitTimeout**](/windows/desktop/api/taskschd/nf-taskschd-iidlesettings-get_waittimeout)屬性。

應用程式可以藉由設定 [**IIdleSettings**](/windows/desktop/api/taskschd/nn-taskschd-iidlesettings) 和 [**IIdleTrigger**](/windows/win32/api/taskschd/nn-taskschd-iidletrigger) 介面中的屬性來控制閒置條件。

如果讀取或寫入 XML，這些條件會在工作排程器架構的 [**Settings**](taskschedulerschema-settings-tasktype-element.md) 元素中指定。

## <a name="cycling-idle-condition"></a>迴圈閒置條件

如果電腦處於閒置狀態，則您可以使用下列閒置條件來終止和重新開機工作。 若要終止和重新開機工作，必須將屬性和元素都設為 True：

-   若要在閒置條件結束時終止工作，請將 [ [**StopOnIdleEnd**](/windows/desktop/api/taskschd/nf-taskschd-iidlesettings-get_stoponidleend) ] 屬性或 [ [**StopOnIdleEnd**](taskschedulerschema-terminateonidleend-idlesettingstype-element.md) ] 元素設定為 [True]。
-   若要在電腦再次進入閒置狀態時重新開機工作，請將 [ [**RestartOnIdle**](/windows/desktop/api/taskschd/nf-taskschd-iidlesettings-get_restartonidle) ] 屬性或 [ [**RestartOnIdle**](taskschedulerschema-restartonidle-idlesettingstype-element.md) ] 元素設定為 [True]。
