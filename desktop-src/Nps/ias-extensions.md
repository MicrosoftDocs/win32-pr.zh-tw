---
title: 網路原則伺服器擴充功能
description: NPS 擴充功能 API 可讓軟體發展人員撰寫可用於驗證、授權和帳戶處理的擴充 Dll。 NPS 擴充功能 API 支援遠端驗證撥入消費者服務 (RADIUS) 通訊協定。
ms.assetid: f459025f-fe5e-4ffa-a651-c70a4f8234ae
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddd6f9bd0be7479726110b41d6060a7e5c836bb8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933466"
---
# <a name="network-policy-server-extensions"></a><span data-ttu-id="11356-104">網路原則伺服器擴充功能</span><span class="sxs-lookup"><span data-stu-id="11356-104">Network Policy Server Extensions</span></span>

> [!Note]  
> <span data-ttu-id="11356-105">從 Windows Server 2008 開始， (IAS) 的網際網路驗證服務已重新命名為網路原則伺服器 (NPS) 。</span><span class="sxs-lookup"><span data-stu-id="11356-105">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.</span></span> <span data-ttu-id="11356-106">本主題的內容適用于 IAS 和 NPS。</span><span class="sxs-lookup"><span data-stu-id="11356-106">The content of this topic applies to both IAS and NPS.</span></span> <span data-ttu-id="11356-107">在整個文字中，NPS 是用來參考服務的所有版本，包括原本稱為 IAS 的版本。</span><span class="sxs-lookup"><span data-stu-id="11356-107">Throughout the text, NPS is used to refer to all versions of the service, including the versions originally referred to as IAS.</span></span>

 

<span data-ttu-id="11356-108">NPS 擴充功能 API 可讓軟體發展人員撰寫可用於驗證、授權和帳戶處理的擴充 Dll。</span><span class="sxs-lookup"><span data-stu-id="11356-108">The NPS Extensions API enables software developers to write extension DLLs that can be used for authentication, authorization, and accounting.</span></span> <span data-ttu-id="11356-109">NPS 擴充功能 API 支援遠端驗證撥入消費者服務 (RADIUS) 通訊協定。</span><span class="sxs-lookup"><span data-stu-id="11356-109">NPS Extensions API supports the Remote Authentication Dial-In User Service (RADIUS) protocol.</span></span>

<span data-ttu-id="11356-110">使用 NPS 擴充功能 API 所執行的延伸模組 Dll 可以提供增強的會話控制和帳戶處理。</span><span class="sxs-lookup"><span data-stu-id="11356-110">The extension DLLs implemented using the NPS Extensions API can provide enhanced session control and accounting.</span></span> <span data-ttu-id="11356-111">您可以使用這些 Dll 來控制使用者網路會話的數目、使用狀態伺服器，以及連接到網域驗證資料庫和 Active Directory 服務等案例。</span><span class="sxs-lookup"><span data-stu-id="11356-111">These DLLs can be used for scenarios such as controlling the number of end-user network sessions, using a state server, and connecting to domain authentication databases and Active Directory services.</span></span> <span data-ttu-id="11356-112">擴充 Dll 可以擴充 NPS 提供的遠端存取授權，方法是在將接受回應傳送回驗證用戶端時，新增自己的授權。</span><span class="sxs-lookup"><span data-stu-id="11356-112">The extension DLLs can expand the remote access authorizations provided by NPS by adding their own authorizations when sending an Accept response back to an authenticating client.</span></span>

<span data-ttu-id="11356-113">NPS 擴充功能 API 適用于任何運算環境，可改善透過遠端伺服器驗證撥入使用者的效率。</span><span class="sxs-lookup"><span data-stu-id="11356-113">NPS Extensions API is applicable in any computing environment where it would improve efficiency to authenticate dial-in users through a remote server.</span></span> <span data-ttu-id="11356-114">這項技術特別適合 (Isp) 的網際網路服務提供者。</span><span class="sxs-lookup"><span data-stu-id="11356-114">This technology is especially useful for Internet Service Providers (ISPs).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="11356-115">本節內容</span><span class="sxs-lookup"><span data-stu-id="11356-115">In This Section</span></span>

[<span data-ttu-id="11356-116">概觀</span><span class="sxs-lookup"><span data-stu-id="11356-116">Overview</span></span>](/windows/desktop/Nps/ias-about-internet-authentication-service)

<span data-ttu-id="11356-117">RADIUS 和 NPS 擴充功能 API 的一般資訊。</span><span class="sxs-lookup"><span data-stu-id="11356-117">General information about RADIUS and the NPS Extensions API.</span></span>

[<span data-ttu-id="11356-118">使用</span><span class="sxs-lookup"><span data-stu-id="11356-118">Using</span></span>](/windows/desktop/Nps/ias-using-internet-authentication-service)

<span data-ttu-id="11356-119">示範如何使用 NPS 擴充功能 API 的範例程式碼。</span><span class="sxs-lookup"><span data-stu-id="11356-119">Sample code that demonstrates how to use the NPS Extensions API.</span></span>

[<span data-ttu-id="11356-120">參考</span><span class="sxs-lookup"><span data-stu-id="11356-120">Reference</span></span>](/windows/desktop/Nps/ias-internet-authentication-service-reference)

<span data-ttu-id="11356-121">組成 NPS 擴充功能 API 的列舉類型、函式和結構的檔。</span><span class="sxs-lookup"><span data-stu-id="11356-121">Documentation of enumerated types, functions, and structures that compose the NPS Extensions API.</span></span>

## <a name="related-topics"></a><span data-ttu-id="11356-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="11356-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="11356-123">網路原則伺服器 (網際網路驗證服務) </span><span class="sxs-lookup"><span data-stu-id="11356-123">Network Policy Server (Internet Authentication Service)</span></span>](portal.md)
</dt> <dt>

[<span data-ttu-id="11356-124">可延伸的驗證通訊協定 (EAP)</span><span class="sxs-lookup"><span data-stu-id="11356-124">Extensible Authentication Protocol (EAP)</span></span>](../eap/eap-start-page.md)
</dt> </dl>

 

 