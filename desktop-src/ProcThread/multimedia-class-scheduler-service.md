---
description: 多媒體類別排程器服務 (MMCSS) 可讓多媒體應用程式確保其時間緊迫的處理會獲得 CPU 資源的優先存取權。
ms.assetid: a7169938-1c72-4c4c-881a-cb08ad6182c7
title: 多媒體類別排程器服務
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80656276af30495c084d0964534a04e11896bcd2
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "103945630"
---
# <a name="multimedia-class-scheduler-service"></a>多媒體類別排程器服務

多媒體類別排程器服務 (MMCSS) 可讓多媒體應用程式確保其時間緊迫的處理會獲得 CPU 資源的優先存取權。 這項服務可讓多媒體應用程式盡可能充分利用 CPU，而不會拒絕 CPU 資源給較低優先順序的應用程式。

MMCSS 會使用儲存在登錄中的資訊來識別支援的工作，並判斷執行這些工作之執行緒的相對優先權。 執行與特定工作相關之工作的每個執行緒都會呼叫 [**AvSetMmMaxThreadCharacteristics**](/windows/desktop/api/Avrt/nf-avrt-avsetmmmaxthreadcharacteristicsa) 或 [**AvSetMmThreadCharacteristics**](/windows/desktop/api/Avrt/nf-avrt-avsetmmthreadcharacteristicsa) 函式，以通知 MMCSS 它正在處理該工作。

如需使用 MMCSS 的程式範例，請參閱 [獨佔模式資料流程](/previous-versions//bb614507(v=vs.85))。

**Windows Server 2003 和 WINDOWS XP：** MMCSS 無法使用。

## <a name="registry-settings"></a>登錄設定

MMCSS 設定會儲存在下列登錄機碼中：

**HKEY \_ LOCAL \_ MACHINE \\ SOFTWARE \\ Microsoft \\ Windows NT \\ CurrentVersion \\ 多媒體 \\ SystemProfile**

此機碼包含名為 **SystemResponsiveness** 的 **REG \_ DWORD** 值，可決定應保證低優先順序工作的 CPU 資源百分比。 例如，如果此值為20，則會為低優先順序工作保留20% 的 CPU 資源。 請注意，未平均整除的值會無條件進位到最接近10的倍數。 0值也會被視為10。

金鑰也包含名為 **tasks** 的子機碼，其中包含工作清單。 依預設，Windows 支援下列工作：

-   **音訊**
-   **擷取**
-   **Distribution**
-   **遊戲**
-   **播放**
-   **Pro 音訊**
-   **視窗管理員**

Oem 可以視需要新增其他工作。

每個工作機碼都包含下列一組值，這些值表示要套用至與工作相關聯之執行緒的特性。

| 值                   | 格式         | 可能值                                                                                                                                                                                                                                                                                                                                                         |
|-------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **親和力**            | **REG \_ DWORD** | 表示處理器親和性的位元遮罩。 0x00 和0xFFFFFFFF 都表示未使用處理器親和性。                                                                                                                                                                                                                                                 |
| **僅限背景**     | **REG \_ SZ**    | 指出這是否為背景工作 (沒有任何使用者介面) 。 背景工作的執行緒不會因為視窗焦點的變更而變更。 這個值可以設定為 True 或 False。                                                                                                                                                                            |
| **BackgroundPriority**  | **REG \_ DWORD** | 背景優先權。 值的範圍是1-8。                                                                                                                                                                                                                                                                                                                    |
| **時脈速率**          | **REG \_ DWORD** | MMCSS 用來判斷處理器資源排程之資料細微性的提示。**Windows Server 2008 和 Windows Vista：** 當執行緒加入此工作時，系統所使用的保證最大頻率（以 100-毫微秒間隔）。 從 Windows 7 和 Windows Server 2008 R2 開始，這種保證已移除，以減少系統電源耗用量。<br/> |
| **GPU 優先順序**        | **REG \_ DWORD** | GPU 優先權。 值的範圍是0-31。 尚未使用此優先順序。                                                                                                                                                                                                                                                                                           |
| **優先順序**            | **REG \_ DWORD** | 工作優先權。 值的範圍是 1 (低) 至 8 (高) 。針對 **排程類別** 為 High 的工作，此值一律會被視為2。<br/>                                                                                                                                                                                                           |
| **排程分類** | **REG \_ SZ**    | 排程分類。 這個值可以設定為 [高]、[中] 或 [低]。                                                                                                                                                                                                                                                                                                 |
| **SFIO 優先順序**       | **REG \_ SZ**    | 排程的 i/o 優先順序。 這個值可以設定為 [閒置]、[低]、[一般] 或 [高]。 不使用這個值。                                                                                                                                                                                                                                                                |



 

> [!Note]  
> 為了節省電力，除非絕對必要，否則應用程式不應該將全系統計時器的解析度設定為較小的值。 如需詳細資訊，請參閱《 [Windows 7 開發人員指南》](../win7devguide/windows-7-developer-guide.md)中的[效能](../win7devguide/performance.md)。

 

## <a name="thread-priorities"></a>執行緒優先順序

MMCSS 可提升處理高優先順序多媒體工作之執行緒的優先順序。

MMCSS 會使用下列因素來判斷線程的優先順序：

-   工作的基本優先權。
-   [**AvSetMmThreadPriority**](/windows/desktop/api/Avrt/nf-avrt-avsetmmthreadpriority)函數的 *Priority* 參數。
-   應用程式是否在前景。
-   每個類別中的執行緒所耗用的 CPU 時間量。

MMCSS 會根據其排程分類來設定用戶端執行緒的優先順序。

| 類別 | 優先順序 | Description                                                                                                                               |
|----------|----------|-------------------------------------------------------------------------------------------------------------------------------------------|
| 高     | 23-26    | 這些執行緒執行的執行緒優先順序低於特定的系統層級工作。 此類別是針對 Pro 音訊工作所設計。 |
| 中   | 16-22    | 這些執行緒是前景中的應用程式的一部分。                                                                      |
| 低      | 8-15     | 此類別包含其餘的執行緒。 必要時，系統會保證 CPU 資源的最小百分比。           |
|          | 1-7      | 這些執行緒已使用其 CPU 資源的配額。 如果沒有可用的低優先順序執行緒可供執行，則可以繼續執行。                |



 

 

 
