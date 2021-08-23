---
title: 關機和清除
description: 若要讓應用程式正常終止，它必須執行下列清除作業。
ms.assetid: fc07adb8-103c-42d8-8187-3f5ee083c6d8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a551ad57ddbf63c6ff598814794bc5837da646e98169d8250e543575abd013a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118950688"
---
# <a name="shutdown-and-cleanup"></a>關機和清除

若要讓應用程式正常終止，它必須執行下列清除作業：

-   藉由呼叫 [**HttpRemoveUrlFromUrlGroup**](/windows/desktop/api/Http/nf-http-httpremoveurlfromurlgroup) 函式來取消註冊先前在 [**HttpAddUrlToUrlGroup**](/windows/desktop/api/Http/nf-http-httpaddurltourlgroup)的呼叫中註冊的 URL，以移除 URL 群組中所有已註冊的 url。
-   藉由呼叫 [**HttpCloseUrlGroup**](/windows/desktop/api/Http/nf-http-httpcloseurlgroup) 函數來關閉 URL 群組。 在伺服器會話下建立的所有 URL 群組都必須在關閉伺服器會話之前關閉。
-   藉由呼叫 [**HttpCloseServerSession**](/windows/desktop/api/Http/nf-http-httpcloseserversession)來關閉伺服器會話。
-   藉由呼叫 [**HttpCloseRequestQueue**](/windows/desktop/api/Http/nf-http-httpcloserequestqueue)來關閉要求佇列的控制碼。
-   藉由呼叫 HttpTerminate 函式，針對應用程式最初對 [**HttpInitialize**](/windows/desktop/api/Http/nf-http-httpinitialize)所進行的每個呼叫，呼叫具有相符旗標設定的 [](/windows/desktop/api/Http/nf-http-httpterminate)函數，以終止 HTTP 伺服器 API 所建立的資源。 每個呼叫都會結束通話 [**HttpInitialize**](/windows/desktop/api/Http/nf-http-httpinitialize)時所建立的所有資源。

 

 




