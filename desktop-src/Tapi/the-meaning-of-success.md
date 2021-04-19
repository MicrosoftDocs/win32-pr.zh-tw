---
description: 當者傳回成功時，函式已成功地往上以函式為基礎的 API 所定義的點。
ms.assetid: e4077d77-dee1-4f1a-a6ee-20ca2f92a1ec
title: SUCCESS 的意義
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d183695e9dce9df88dea5fe9464f16163130cd0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978257"
---
# <a name="the-meaning-of-success"></a>SUCCESS 的意義

## <a name="tapi-2x"></a>TAPI 2。x

當作業傳回成功指示時 (同步作業的函式傳回時，或非同步地透過 [**行 \_ 回復**](./line-reply.md) 或 [**電話 \_ 回復**](./phone-reply.md) 訊息進行非同步作業) ，則會假設下列條件成立：

-   函式已成功地以函式為基礎，逐步執行 API 所定義的點。 到達該點之後，表示作業已完成，或處於狀態，讓獨立的狀態訊息會通知應用程式有關後續進度。

    例如，服務提供者的 [**lineMakeCall**](/windows/win32/api/tapi/nf-tapi-linemakecall) 執行不會在此呼叫進入繼續通話狀態時傳回成功。 在理想的情況下，提供者應該儘快指出成功，例如，當通話進入撥號音通話狀態時 (是否適用) 。 一旦成功返回應用程式，LINE \_ CALLSTATE 訊息會通知應用程式呼叫的進度。 延遲傳回 **lineMakeCall** 成功指示的服務提供者（例如，在撥接完成之前），必須注意這會造成該提供者的缺點，因為應用層級的可用性可能會受到嚴格限制。 例如，在撥號完成且所有數位都傳送至交換器之後，使用者將無法取消通話設定要求進行中。

-   傳回信息 (的函式（例如) [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) ）只有在要求的資訊可供應用程式使用時，才會傳回成功。 如果函式傳回 (行或呼叫) 的控制碼，則只有在控制碼有效之後，才能傳回 SUCCESS。 在造成建立的函式成功指示之前，不應該傳送有關該行或呼叫的訊息。 服務提供者負責隱藏這類訊息。
-   啟用特定永久性條件 (例如 [**lineMonitorDigits**](/windows/win32/api/tapi/nf-tapi-linemonitordigits)) 的函式只會在啟用條件之後傳回成功，而不是在條件再次移除時 (例如，當所有數位監視都已完成) 時，不會傳回成功。
-   呼叫控制函式 (例如 [**lineHold**](/windows/win32/api/tapi/nf-tapi-linehold) 或 [**lineSetupTransfer**](/windows/win32/api/tapi/nf-tapi-linesetuptransfer)，但不是 [**lineMakeCall**](/windows/win32/api/tapi/nf-tapi-linemakecall)) 在作業完成時傳回成功。 某些電話網絡不會提供通知 (正面或負面) 有關服務提供者提出的特定要求是否完成。 在這種情況下，服務提供者必須在要求成功或失敗時決定。 因此，「成功」可能表示服務提供者已起始動作來滿足要求，但不一定需要其他任何動作。 例如，提供者可能不會收到來自交換器之要求的肯定通知，雖然它已將成功訊息傳送至應用程式。

## <a name="tapi-3x"></a>TAPI 3。x

當作業傳回成功指示時 (同步作業的函式傳回時，或使用非同步作業的非同步完成回呼程式 [**非同步 \_ 完成**](/windows/win32/api/tspi/nc-tspi-async_completion) 回檔程式非同步作業) ，則會假設下列條件成立：

-   函式已成功完成至服務提供者定義的點。 服務提供者會以函式為基礎來定義點。 到達該點之後，表示作業已完成，或處於狀態，因此後續的獨立狀態訊息會通知應用程式進度。
-   傳回信息 (例如 [**TSPI \_ LinePark**](/windows/win32/api/tspi/nf-tspi-tspi_linepark) 或 [**TSPI) \_ lineDevSpecific**](/windows/win32/api/tspi/nf-tspi-tspi_linedevspecific) 的函式，只有在要求的資訊可供呼叫端使用時，才會傳回成功。 傳回控制碼 (至開啟的行、開啟的電話或呼叫的函式，) 在函式傳回時立即傳回控制碼。 服務提供者和呼叫端都必須將控制碼視為「尚未生效」，直到最終成功指示為止。 服務提供者負責防止任何回呼訊息 [**LINEEVENT**](/windows/win32/api/tspi/nc-tspi-lineevent) 或 [**PHONEEVENT**](/windows/desktop/api/tspi/nc-tspi-phoneevent) 程式相關的開啟行、開啟的電話，或在成功指示之後進行呼叫。 如果最終結果為錯誤，則任何立即傳回的控制碼都會變成無效，而不會採取任何進一步的動作。
-   啟用特定永久性條件的函式 (例如 [**TSPI \_ lineMonitorDigits**](/windows/win32/api/tspi/nf-tspi-tspi_linemonitordigits)) 只會在啟用條件之後傳回成功，而不是在條件再次移除時 (例如，當數位監視完成) 時，不會傳回成功。
-   呼叫控制函式 (例如 [**TSPI \_ LineHold**](/windows/win32/api/tspi/nf-tspi-tspi_linehold) 和 [**TSPI \_ lineSetupTransfer**](/windows/win32/api/tspi/nf-tspi-tspi_linesetuptransfer)，但無法 [**TSPI \_ lineMakeCall**](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall)) 在作業完成時傳回成功。 在不提供這些函式之正面通知的電話語音環境中，服務提供者會強制對函式成功或失敗做出最佳決策。
-   服務提供者的 [**TSPI \_ lineMakeCall**](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall) 執行，必須晚于呼叫進入 *繼續* 通話狀態時才會傳回成功。 在理想的情況下，提供者會儘快指出成功，例如，當呼叫進入 *撥號* 程式通話狀態時 (如適用) 。 當成功傳回到應用程式時， [**LINE \_ CALLSTATE**](/previous-versions/windows/desktop/legacy/ms725219(v=vs.85)) 訊息會通知呼叫端有關呼叫的進度。 延遲傳回 **TSPI \_ lineMakeCall** 成功指示的服務提供者（例如，在撥接完成之前）會嚴重限制應用層級的彈性。 在 **TSPI \_ lineMakeCall** 中傳回成功的延遲會防止使用者取消進行中的通話設定要求，直到撥號完成，而且所有數位都會傳送至交換器。

 

 
