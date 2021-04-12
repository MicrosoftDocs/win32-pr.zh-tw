---
title: 啟用安全性
description: 啟用安全性
ms.assetid: 0c13d473-a9f9-40b5-951b-731eab736fe6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e5b01b918666e911d96ed16528ba5045103f445
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104463789"
---
# <a name="activation-security"></a><span data-ttu-id="55b52-103">啟用安全性</span><span class="sxs-lookup"><span data-stu-id="55b52-103">Activation Security</span></span>

<span data-ttu-id="55b52-104">啟用安全性 (也稱為啟動安全性) 有助於控制可以啟動伺服器的人員。</span><span class="sxs-lookup"><span data-stu-id="55b52-104">Activation security (also called launch security) helps control who can launch a server.</span></span> <span data-ttu-id="55b52-105">「服務控制管理員」會自動套用「啟用安全性」 (特定電腦的 SCM) 。</span><span class="sxs-lookup"><span data-stu-id="55b52-105">Activation security is automatically applied by the service control manager (SCM) of a particular computer.</span></span> <span data-ttu-id="55b52-106">當收到來自用戶端的要求以啟始物件 (如 [實例建立](instance-creation-helper-functions.md) 協助程式函式中所述) ，SCM 會根據儲存在其登錄中的啟用安全性資訊來檢查要求。</span><span class="sxs-lookup"><span data-stu-id="55b52-106">Upon receipt of a request from a client to activate an object (as described in [Instance Creation Helper Functions](instance-creation-helper-functions.md)), the SCM checks the request against activation-security information stored within its registry.</span></span> <span data-ttu-id="55b52-107">也會檢查是否有相同電腦啟用 (啟用安全性。 ) </span><span class="sxs-lookup"><span data-stu-id="55b52-107">(Activation security is also checked for same-computer activations.)</span></span>

<span data-ttu-id="55b52-108">判斷用戶端的身分識別時，啟用會檢查用戶端呼叫 [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)時所設定的遮蓋旗標。</span><span class="sxs-lookup"><span data-stu-id="55b52-108">When determining the identity of the client, activation examines the cloaking flag set in the client's call to [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span> <span data-ttu-id="55b52-109">如果 (針對動態或靜態的掩蓋) 設定了遮蓋旗標，則會使用執行緒權杖（如果有的話）來判斷用戶端的身分識別。</span><span class="sxs-lookup"><span data-stu-id="55b52-109">If the cloaking flag is set (for either dynamic or static cloaking), the thread token is used, if present, to determine the identity of the client.</span></span> <span data-ttu-id="55b52-110">如果未設定任何掩蓋，則會使用進程權杖，而不是執行緒 token。</span><span class="sxs-lookup"><span data-stu-id="55b52-110">If no cloaking is set, the process token is used instead of the thread token.</span></span>

<span data-ttu-id="55b52-111">如需啟用安全性的詳細資訊，請參閱 [**COAUTHINFO**](/windows/desktop/api/wtypesbase/ns-wtypesbase-coauthinfo) 和 [**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo)。</span><span class="sxs-lookup"><span data-stu-id="55b52-111">For more information about activation security, see [**COAUTHINFO**](/windows/desktop/api/wtypesbase/ns-wtypesbase-coauthinfo) and [**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo).</span></span>

## <a name="related-topics"></a><span data-ttu-id="55b52-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="55b52-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="55b52-113">COM 中的安全性</span><span class="sxs-lookup"><span data-stu-id="55b52-113">Security in COM</span></span>](security-in-com.md)
</dt> </dl>

 

 