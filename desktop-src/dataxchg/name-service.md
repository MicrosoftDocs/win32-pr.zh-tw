---
title: 名稱服務
description: 本主題討論動態資料交換管理程式庫如何讓伺服器應用程式註冊其支援的服務名稱。
ms.assetid: 4b7e7f43-18aa-4c2e-aa2b-5ce7bb18048f
keywords:
- 'Windows消費者介面，動態資料交換 (DDE) '
- 動態資料交換 (的 DDE) ，名稱服務
- DDE (動態資料交換) ，名稱服務
- '資料交換、動態資料交換 (DDE) '
- 'Windows消費者介面，動態資料交換管理程式庫 (DDEML) '
- 動態資料交換管理程式庫 (DDEML) ，名稱服務
- DDEML (動態資料交換管理程式庫) ，名稱服務
- '資料交換、動態資料交換管理程式庫 (DDEML) '
- 動態資料交換 (的 DDE) ，服務名稱註冊
- DDE (動態資料交換) ，服務名稱註冊
- 動態資料交換管理程式庫 (DDEML) ，服務名稱註冊
- DDEML (動態資料交換管理程式庫) ，服務名稱註冊
- 動態資料交換 (的 DDE) ，服務名稱篩選
- DDE (動態資料交換) ，服務名稱篩選
- 動態資料交換管理程式庫 (DDEML) ，服務名稱篩選
- DDEML (動態資料交換管理程式庫) ，服務名稱篩選
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7346bd98979e9bd5a4aa0e43493e975d802875cf8fd0fc79d7bd002bcd0c5494
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118811645"
---
# <a name="name-service"></a>名稱服務

動態資料交換管理程式庫 (DDEML) 讓伺服器應用程式能夠註冊它所支援的服務名稱，以及防止 DDEML 將不支援之服務名稱的 [**XTYP \_ CONNECT**](xtyp-connect.md)交易傳送到伺服器動態資料交換 (的) 回呼函數。

下列主題描述名稱服務。

-   [服務名稱註冊](#service-name-registration)
-   [服務名稱篩選](#service-name-filter)

## <a name="service-name-registration"></a>服務名稱註冊

藉由向 DDEML 註冊其服務名稱，伺服器會通知系統中有新伺服器可用的其他 DDE 應用程式。 伺服器會藉由呼叫 [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) 函數並指定可識別名稱的字串控制碼，來註冊服務名稱。 在回應中，DDEML 會將 [**XTYP \_**](xtyp-register.md)暫存器交易傳送到系統 (中每個 DDEML 應用程式的回呼函式，除了在 DdeInitialize 函式中指定 CBF \_ SKIP \_ 註冊篩選旗標的) 。 [](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) **XTYP \_ REGISTER** 交易會將兩個字串控制碼傳遞給回呼函式：第一個會識別指定基底服務名稱的字串，而第二個則會識別指定實例特定服務的字串。 用戶端通常會使用可用伺服器清單中的基本服務名稱，讓使用者可以從清單中選取伺服器。 如果有多個實例正在執行，則用戶端會使用實例特定服務名稱來建立與伺服器應用程式之特定實例的交談。

伺服器可以使用 [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) 來取消註冊服務名稱。 此函式會讓 DDEML 將 [**XTYP \_ 取消註冊**](xtyp-unregister.md) 交易傳送到系統中的其他 DDE 應用程式，通知他們無法再使用該名稱來建立交談。

在呼叫 [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)之後，伺服器必須呼叫 [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice)來立即註冊其服務名稱。 伺服器必須在呼叫 [**DdeUninitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeuninitialize)函式之前，先使用 **DdeNameService** 取消註冊其服務名稱。

## <a name="service-name-filter"></a>服務名稱篩選

除了註冊服務名稱之外， [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) 還可讓伺服器開啟或關閉其服務名稱篩選。 當伺服器關閉其服務名稱篩選時，DDEML 會在任何用戶端呼叫 [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect)函式時，不論函式中指定的服務名稱為何，都會將 [**XTYP \_ CONNECT**](xtyp-connect.md)交易傳送到伺服器的 DDE 回呼函式。 當伺服器開啟其服務名稱篩選時，DDEML 只會在 **DdeConnect** 指定伺服器在 **DdeNameService** 呼叫中指定的服務名稱時，才會將 **XTYP \_ CONNECT** 交易傳送至伺服器。

根據預設，當應用程式呼叫 [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)時，服務名稱篩選為開啟。 此預設值可防止 DDEML 在伺服器建立字串處理所需的字串之前，將 [**XTYP \_ CONNECT**](xtyp-connect.md) 交易傳送到伺服器。 伺服器可以在呼叫 DdeNameService 時指定 DNS FILTEROFF 旗標，以關閉其服務名稱篩選 \_ 。 [](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) DNS \_ 篩選旗標會開啟篩選。

 

 




