---
description: 電池可提供可攜式電腦的電源，以及在不斷電供應系統供應 (UPS) 上執行的電腦。
ms.assetid: 3580b37d-611c-46b4-9300-4943833d6852
title: 電池資訊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4f9838a2a95db037b9655f116f07e3cf2e072d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106999894"
---
# <a name="battery-information"></a>電池資訊

電池可提供可攜式電腦的電源，以及在不斷電供應系統供應 (UPS) 上執行的電腦。 在這些電腦上，作業系統會提供電池狀態的相關資訊，讓應用程式可以為使用者提供實用的功能。  (不支援某些較舊的非標準電池系統和 Ups。 ) 

請注意，此總覽假設您已經熟悉 [裝置管理](/windows/desktop/DevIO/device-management)。

若要取得電池狀態的相關資訊，請使用 [**GetSystemPowerStatus**](/windows/desktop/api/Winbase/nf-winbase-getsystempowerstatus) 函式，此函式會傳回系統中所有電源來源的一般資訊。 您應該盡可能使用 **GetSystemPowerStatus** 。

不過，在某些情況下，需要每個個別電池的詳細資訊。 基於這個目的，每個電池裝置都會公開一個 IOCTL 介面。 下列 IOCTL 作業會使用 [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) 函數來執行：

<dl>

[**IOCTL \_ 電池 \_ 查詢 \_ 資訊**](ioctl-battery-query-information.md)  
[**IOCTL \_ 電池 \_ 查詢 \_ 狀態**](ioctl-battery-query-status.md)  
[**IOCTL \_ 電池 \_ 查詢 \_ 標記**](ioctl-battery-query-tag.md)  
[**IOCTL \_ 電池 \_ 設定 \_ 資訊**](ioctl-battery-set-information.md)  
</dl>

若要使用此介面，應用程式必須遵循幾個步驟。 首先，它必須使用安裝程式常式來列舉具有電池類別介面的所有裝置。 請注意，這些裝置代表電池埠，而不是系統中的實際電池。 然後，應用程式必須開啟每個裝置的控制碼，讓它可以使用 [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) 函式將要求傳送至裝置，然後取得所插入之任何電池的標記。 完成這些步驟之後，應用程式就可以將查詢傳送到每部電池裝置。

## <a name="battery-tags"></a>電池標記

因為每個電池裝置都代表可插入電池的位置，所以必須有一種方式來判斷電池何時移除、更換、更換或變更為其他任何方式。 若要這樣做，特定位置中的每個電池都會被指派一個標記。 所有查詢都必須使用這個標記來取得資訊。 如果應用程式所提供的標記與電池不符，則查詢會失敗，並向應用程式指出電池已變更。 若要成功完成查詢，需要新的電池標記。 使用 [**IOCTL \_ 電池 \_ 查詢 \_ 標記**](ioctl-battery-query-tag.md) 作業取得標記。 如果該位置中有電池，則傳回的標記可傳遞給任何其他電池 IOCTLs 來執行其他功能。 在多電池系統上，每個電池裝置 (位置) 會獨立發出電池標籤，因此來自兩個不同裝置的標籤有時可能相同。

電池標籤的變更不一定表示已移除並重新插入或更換電池。 如果任何通常是靜態的資料有變更，就可以產生新的標記。 例如，當電池充電完成時，最後一次完全收費的容量可能已變更。 如果電池通訊暫時遺失，或從 BIOS 發出不當的通知，標記也會變更。 在某些系統上，每次 AC 狀態變更時，可能會更新電池標記。 此行為是因為電池系統的特性而不常見。

只要更新電池標籤，就應該將電池視為新電池，並重新讀取所有快取的資料。 如果應用程式需要知道相同的實體電池是否存在，則應該在使用 **BatteryUniqueID** 資訊層級進行呼叫時，檢查 [**IOCTL \_ 電池 \_ 查詢 \_ 資訊**](ioctl-battery-query-information.md)的輸出緩衝區中的 **BatteryUniqueID** 值。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於電源管理](about-power-management.md)
</dt> <dt>

[列舉電池裝置](enumerating-battery-devices.md)
</dt> </dl>

 

 
