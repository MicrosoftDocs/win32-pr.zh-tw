---
description: 網路提供者是一種 DLL，可讓 Windows 作業系統支援特定的網路通訊協定。
ms.assetid: 21dfa941-72fd-4f2c-8bc4-379ed6ca2a4c
title: 執行網路提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97819b033c57feb25cf882f97051785123e2e382
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112192"
---
# <a name="implementing-a-network-provider"></a>執行網路提供者

網路提供者是一種 DLL，可讓 Windows 作業系統支援特定的網路通訊協定。 它是藉由執行網路提供者 API 來完成。 此 API 是 [*多個提供者路由器*](../secgloss/m-gly.md) (MPR) 呼叫以與網路通訊的一組功能。 網路提供者接著會將這些呼叫轉譯成網路特定 API 呼叫，以執行 MPR 所指定的動作。 如此一來，Windows 作業系統就可以與新的網路通訊協定互動，而不需要瞭解其網路特定的 Api。

若要建立網路提供者，請撰寫可匯出 [**NPGetCaps**](/windows/desktop/api/Npapi/nf-npapi-npgetcaps) 函式的 DLL。

支援網路提供者 API 中的其他函式是選擇性的。 如果您的網路提供者不需要函式，則您的 DLL 不需要加以執行，也不需要提供存根的實作為。 如需詳細資訊，請參閱 [網路提供者](authentication-functions.md)函式中的個別函數主題。

例外狀況是，如果您支援下列其中一個列舉函數，您也必須支援其他兩個函式： [**NPOpenEnum**](/windows/desktop/api/Npapi/nf-npapi-npopenenum)、 [**NPEnumResource**](/windows/desktop/api/Npapi/nf-npapi-npenumresource)和 [**NPCloseEnum**](/windows/desktop/api/Npapi/nf-npapi-npcloseenum)。

下列指導方針說明如何撰寫可與 MPR 和 Windows 作業系統妥善互動的網路提供者。 可能的話，您的提供者應該遵循下列指導方針來進行速度、驗證和路由。

## <a name="speed"></a>速度

網路提供者應該能夠快速判斷網路資源是否為自己的資源。 這是因為 MPR 可能必須迴圈許多提供者來尋找資源的擁有者。

如果網路提供者未擁有資源，它應該會立即傳回 WN 錯誤的網路服務（不 \_ 正確） \_ 狀態碼。

支援 [**NPGetDirectoryType**](/windows/desktop/api/Npapi/nf-npapi-npgetdirectorytype) 的提供者也很重要，因為它是在 WinFile 正在繪製目錄樹狀結構時呼叫。

## <a name="validation"></a>驗證

驗證的順序很重要。 網路提供者應該先判斷其網路是否已啟動，然後判斷網路和網路提供者是否支援此作業。 如果在這些檢查之後，網路提供者會收到任何網路資源，就應該判斷它是否擁有它們。 最後，它應該驗證其他參數。

## <a name="routing"></a>路由

如果 MPR 必須迴圈處理網路提供者，它將會嘗試所有提供者，直到其中一個接受呼叫為止。 換句話說，MPR 一律會繼續嘗試尋找網路提供者。

但是，它會記下提供者所報告的第一個重大錯誤。 錯誤 \_ NETPATH 錯誤、錯誤 \_ \_ 網路名稱無效、錯誤不正確錯誤 \_ \_ \_ \_ \_ \_ 層級，因為它們只是表示提供者不管理資源。 但是，如果提供者失敗並出現錯誤的 \_ \_ 密碼無效或其他重大錯誤，MPR 會記錄此錯誤，並繼續進行網路提供者的迴圈。 一般來說，當路由傳送時，如果沒有任何提供者接受呼叫，MPR 就會報告在迴圈通過網路提供者時所遇到的第一個重大錯誤。

當您決定要傳回的錯誤訊息時，您的網路提供者應該會將此 MPR 的行為納入考慮。

## <a name="implementation-note"></a>執行附注

在執行網路提供者 DLL 時，提供者不能呼叫其他 [Windows 網路功能](../wnet/windows-networking-functions.md)、 [Shell api](../shell/samples-usingthumbnailproviders.md)，或其他以 UNC 路徑為基礎的查詢，這些查詢可能會導致 MPR 子系統的進入。 如果您從網路提供者 DLL 進行這類呼叫，則應用程式或其他作業系統元件可能會遇到爭用、效能不佳或 MPR 子系統內的鎖死。

 

 
