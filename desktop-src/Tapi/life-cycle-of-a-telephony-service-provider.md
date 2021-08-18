---
description: 本主題提供 TSP 作業的高階評論。
ms.assetid: 8ee592ff-387e-449e-8e3f-4f6407166fe5
title: 電話語音服務提供者的生命週期
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6282f4e7b946ffb79bd6233688869616cc0b0259a1d491834452290474c552a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012694"
---
# <a name="life-cycle-of-a-telephony-service-provider"></a>電話語音服務提供者的生命週期

本主題提供 TSP 作業的高階評論。

會話是特定設定維持有效的時間，以及執行電話語音作業的時間。服務提供者可在第一次載入和最後釋出的時間之間支援許多會話。 針對每個會話，TAPI 會協調介面的版本、啟動會話、執行作業，最後關閉會話。 服務提供者不能將來自某個會話的資訊保留給下一個會話。

已知介面版本之後，TAPI 會呼叫 [**TSPI \_ providerInit**](/windows/win32/api/tspi/nf-tspi-tspi_providerinit) 函數來設定所有指令引數。 服務提供者可確保在呼叫 **TSPI \_ providerInit** 函式時，登錄中的所有設定資訊都是穩定的。 大部分的服務提供者會在該時間讀取所有設定資訊。

在服務提供者初始化之後，正常作業可以依照任何順序繼續進行。

TAPI 會以每個裝置為基礎來協調裝置特定資訊。 當裝置開啟時，TAPI 和服務提供者會認可至版本。

服務提供者可以接收選取和取消延伸模組版本的要求。 選取延伸模組版本時，裝置會根據該裝置特定的擴充功能版本，嚴格地操作。

裝置特定擴充功能版本的協商可能會在裝置開啟之前和之後發生多次。 TAPI 會傳遞版本範圍，而服務提供者會從這個範圍選取並傳回值。 一般來說，服務提供者已停用裝置特定的擴充功能。

這會認可 TAPI 和服務提供者，以在該擴充功能版本層級運作，直到取消選取為止。 在裝置專屬擴充功能生效的期間，嘗試協商延伸模組版本，應該只允許目前作用中的版本層級。 取消裝置特定的擴充功能之後，就可以協商和選取不同的版本。

下圖顯示「**開啟/關閉**」配對內的電話作業。 其中有些作業是同步的，有些則是非同步。 如果作業以非同步方式完成，則在第一次報告完成之前，可以要求另一個作業。 因此，作業可能會以任何方式重迭。 服務提供者最後必須針對任何要求的非同步作業回報完成。 關閉電話會強制完成未完成的非同步作業， (可能發生「失敗」指示) 。

線路裝置的生命週期與手機的生命週期類似，不同之處在于這些行會有自己的協商、初始化、開啟和關閉程式。 開啟的行作業會以自己的 **開啟/關閉** 配對來括住。 這組組合接著會在與電話 **開啟/關閉** 的相同 **初始化/關機** 配對之間加上括弧。

呼叫的生命週期會嚴格地在包含它們的行的 **開啟/關閉** 之間加上括弧。 呼叫的存留期可以透過數種方式開始：

-   透過 [**lineMakeCall**](/windows/win32/api/tapi/nf-tapi-linemakecall)、 [**lineSetupTransfer**](/windows/win32/api/tapi/nf-tapi-linesetuptransfer)或 [**lineSetupConference**](/windows/win32/api/tapi/nf-tapi-linesetupconference)等功能從 TAPI 要求。
-   自發地源自服務提供者，做為新的來電、在連接的電話聽筒上使用使用者起始的呼叫，或以其他作業的副作用（例如放置現有的來電）來產生的呼叫。

同一行內的相異呼叫存留期可以任何方式彼此重迭。 所有呼叫會在叫用 TSPI 函式 [**TSPI \_ lineCloseCall**](/windows/win32/api/tspi/nf-tspi-tspi_lineclosecall) 時，結束其存留期。 下圖顯示數個呼叫的生命週期。

![重迭呼叫的生命週期](images/modell.png)

通話可能源自于 TAPI，如 **MakeCall/CloseCall** 配對所示。 呼叫也可能源自服務提供者。 服務提供者會向 TAPI 提供的回呼程式發出 [**一行 \_ NEWCALL**](line-newcall.md) 訊息。 在這種情況下，TAPI 會傳回其呼叫的識別碼，此識別碼包含在呼叫上發生的後續回呼報告事件中。 如果是存留期源自 TAPI 的呼叫，此識別碼會包含在建立呼叫的 TSPI 作業中。

所有開始通話存留期的作業都會導致 TAPI 和服務提供者交換新呼叫的識別碼。 在 TAPI 發出呼叫的情況下，TAPI 會傳遞其識別碼，並接收服務提供者的識別碼做為傳回參數。 在呼叫源自服務提供者的情況下，服務提供者會將它的識別碼傳遞給 TAPI，並接收 TAPI 識別碼作為傳回參數。

下圖提供服務提供者安裝、設定和移除的高度高階觀點;橫跨許多會話的生命週期序列。 這些作業的一般生命週期可以顯示下列時間表。

![服務提供者安裝、設定和移除](images/model2.png)

會顯示一般的安裝和移除生命週期，橫跨多個會話。 對 **安裝** 和 [**移除**](/windows/win32/api/tapi3if/nf-tapi3if-itcollection2-remove) 程式的呼叫會嚴格配對，且不會重迭。 對設定程式 **的呼叫可能會在這** 組內多次發生。 服務提供者通常會使用這種方式，做為 **安裝** 程式的內部副作用，以建立線路和電話專案。 設定程式可能會在其他時間 **呼叫，以改變現有的安裝** 程式。 必須先完成 **安裝** 程式，才能允許任何其他 TSPI 函數。 在理想的情況下，所有的會話都會嚴格地嵌套在 **安裝/移除** 程式配對內。

[**TSPI \_ providerInstall**](/windows/win32/api/tspi/nf-tspi-tspi_providerinstall)、 [**TSPI \_ providerConfig**](/windows/win32/api/tspi/nf-tspi-tspi_providerconfig)和 [**TSPI \_ providerRemove**](/windows/win32/api/tspi/nf-tspi-tspi_providerremove)的函式會與服務提供者本身互動，而不是與任何特定裝置互動。 它們會影響跨多個會話繼續生存的靜態設定資訊，而且必須要有其他作業才能繼續。 因此，所有其他作業都是在 **TSPI \_ providerInstall** 的調用和其相符的 **TSPI \_ providerRemove** 完成之間進行嵌套。 這兩項作業通常會在不同的服務提供者負載或不同的機器開機情況下發生。 外部呼叫 **設定函數是選擇性的，** 因為 **安裝** 程式除了本身之外，還需要包含 **設定行為。** 從外部呼叫它的一般原因是要修改現有的設定。

奧妙內嵌在 [**TSPI \_ providerRemove**](/windows/win32/api/tspi/nf-tspi-tspi_providerremove) 作業完成的概念中。 您可以允許使用者執行電話語音服務所提供的電話語音主控台公用程式來改變服務提供者設定，即使正在進行) 中的電話語音 (作業也是如此。 因此， [**TSPI \_ ProviderConfig**](/windows/win32/api/tspi/nf-tspi-tspi_providerconfig) 和 **TSPI \_ providerRemove** 規格都允許在有未處理的會話時進行調用。 不過，對設定所做的任何變更都需要延遲，直到重新開機並重新啟動電話語音作業為止。 因此，嚴格來說， **TSPI \_ ProviderConfig** 或 **TSPI \_ providerRemove** 作業的完成會在任何會話之外進行。 動作的嵌套如下圖所示，即使程式呼叫可能會以稍有不同的順序出現。 當作業正在進行時，服務提供者允許服務提供者 **只允許設定或**[**移除**](/windows/win32/api/tapi3if/nf-tapi3if-itcollection2-remove)，雖然使用者應該會收到對話方塊的通知。 更方便使用的執行，可讓您最好使用至少一部分的作業。

這些 **安裝**、設定和 [**移除**](/windows/win32/api/tapi3if/nf-tapi3if-itcollection2-remove)作業都有對任何 **執行中的** 電話語音應用程式發出信號的副作用，最後導致它們關閉電話語音服務的使用。 這會同時結束服務提供者的所有未完成會話。 這表示服務提供者必須在新的會話開始時，讀取新的登錄設定。 當作業正在進行時，因設定或 [**移除**](/windows/win32/api/tapi3if/nf-tapi3if-itcollection2-remove)而暫 **止的任何** 變更，則會生效。

 

 
