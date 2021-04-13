---
title: EAP 安裝
description: 廠商會在動態連結程式庫中執行 EAPs，也稱為驗證通訊協定， (Dll) 。
ms.assetid: af10b1e9-45c9-4640-ba79-fc9c23cc3c47
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 619505a55108ebde0e14d7ff20c78394c6c90fad
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/26/2019
ms.locfileid: "104373987"
---
# <a name="eap-installation"></a><span data-ttu-id="f77e7-103">EAP 安裝</span><span class="sxs-lookup"><span data-stu-id="f77e7-103">EAP Installation</span></span>

<span data-ttu-id="f77e7-104">廠商會在動態連結程式庫中執行 EAPs，也稱為驗證通訊協定， (Dll) 。</span><span class="sxs-lookup"><span data-stu-id="f77e7-104">Vendors implement EAPs, also known as authentication protocols, in dynamic-link libraries (DLLs).</span></span> <span data-ttu-id="f77e7-105">驗證通訊協定的 DLL 必須同時位於用戶端和伺服器電腦上。</span><span class="sxs-lookup"><span data-stu-id="f77e7-105">A DLL for the authentication protocol must reside on both the client and server computers.</span></span> <span data-ttu-id="f77e7-106">為了簡單起見，用戶端和伺服器 Dll 可能完全相同;不過，這不是必要條件。</span><span class="sxs-lookup"><span data-stu-id="f77e7-106">For simplicity, the client and server DLLs may be identical; however, this is not a requirement.</span></span> <span data-ttu-id="f77e7-107">此外，請注意，相同的 DLL 可能會支援多個驗證通訊協定。</span><span class="sxs-lookup"><span data-stu-id="f77e7-107">Also, be aware that the same DLL may support more than one authentication protocol.</span></span>

<span data-ttu-id="f77e7-108">廠商應提供安裝軟體以安裝和移除 DLL。</span><span class="sxs-lookup"><span data-stu-id="f77e7-108">The vendor should provide setup software to install and remove the DLL.</span></span> <span data-ttu-id="f77e7-109">安裝軟體也應該在系統登錄中為驗證通訊協定建立適當的機碼和值，並在卸載時移除這些金鑰和值。</span><span class="sxs-lookup"><span data-stu-id="f77e7-109">The setup software should also create the appropriate keys and values for the authentication protocol in the system registry and remove them upon uninstall.</span></span>

<span data-ttu-id="f77e7-110">每個 EAP DLL 的安裝應該會建立下列登錄機碼。</span><span class="sxs-lookup"><span data-stu-id="f77e7-110">The installation of each EAP DLL should create the following registry key.</span></span>

<span data-ttu-id="f77e7-111">**HKEY \_LOCAL \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **Rasman** \\ **PPP** \\ **EAP** \\ **&lt; eaptypeid &gt;**</span><span class="sxs-lookup"><span data-stu-id="f77e7-111">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Services**\\**Rasman**\\**PPP**\\**EAP**\\**&lt;eaptypeid&gt;**</span></span>

<span data-ttu-id="f77e7-112">在上述路徑中， **&lt; eaptypeid &gt;** 是驗證通訊協定的識別碼。</span><span class="sxs-lookup"><span data-stu-id="f77e7-112">In the preceding path, **&lt;eaptypeid&gt;** is the ID of the authentication protocol.</span></span> <span data-ttu-id="f77e7-113">廠商必須從網際網路指派的號碼授權單位取得此識別碼 (IANA) 。</span><span class="sxs-lookup"><span data-stu-id="f77e7-113">The vendor must obtain this ID from the Internet Assigned Numbers Authority (IANA).</span></span>

<span data-ttu-id="f77e7-114">如需此機碼支援值的詳細資訊和描述，請參閱 [驗證通訊協定登錄值](authentication-protocol-registry-values.md)。</span><span class="sxs-lookup"><span data-stu-id="f77e7-114">For more information and a description of the supported values for this key, see [Authentication Protocol Registry Values](authentication-protocol-registry-values.md).</span></span>

 

 




