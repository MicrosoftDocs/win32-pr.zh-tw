---
description: 驗證層級的協商
ms.assetid: 31353d02-bfe2-48ac-81a1-0e38895a8a75
title: 驗證層級的協商
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38b9983bd2a2df1d85cc6df4bfc0ba2a757b200f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106997072"
---
# <a name="negotiation-of-authentication-level"></a><span data-ttu-id="f1168-103">驗證層級的協商</span><span class="sxs-lookup"><span data-stu-id="f1168-103">Negotiation of Authentication Level</span></span>

<span data-ttu-id="f1168-104">用戶端和伺服器都必須參與驗證，而且每個合作物件都表示它想要執行特定層級的驗證。</span><span class="sxs-lookup"><span data-stu-id="f1168-104">Both client and server must participate in authentication, and each party indicates that it wants to perform a certain level of authentication.</span></span> <span data-ttu-id="f1168-105">在呼叫開始時，會在兩個合作物件之間協商驗證層級、選擇適當的服務，並根據所) 選的驗證等級，進行驗證並繼續 (有可能的加密。</span><span class="sxs-lookup"><span data-stu-id="f1168-105">At the beginning of a call, the authentication level is negotiated between the two parties, an appropriate service is chosen, and the call is authenticated and proceeds (with possible encryption, depending on the authentication level chosen).</span></span> <span data-ttu-id="f1168-106">用戶端與伺服器之間協商的驗證層級會決定為最大 (*用戶端喜好* 設定，也就是 *伺服器喜好* 設定) 。</span><span class="sxs-lookup"><span data-stu-id="f1168-106">The authentication level negotiated between client and server is determined as Maximum(*Client preference*, *Server preference*).</span></span> <span data-ttu-id="f1168-107">這表示伺服器隨時都可以決定最適合的驗證層級;也就是說，您可以從伺服器以系統管理員的身份進行驗證。</span><span class="sxs-lookup"><span data-stu-id="f1168-107">The effect of this means that the server can always dictate a minimum level of authentication that it is comfortable with; that is, authentication can be administratively dictated from the server.</span></span>

<span data-ttu-id="f1168-108">用戶端會指定它想要在特定層級執行驗證，就像使用任何 COM 應用程式一樣。</span><span class="sxs-lookup"><span data-stu-id="f1168-108">The client specifies that it wants to perform authentication at a certain level as with any COM application.</span></span> <span data-ttu-id="f1168-109">用戶端驗證等級可以指定如下：</span><span class="sxs-lookup"><span data-stu-id="f1168-109">The client authentication level can be indicated as follows:</span></span>

-   <span data-ttu-id="f1168-110">每一部用戶端電腦，使用 [DCOMCNFG](/windows/desktop/com/setting-machine-wide-security-using-dcomcnfg) 或 [元件服務] 系統管理工具所設定的全電腦 COM 驗證等級。</span><span class="sxs-lookup"><span data-stu-id="f1168-110">Per client machine, with the machine-wide COM authentication level set by using either [DCOMCNFG](/windows/desktop/com/setting-machine-wide-security-using-dcomcnfg) or the Component Services administrative tool.</span></span>
-   <span data-ttu-id="f1168-111">根據用戶端應用程式，如果用戶端應該是 COM + 應用程式，則使用 [DCOMCNFG](/windows/desktop/com/setting-processwide-security-using-dcomcnfg) 或使用 [元件服務] 系統管理工具。</span><span class="sxs-lookup"><span data-stu-id="f1168-111">Per client application administratively, using [DCOMCNFG](/windows/desktop/com/setting-processwide-security-using-dcomcnfg) or using the Component Services administrative tool if the client should be a COM+ application.</span></span>
-   <span data-ttu-id="f1168-112">以程式設計方式，使用 [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)來處理每個用戶端。</span><span class="sxs-lookup"><span data-stu-id="f1168-112">Per client process programmatically, with [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span>
-   <span data-ttu-id="f1168-113">在任何時間點以程式設計的方式使用 [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket)。</span><span class="sxs-lookup"><span data-stu-id="f1168-113">At any point programmatically, using [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span></span>

<span data-ttu-id="f1168-114">COM + 伺服器應用程式會使用 [元件服務] 系統管理工具 (或透過管理腳本) ，以系統管理員的方式指定驗證層級。</span><span class="sxs-lookup"><span data-stu-id="f1168-114">The COM+ server application specifies an authentication level administratively by using the Component Services administrative tool (or through an administrative script).</span></span>

<span data-ttu-id="f1168-115">協商呼叫的驗證會依照下列順序進行：</span><span class="sxs-lookup"><span data-stu-id="f1168-115">Negotiating authentication for a call proceeds in the following sequence:</span></span>

1.  <span data-ttu-id="f1168-116"> (*用戶端*、 *伺服器*) 的最大值選擇驗證等級。</span><span class="sxs-lookup"><span data-stu-id="f1168-116">Authentication level is chosen as MAX(*client*, *server*).</span></span>
2.  <span data-ttu-id="f1168-117">驗證通訊協定的協商。</span><span class="sxs-lookup"><span data-stu-id="f1168-117">Negotiation of authentication protocol.</span></span>
3.  <span data-ttu-id="f1168-118">伺服器會驗證用戶端身分識別。</span><span class="sxs-lookup"><span data-stu-id="f1168-118">Server authenticates client identity.</span></span>
4.  <span data-ttu-id="f1168-119">（選擇性）用戶端會根據驗證通訊協定來驗證服務器身分識別。</span><span class="sxs-lookup"><span data-stu-id="f1168-119">Optionally, client authenticates server identity, depending on the authentication protocol.</span></span>
5.  <span data-ttu-id="f1168-120">方法呼叫會與所選的驗證層級進行通訊。</span><span class="sxs-lookup"><span data-stu-id="f1168-120">Method calls are communicated with the chosen level of authentication.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f1168-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="f1168-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f1168-122">用戶端驗證</span><span class="sxs-lookup"><span data-stu-id="f1168-122">Client Authentication</span></span>](client-authentication.md)
</dt> </dl>

 

 
