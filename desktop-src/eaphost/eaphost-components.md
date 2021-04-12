---
title: EAPHost 的元件
description: 瞭解 EAPHost authentication 的三個元件。 使用 EAPHost authentication 來查看其他可用的資源。
ms.assetid: f875c3f8-d2fb-461e-b356-e1b2ccaf9981
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ede2fc6a705ec77fe982778239a92c7ffb10ef9
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104463717"
---
# <a name="components-of-eaphost"></a><span data-ttu-id="04cf3-104">EAPHost 的元件</span><span class="sxs-lookup"><span data-stu-id="04cf3-104">Components of EAPHost</span></span>

<span data-ttu-id="04cf3-105">本主題說明 EAPHost authentication 的三個元件。</span><span class="sxs-lookup"><span data-stu-id="04cf3-105">This topic describes the three components of EAPHost authentication.</span></span>

## <a name="eaphost-components"></a><span data-ttu-id="04cf3-106">EAPHost 元件</span><span class="sxs-lookup"><span data-stu-id="04cf3-106">EAPHost Components</span></span>

<span data-ttu-id="04cf3-107">EAPHost authentication 具有下列三個元件。</span><span class="sxs-lookup"><span data-stu-id="04cf3-107">EAPHost authentication has the following three components.</span></span>

-   <span data-ttu-id="04cf3-108">發出驗證要求的要求者。</span><span class="sxs-lookup"><span data-stu-id="04cf3-108">The supplicant, which makes the authentication requests.</span></span>
-   <span data-ttu-id="04cf3-109">對等 (或用戶端) EAP 方法，其會在用戶端上執行特定的 EAP 方法和管理驗證會話。</span><span class="sxs-lookup"><span data-stu-id="04cf3-109">The peer (or client) EAP methods, which implement the specific EAP methods and manage the authentication session on the client side.</span></span>
-   <span data-ttu-id="04cf3-110">驗證器 (或伺服器) EAP 方法，其可執行 EAP 通訊協定的伺服器端。</span><span class="sxs-lookup"><span data-stu-id="04cf3-110">The authenticator (or server) EAP methods, which implement the server side of the EAP protocol.</span></span>

<span data-ttu-id="04cf3-111">系統會直接從想要透過 EAPHost 驗證的應用程式呼叫要求者 Api。</span><span class="sxs-lookup"><span data-stu-id="04cf3-111">The supplicant APIs are called directly from an application that wants to authenticate via EAPHost.</span></span> <span data-ttu-id="04cf3-112">不過，對等方法和驗證器方法 Api 是必須針對特定 EAP 驗證方法類型（例如 Microsoft 挑戰交握驗證通訊協定2.0 版 (CHAPv2) ）所執行的函式原型。</span><span class="sxs-lookup"><span data-stu-id="04cf3-112">The peer method and authenticator method APIs, however, are function prototypes that must be implemented for a specific EAP authentication method type - such as the Microsoft Challenge Handshake Authentication Protocol version 2.0 (MS-CHAPv2).</span></span>

<span data-ttu-id="04cf3-113">如果您正在撰寫將使用 EAPHost 進行驗證的應用程式，請參閱 [EAPHost 要求者 API 參考](eap-host-supplicant-api-reference.md)。</span><span class="sxs-lookup"><span data-stu-id="04cf3-113">If you are authoring an application that will use EAPHost for authentication, please refer to the [EAPHost Supplicant API Reference](eap-host-supplicant-api-reference.md).</span></span>

<span data-ttu-id="04cf3-114">如果您要撰寫新的 EAP 驗證方法以由 EAPHost 管理，請參閱 [EAPHost 對等方法 Api 參考](eap-host-peer-method-api-reference.md) 和 [EAPHost 驗證器方法 api](eaphost-authenticator-method-apis.md)。</span><span class="sxs-lookup"><span data-stu-id="04cf3-114">If you are authoring a new EAP authentication method to be managed by EAPHost, please refer to the [EAPHost Peer Method API Reference](eap-host-peer-method-api-reference.md) and the [EAPHost Authenticator Method APIs](eaphost-authenticator-method-apis.md).</span></span> <span data-ttu-id="04cf3-115">請注意，您將會建立這些 Api 的實作為 EAPHost 載入之新 DLL 中公開的 Api，而不是直接呼叫它們。</span><span class="sxs-lookup"><span data-stu-id="04cf3-115">Note that you will be creating implementations of these APIs exposed in a new DLL that EAPHost loads, rather than calling them directly.</span></span>

 

 




