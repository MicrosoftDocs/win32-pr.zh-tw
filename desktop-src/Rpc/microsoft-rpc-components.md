---
title: RPC 元件
description: 遠端程序呼叫 (RPC) 元件。
ms.assetid: 7caaf01a-7f20-470f-afcf-478146cae5eb
keywords:
- 遠端程序呼叫 RPC、描述的元件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44b3416589eccf865b70d3da82fa7494631ab7592f172bb46c10eccb1d96fad1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118928117"
---
# <a name="rpc-components"></a>RPC 元件

RPC 包含下列主要元件：

-   MIDL 編譯器
-   執行時間程式庫和標頭檔
-   名稱服務提供者 (有時稱為定位器) 
-   端點對應程式 (有時稱為埠對應程式) 

在 RPC 模型中，您可以使用針對此用途設計的語言，正式指定遠端程式的介面。 這種語言稱為介面定義語言或 IDL。 這種語言的 Microsoft 執行稱為「Microsoft 介面定義語言」或「MIDL」。

建立介面之後，您必須透過 MIDL 編譯器來傳遞它。 此編譯器會產生可將本機程序呼叫轉譯為遠端程序呼叫的存根。 存根是可對執行時間程式庫函式進行呼叫的預留位置函式，該函式會管理遠端程序呼叫。 這種方法的優點是，網路對您的分散式應用程式幾乎是完全透明的。 您的用戶端程式會呼叫看似本機程式的內容;將其轉換為遠端呼叫的工作會自動完成。 所有轉譯資料、存取網路和取得結果的程式碼，會由 MIDL 編譯器為您產生，而您的應用程式不會看到這些結果。

 

 




