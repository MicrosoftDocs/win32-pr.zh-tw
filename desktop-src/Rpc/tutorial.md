---
title: 教學課程
description: 本教學課程會引導您完成從現有的獨立應用程式建立簡單、單一用戶端單一伺服器分散式應用程式所需的步驟。
ms.assetid: afdfa037-58c0-4dcf-aa27-6839db0515e6
keywords:
- 遠端程序呼叫 RPC，教學課程
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7c19b0d8ec3b3eb55cf29ccfd87eca43775c2ea
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021813"
---
# <a name="tutorial"></a>教學課程

本教學課程會引導您完成從現有的獨立應用程式建立簡單、單一用戶端單一伺服器分散式應用程式所需的步驟。 這些步驟包括：

-   建立介面定義和應用程式佈建檔。
-   使用 MIDL 編譯器，從這些檔案產生 C 語言用戶端和伺服器 stub 和標頭。
-   撰寫用戶端應用程式，以管理其與伺服器的連接。
-   撰寫包含實際遠端程式的伺服器應用程式。
-   將這些檔案編譯並連結至 RPC 執行時間程式庫，以產生分散式應用程式。

用戶端應用程式會在遠端程序呼叫中，將字元字串傳遞給伺服器，而伺服器會將字串 "Hello，World" 列印到其標準輸出。

這個範例應用程式的完整原始程式檔，以及用來處理命令列輸入的額外程式碼，以及將各種狀態訊息輸出到使用者的程式，都位於 \\ 平臺軟體發展工具組 (SDK) 的 RPC Hello 目錄中。

本節提供下列主題的討論：

-   [獨立應用程式](the-standalone-application.md)
-   [定義介面](defining-the-interface.md)
-   [產生 UUID](generating-the-uuid.md)
-   [IDL 檔案](the-idl-file.md)
-   [ACF 檔案](the-acf-file.md)
-   [產生存根檔案](generating-the-stub-files.md)
-   [用戶端應用程式](the-client-application.md)
-   [伺服器應用程式](the-server-application.md)
-   [停止伺服器應用程式](stopping-the-server-application.md)
-   [編譯和連結](compiling-and-linking.md)
-   [執行應用程式](running-the-application.md)

 

 




