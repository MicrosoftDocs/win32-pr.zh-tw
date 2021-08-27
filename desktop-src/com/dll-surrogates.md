---
title: DLL 代理
description: DLL 代理
ms.assetid: fe30c0ae-1d19-4a5f-8ee3-8a5337c79c44
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 808efe4a431a703282a705000d2fe18f6b4cfcde121d95c39fe65541b0260503
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119993248"
---
# <a name="dll-surrogates"></a>DLL 代理

COM 可讓您建立可載入至代理 EXE 進程的 DLL 伺服器。 這結合了撰寫 DLL 伺服器的便利性與可執行檔的優點。 Microsoft Visual Studio 等開發工具有助於撰寫 dll 伺服器，但是 dll 伺服器本身也有限制。 在代理程式中執行 DLL 伺服器可提供數個可能的優點：

-   錯誤隔離和同時服務多個用戶端的能力。
-   在分散式環境中，可以使用 DLL 伺服器執行來服務遠端用戶端。
-   它可以允許用戶端保護自己免于受信任的伺服器程式碼，同時讓他們能夠存取 DLL 伺服器所提供的服務。
-   在代理中執行 DLL 伺服器會提供具有代理程式安全性的 DLL。

COM 提供預設的代理程式，或者如果您有特殊需求，則可以撰寫自訂的代理。

下列主題提供 DLL 代理連結的詳細資訊：

-   [DLL 伺服器需求](dll-server-requirements.md)
-   [使用 System-Supplied 代理](using-the-system-supplied-surrogate.md)
-   [撰寫自訂代理](writing-a-custom-surrogate.md)

 

 




