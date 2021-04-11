---
title: EAP 實行詳細資料
description: 存取點 (Ap) ，例如遠端存取服務 (RAS) 、使用必須由協力廠商 EAP DLL 匯出的函式呼叫來與 EAP 執行互動。
ms.assetid: 85775c03-7538-41a1-9f83-42e71025a79c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41115b16d843b0c1b087eac1c348a0491df1173a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314884"
---
# <a name="eap-implementation-details"></a><span data-ttu-id="b6d69-103">EAP 實行詳細資料</span><span class="sxs-lookup"><span data-stu-id="b6d69-103">EAP Implementation Details</span></span>

<span data-ttu-id="b6d69-104">存取點 (Ap) ，例如遠端存取服務 (RAS) 、使用必須由協力廠商 EAP DLL 匯出的函式呼叫來與 EAP 執行互動。</span><span class="sxs-lookup"><span data-stu-id="b6d69-104">Access Points (APs), such as Remote Access Service (RAS), interact with EAP implementations through the use of function calls that must be exported by the third-party EAP DLL.</span></span> <span data-ttu-id="b6d69-105">換句話說，EAP 是提供者 API，這表示外掛程式或 Dll 會將程式碼實作為 EAP 提供者，但不能自行呼叫 EAP Api。</span><span class="sxs-lookup"><span data-stu-id="b6d69-105">In other words, EAP is a provider API, meaning that plug-ins or DLLs implement code to become an EAP provider, but must not call the EAP APIs themselves.</span></span> <span data-ttu-id="b6d69-106">例如，EAP DLL 的程式設計人員會建立 EAP 初始化常式的程式碼，並將此程式碼放入 EAP 預先定義的函式 [**RasEapInitialize**](/previous-versions/windows/desktop/legacy/aa363527(v=vs.85))中。</span><span class="sxs-lookup"><span data-stu-id="b6d69-106">For example, a programmer of an EAP DLL creates code for an EAP initialization routine and places this code in the EAP predefined function [**RasEapInitialize**](/previous-versions/windows/desktop/legacy/aa363527(v=vs.85)).</span></span> <span data-ttu-id="b6d69-107">然後，在執行時間，AP 連接管理員會呼叫包含程式碼的 **RasEapInitialize** 函式，以初始化 EAP 執行。</span><span class="sxs-lookup"><span data-stu-id="b6d69-107">Then at run-time, the AP connection manager calls the **RasEapInitialize** function, which contains the code, to initialize the EAP implementation.</span></span>

<span data-ttu-id="b6d69-108">下列主題將詳細說明此互動：</span><span class="sxs-lookup"><span data-stu-id="b6d69-108">The following topics detail this interaction:</span></span>

-   [<span data-ttu-id="b6d69-109">EAP 的存取點初始化</span><span class="sxs-lookup"><span data-stu-id="b6d69-109">Access Point Initialization of EAP</span></span>](ras-initialization-of-eap.md)
-   [<span data-ttu-id="b6d69-110">驗證通訊協定初始化</span><span class="sxs-lookup"><span data-stu-id="b6d69-110">Authentication Protocol Initialization</span></span>](authentication-protocol-initialization.md)
-   [<span data-ttu-id="b6d69-111">存取點和驗證通訊協定互動</span><span class="sxs-lookup"><span data-stu-id="b6d69-111">Access Point and Authentication Protocol Interaction</span></span>](ras-and-authentication-protocol-interaction-during-authentication.md)
-   [<span data-ttu-id="b6d69-112">完成驗證會話</span><span class="sxs-lookup"><span data-stu-id="b6d69-112">Completion of the Authentication Session</span></span>](completion-of-the-authentication-session.md)

 

 