---
description: 網路來源驗證
ms.assetid: bffc33ec-0fb0-4bbe-9bac-583b9d4e1153
title: 網路來源驗證
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09c38968fccf501f49ac7666a066b88528b237bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026393"
---
# <a name="network-source-authentication"></a><span data-ttu-id="286a1-103">網路來源驗證</span><span class="sxs-lookup"><span data-stu-id="286a1-103">Network Source Authentication</span></span>

<span data-ttu-id="286a1-104">某些媒體主機在允許存取媒體之前，可能需要來自用戶端應用程式的使用者認證。</span><span class="sxs-lookup"><span data-stu-id="286a1-104">Certain media hosts may require user credentials from client applications before allowing access to the media.</span></span> <span data-ttu-id="286a1-105">使用者認證包括識別和辨識證明，例如使用者名稱和密碼，媒體伺服器會使用這些認證來授與存取權給其所裝載的網路來源。</span><span class="sxs-lookup"><span data-stu-id="286a1-105">User credentials include identification and proof of identification, such as user name and password, which are used by the media server to grant access to the network source it hosts.</span></span> <span data-ttu-id="286a1-106">網路來源可以提供 NTLM、摘要式或基本驗證。</span><span class="sxs-lookup"><span data-stu-id="286a1-106">The network source can provide NTLM, Digest, or Basic authentication.</span></span>

<span data-ttu-id="286a1-107">以媒體基礎為基礎的應用程式可以將特定 URL 的使用者認證儲存在公開 [**IMFNetCredential**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredential)介面的 *credential* 物件中。</span><span class="sxs-lookup"><span data-stu-id="286a1-107">Applications based on Media Foundation can store user credentials for a specific URL in a *credential* object that exposes the [**IMFNetCredential**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredential) interface.</span></span> <span data-ttu-id="286a1-108">認證物件會儲存加密的認證，並提供方法來傳回信息，例如使用者名稱、密碼和網域。</span><span class="sxs-lookup"><span data-stu-id="286a1-108">The credential object stores encrypted credentials and provides methods to return information such as user name, password, and domain.</span></span>

<span data-ttu-id="286a1-109">認證物件會在快取中建立和維護。</span><span class="sxs-lookup"><span data-stu-id="286a1-109">The credential objects are created and maintained in a cache.</span></span> <span data-ttu-id="286a1-110">[**IMFNetCredentialCache**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialcache)介面所公開的 *認證* 快取物件，提供從認證快取中取得認證物件的方法。</span><span class="sxs-lookup"><span data-stu-id="286a1-110">The *credential cache* object, exposed by the [**IMFNetCredentialCache**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialcache) interface provides methods for retrieving the credential objects from the credential cache.</span></span>

<span data-ttu-id="286a1-111">支援驗證的應用程式必須執行 [**IMFNetCredentialManager**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager) 介面。</span><span class="sxs-lookup"><span data-stu-id="286a1-111">An application that supports authentication must implement the [**IMFNetCredentialManager**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager) interface.</span></span> <span data-ttu-id="286a1-112">媒體基礎不會提供此介面的預設執行。</span><span class="sxs-lookup"><span data-stu-id="286a1-112">Media Foundation does not provide a default implementation of this interface.</span></span> <span data-ttu-id="286a1-113">認證管理員負責收集來自使用者輸入或從持續性儲存區讀取的 URL 所需的認證。</span><span class="sxs-lookup"><span data-stu-id="286a1-113">The credential manager is responsible for gathering the required credentials for a URL from user input or reading from persisted storage.</span></span>

<span data-ttu-id="286a1-114">本節包含下列主題：</span><span class="sxs-lookup"><span data-stu-id="286a1-114">This section contains the following topics:</span></span>

-   [<span data-ttu-id="286a1-115">設定認證管理員</span><span class="sxs-lookup"><span data-stu-id="286a1-115">Setting a Credential Manager</span></span>](setting-a-credential-manager.md)
-   [<span data-ttu-id="286a1-116">使用認證快取</span><span class="sxs-lookup"><span data-stu-id="286a1-116">Using the Credential Cache</span></span>](using-the-credential-cache.md)
-   [<span data-ttu-id="286a1-117">執行 IMFNetCredentialManager</span><span class="sxs-lookup"><span data-stu-id="286a1-117">Implementing IMFNetCredentialManager</span></span>](implementing-imfnetcredentialmanager.md)

## <a name="related-topics"></a><span data-ttu-id="286a1-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="286a1-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="286a1-119">媒體基礎中的網路功能</span><span class="sxs-lookup"><span data-stu-id="286a1-119">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 



