---
description: 電話語音是一項很重要的功能，稱為「輔助電話語音」。
ms.assetid: 1c41f52b-f8bf-410e-a966-9323a690a4d5
title: 輔助電話語音總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b6a8826fd0c273936204d9250fb91504333d807
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944605"
---
# <a name="assisted-telephony-overview"></a>輔助電話語音總覽

電話語音是一項很重要的功能，稱為「輔助電話語音」。 輔助電話語音是設計用來建立語音通話和媒體通話，以供任何應用程式使用，而不只是專用於電話功能。 換句話說，輔助電話語音可讓應用程式進行電話通話，而不需要知道完整電話語音 API 的服務詳細資料。 它會將電話語音擴充至文書處理應用程式、試算表、資料庫、個人資訊管理員和其他非電話語音應用程式。

如需基本電話語音的 TAPI 2.x 輔助電話語音功能清單，請參閱 [Tapi 快速功能參考](./tapi-quick-function-reference.md)。 TAPI 3.x 透過 [**ITRequest**](/windows/desktop/api/tapi3if/nn-tapi3if-itrequest) 介面支援輔助電話語音。

下列範例會說明協助電話語音的實用性。 試算表應用程式可以併入用來撥打語音電話電話號碼的函式。 只要應用程式不需要完整電話語音 API 所提供的詳細呼叫控制項，輔助電話語音就是提供電話功能的最簡單且最有效率的方式。

![使用試算表應用程式協助電話語音](images/assist4.png)

輔助電話語音和完整的電話語音 API 是使用並以不同的方式執行，因此不建議您在單一應用程式中混用輔助電話語音函數呼叫和電話語音 API 函數呼叫。

## <a name="using-assisted-telephony"></a>使用輔助電話語音

使用輔助電話語音服務的應用程式，只會起始由 TAPI 暫時排入佇列的呼叫要求。 要求收件者應用程式會抓取這些要求，並代表輔助電話語音應用程式執行這些要求。 [**TapiRequestMakeCall**](/windows/win32/api/tapi/nf-tapi-tapirequestmakecall)函式會要求語音通話的建立。 要求的應用程式不會控制呼叫。

TAPI 可讓使用者為每個服務建立不同或相同的要求收件者應用程式。 應用程式會藉由向 [**lineRegisterRequestRecipient**](/windows/win32/api/tapi/nf-tapi-lineregisterrequestrecipient)註冊來成為要求收件者，其中 **TRUE** 會指定為參數 *bEnable* 的值。  (指定 **FALSE** 取消註冊應用程式做為要求收件者，當它判定其收件者的職責是針對目前的會話時，就應該執行此動作。 ) 應用程式會在 **lineRegisterRequestRecipient** 的 *dwRequestMode* 參數中選取要處理的服務。 要求的可能值為 LINEREQUESTMODE \_ MAKECALL，以顯示應用程式將會處理 [**tapiRequestMakeCall**](/windows/win32/api/tapi/nf-tapi-tapirequestmakecall) 要求。 如果有多個應用程式註冊相同的服務，則會使用優先順序配置來允許使用者選取處理要求時慣用的應用程式。 此優先順序配置與用於呼叫移交的相同，以及根據登錄中 **HandoffPriorities** 中的檔案名清單來路由傳送來電的方式相同。

## <a name="call-requests"></a>呼叫要求

輔助電話語音提供具備電話語音功能的應用程式，可讓您在不需要開發人員完全 >serilog.sinks.literate 電話語音的情況下撥打電話。

[**TapiRequestMakeCall**](/windows/win32/api/tapi/nf-tapi-tapirequestmakecall)函式會要求使用者與其電話號碼所指定的遠端方之間進行語音通話。 系統會對 TAPI 發出要求，將它傳遞給註冊為這類要求收件者的應用程式。 此收件者是通話管理員應用程式。

在應用程式提出要求之後，就會從呼叫管理員應用程式完全控制呼叫，因為輔助電話語音應用程式無法管理呼叫。 由於電話語音和所有使用者介面作業的更複雜層面都是由「呼叫管理員」應用程式處理，因此，必須以任何實質方式修改啟用電話語音的應用程式。 事實上，允許從內建指令碼語言叫用這項作業的應用程式，可能完全不需要修改。

[**TapiGetLocationInfo**](/windows/win32/api/tapi/nf-tapi-tapigetlocationinfo)函式會將國家或地區碼和城市 (區域，傳回給應用程式，) 程式碼，使用者已在電話語音主控台的目前位置參數中設定。 應用程式可以使用這項資訊來協助使用者形成適當的標準電話號碼，例如，當輸入電話簿專案或資料庫記錄中的新數位時，提供這些電話號碼作為預設值。

## <a name="request-recipients"></a>要求收件者

需要有兩種應用程式才能執行輔助電話語音。 輔助電話語音 *用戶端* 是指使用「tapi」首碼的函式來使用「輔助電話語音」的應用程式。 這類用戶端應用程式的其中一個範例，就是要新增 **撥號** 功能表命令或工具列按鈕的試算表。

輔助電話語音 *伺服器* 是一種應用程式，可執行由另一個應用程式對「tapi」首碼函式的呼叫所產生的電話語音 API 函式。 為了使其成為輔助電話語音伺服器，這類應用程式會使用 [**lineRegisterRequestRecipient**](/windows/win32/api/tapi/nf-tapi-lineregisterrequestrecipient) 函式註冊為一部。

輔助電話語音 (的功能（開頭為「tapi」前置詞） ) 稱為「要求函式」（ *request 函數*）。 處理這些要求（輔助電話語音伺服器）的輔助電話語音應用程式稱為 *要求* 收件者。

## <a name="processing-assisted-telephony-requests"></a>處理輔助電話語音要求

傳遞和處理要求的程式如下所示：

1.  當 TAPI 收到輔助電話語音要求時，它會檢查要求收件者，也就是目前註冊來處理該要求類型的應用程式。 如果有要求收件者，則會將要求排入佇列，而且已針對該要求的服務註冊的最高優先順序應用程式會收到 [**一行 \_ 要求**](./line-request.md) 訊息。 此訊息會通知要求收件者有新的要求已抵達，並且會指出要求的模式。
2.  如果 TAPI 找不到目前正在執行的應用程式來處理這類要求，它會嘗試啟動已註冊為能夠執行此動作的應用程式。 此註冊資訊會記錄在登錄中的 **HandoffPriorities** 中。 TAPI 會嘗試依 **HandoffPriorities** 區段中列出的順序來啟動應用程式。  (請參閱下列步驟。 ) 

    如果目前沒有註冊任何應用程式，TAPI 會在 **HandoffPriorities** 中檢查相關聯專案上的要求處理應用程式清單。 如果檔案中缺少相關聯的行（如果沒有列出任何應用程式），或如果清單中沒有任何應用程式可以啟動，則會拒絕要求，並出現錯誤 TAPIERR \_ NOREQUESTRECIPIENT。

    當要求收件者啟動時 (是否已由 TAPI 啟動) 它會在啟動程式期間呼叫 [**lineRegisterRequestRecipient**](/windows/win32/api/tapi/nf-tapi-lineregisterrequestrecipient) ，並將自己註冊為要求收件者。

3.  如果專案中列出一或多個應用程式，則 TAPI 會從第一個列出的應用程式開始， (最高優先順序) ，然後使用 [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) 函式嘗試啟動它。 如果嘗試啟動應用程式失敗，TAPI 會嘗試啟動清單中的下一個應用程式。 當任何應用程式成功啟動時，TAPI 只會將要求排入佇列，並將成功指示傳回給應用程式，即使尚未將要求告知要求收件者也一樣。

    當要求收件者應用程式啟動之後，它會呼叫 [**lineRegisterRequestRecipient**](/windows/win32/api/tapi/nf-tapi-lineregisterrequestrecipient)，這會導致傳送 [**線路 \_ 要求**](./line-request.md) 訊息，以通知要求已排入佇列。 如果基於某些原因而啟動的應用程式永遠不會註冊，則要求會一直排入佇列，並永遠留在佇列中，直到應用程式註冊該類型的要求為止。

4.  如果 TAPI 發現這類已註冊的應用程式已在執行中或成功啟動，它會將要求排入佇列，並將要求 \_ 訊息傳送至伺服器應用程式，並將函式呼叫的成功指示傳回給輔助電話語音應用程式。 此成功訊息指出要求已被接受並排入佇列，而不是已成功執行。

當伺服器應用程式準備好處理要求時，它會呼叫 [**lineGetRequest**](/windows/win32/api/tapi/nf-tapi-linegetrequest) 函數。 這可讓它收到所需的任何資訊，例如要撥打的位址。 然後，它會使用 TAPI 函式 (（例如 [**lineMakeCall**](/windows/win32/api/tapi/nf-tapi-linemakecall) 和) [**lineDrop**](/windows/win32/api/tapi/nf-tapi-linedrop) ）來處理要求，否則會使用這些功能來放置呼叫。 叫用 **lineGetRequest** 會從 TAPI 移除要求，並將要求參數複製到應用程式佈建的要求緩衝區中。 緩衝區內容的大小和轉譯取決於要求模式。

伺服器必須確保在執行要求時使用正確的參數。 當您這樣做時，會遵循下列步驟：

1.  要求收件者會先收到 [**一行 \_ 要求**](./line-request.md) 訊息，告知要求佇列中的要求可以存在。 這會告知應用程式呼叫 [**lineGetRequest**](/windows/win32/api/tapi/nf-tapi-linegetrequest) ，並持續呼叫它，直到佇列已清空 (如果要求是用來進行新的呼叫) ，或卸載現有的呼叫。 此訊息不會包含要求的參數，但會要求卸載現有的呼叫。
2.  如果要求要進行新的呼叫，輔助電話語音伺服器會使用 [**lineGetRequest**](/windows/win32/api/tapi/nf-tapi-linegetrequest) 函式來取得完整的要求，其中包含要求的參數。 伺服器現在擁有所需的所有資訊，例如要撥打的電話號碼或要求的製造商識別。 但是，伺服器必須先配置儲存此資訊所需的記憶體。
3.  最後，伺服器會叫用適當的 TAPI 函數或一組函數來執行要求。

如果 TAPI 無法啟動能夠作為要求收件者的應用程式，則輔助電話語音通話會失敗，並傳回錯誤 TAPIERR \_ NOREQUESTRECIPIENT。

## <a name="notes-on-request-recipient-operations"></a>要求收件者作業的注意事項

下列資訊會考慮處理電話語音要求的系統：

-   預設登錄應該會在 [**tapiRequestMakeCall**](/windows/win32/api/tapi/nf-tapi-tapirequestmakecall)的優先順序清單中列出呼叫管理員應用程式。 它很有説明，但不是必要的，因為呼叫管理員應用程式有一個功能表選項，可讓使用者將其設定為最高優先順序。
-   當 TAPI 自動啟動輔助電話語音收件者應用程式，且該應用程式是系統中唯一的 TAPI 應用程式時，此動作會初始化 TAPI。 如果輔助電話語音收件者應用程式在註冊輔助電話語音要求之前初始化並關閉線路裝置，則 TAPI 也會關閉，而且會遺失輔助電話語音要求。 當另一個啟動的 TAPI 應用程式執行初始化和關閉時，也可能會遺失輔助電話語音要求。

 

 
