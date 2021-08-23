---
title: 物件管理
description: 本節涵蓋 Windows 篩選平台 (WFP) API 物件類型的正確用法。
ms.assetid: 2625ef9a-0e62-4e21-ba93-047965d0d782
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5cb51d4e78049d7911a4a5ed265091e05bc1cbb00ce470e332d59dd23c6026d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119068848"
---
# <a name="object-management"></a>物件管理

本節涵蓋 Windows 篩選平台 (WFP) API 物件類型的正確用法。

## <a name="sessions"></a>工作階段

WFP API 是會話導向的，大部分的函式呼叫都是在會話的內容中進行。 藉由呼叫 [**FwpmEngineOpen0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineopen0)來建立新的用戶端會話。 當用戶端呼叫 [**FwpmEngineClose0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineclose0) 或用戶端進程終止時，會話便會結束。 當會話損毀時（基於用途或 RPC 取消），基礎篩選引擎 (BFE) 先中止任何現有的交易。

建立新的會話時，呼叫端可以將 [**FWPM \_ 會話 \_ 旗標 \_ 動態**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_session0) 旗標傳遞給 [**FwpmEngineOpen0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineopen0)，以建立動態會話。 當會話結束時，會自動刪除動態會話期間加入的任何物件。

## <a name="transactions"></a>交易

WFP API 是交易式的，大部分的函式呼叫都是在交易的內容中進行。 呼叫端可以使用 [**FwpmTransactionBegin0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmtransactionbegin0)、 [**FwpmTransactionCommit0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmtransactioncommit0)和 [**FwpmTransactionAbort0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmtransactionabort0) 來明確控制交易。 但是，如果在明確交易之外進行函式呼叫，則會在隱含交易內執行函式。 如果交易正在進行中，當會話終止時，它會自動中止。 永遠不會強制中止隱含交易。

交易可以是唯讀或讀取/寫入，而且會強制執行嚴格的不可部分完成一致性隔離持久 ([ACID](../cossdk/acid-properties.md)) 的語法。

每個用戶端會話一次只能有一個交易在進行中。 如果呼叫端在認可或中止第一個交易之前嘗試開始第二個交易，BFE 會傳回錯誤。

如果作業在交易過程中失敗，則不會影響交易的整體狀態。 例如，假設用戶端開始交易，並在第四個呼叫失敗之前成功呼叫 [**FwpmFilterAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilteradd0) 三次。 用戶端現在可以選擇下列選項：

-   中止交易，在這種情況下，將不會新增任何篩選。
-   認可交易，在這種情況下，將會新增前三個篩選準則。
-   繼續進行更多作業，包括可能會重試失敗的 [**FwpmFilterAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilteradd0)。

開始交易時，BFE 會等待會話的 [**txnWaitTimeoutInMSec**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_session0) 到期，以取得鎖定。 如果在這段時間內未取得鎖定，則鎖定取得 (，且 [**FwpmTransactionBegin0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmtransactionbegin0) 呼叫) 將會失敗。 這可防止用戶端無限期地回應。 如果用戶端未指定鎖定超時，則預設為15秒。

每一筆交易也有鎖定超時。 這是它可以擁有鎖定的最大時間量。 如果擁有者未在這段時間內釋放鎖定，則會強制中止交易，而導致釋放鎖定。 鎖定超時無法設定。 它對核心模式呼叫端是無限的，而且使用者模式呼叫端的時間是一小時。 如果交易遭到強制中止，則在該交易內進行的下一次呼叫會失敗，並會 **\_ \_ \_ 中止 TXN**。

## <a name="object-lifetimes"></a>物件存留期

物件可以有四個可能的存留期之一：

-   動態—只有在使用動態會話控制碼加入物件時，物件才會是動態的。 動態物件會一直存留，直到其被刪除或擁有會話終止為止。
-   靜態：物件預設為靜態。 靜態物件會一直存留到刪除為止、BFE 停止或系統關機。
-   持續性：持續性物件是藉由將適當的 **FWPM \_ \* \_ 旗標 \_ 持續** 旗標傳遞給 **FWPM \* Add0** 函式所建立。 持續性物件會存留到刪除為止。
-   內建-內建物件是由 BFE 預先定義，無法新增或刪除。 它們會永遠存留。

您可以藉由將適當的旗標傳遞給 [**FwpmFilterAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilteradd0)，將核心模式層中的篩選標記為開機時間篩選器。 開機時間篩選器會在 TCP/IP 驅動程式啟動時新增至系統，並在 BFE 完成初始化時移除。 當 BFE 啟動時，就會新增持續性物件。

在許多情況下，如果提供者已停用，原則提供者可能不想強制執行其持續性原則。 加入提供者時，呼叫端可以指定選擇性的 Windows 服務名稱。 加入持續性物件時，呼叫端可以選擇性地指定「擁有」該物件的提供者。 在服務啟動時，只有當 BFE 未與提供者相關聯，或相關聯的提供者沒有 Windows 服務名稱，或相關聯的 Windows 服務設定為自動啟動時，才會將持續性物件新增至系統。

## <a name="object-associations"></a>物件關聯

某些物件具有其他物件的參考。 例如，篩選準則一律會參考圖層，並可參考標注和提供者內容。 物件無法參考可能存留期較短的物件。 因此，動態物件無法從不同的會話參考動態物件。 靜態物件無法參考動態物件。 持續性物件無法參考動態物件、靜態物件或其他提供者所擁有的持續性物件。

必須先刪除所有參考該物件的物件，才能刪除該物件。

## <a name="luids-and-guids"></a>Luid 和 Guid

所有使用者模式的 WFP API 物件 (FWPM) 是由全域唯一識別碼 (**guid**) ，並依 **guid** s 參考其他物件。 **GUID** 只需要在物件類型內是唯一的。 例如，篩選準則和提供者內容可以有相同的 **GUID**，但不能有兩個篩選準則。 加入新的物件時，呼叫端可以指派物件的 **GUID** ，或將它保持為零初始化，讓 BFE 指派 **GUID**。

所有核心模式的 WFP API 物件 (FWPS) 是由本機唯一識別碼 (**luid**) 所識別，並依其 LUID 參考其他物件。 從 **GUID** 切換至 **LUID** 可讓 WFP 節省非分頁的集區，並將執行時間處理優化。 **LUID** 的寬度取決於物件類型，以及從 **UINT16** 到 **UINT64** 的範圍。 **LUID** 一律會由 BFE 指派。

 

 