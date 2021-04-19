---
description: 在某些情況下，金鑰必須從密碼編譯服務提供者的安全環境中匯出 (CSP) 到應用程式的資料空間。 已匯出的金鑰會儲存在加密的金鑰 BLOB 結構中。
ms.assetid: 859b1bfe-6182-4728-a721-1f34cc98f66f
title: 密碼編譯金鑰儲存和交換
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be7e789a736f0fcd5208bc16d73b43c6a9232e33
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106998062"
---
# <a name="cryptographic-key-storage-and-exchange"></a><span data-ttu-id="12b6d-104">密碼編譯金鑰儲存和交換</span><span class="sxs-lookup"><span data-stu-id="12b6d-104">Cryptographic Key Storage and Exchange</span></span>

<span data-ttu-id="12b6d-105">在某些情況下，金鑰必須從 [*密碼編譯服務提供者*](../secgloss/c-gly.md) 的安全環境中匯出 (CSP) 到應用程式的資料空間。</span><span class="sxs-lookup"><span data-stu-id="12b6d-105">There are situations where keys must be exported from the secure environment of the [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) into an application's data space.</span></span> <span data-ttu-id="12b6d-106">已匯出的金鑰會儲存在加密的 [*金鑰 BLOB*](../secgloss/k-gly.md) 結構中。</span><span class="sxs-lookup"><span data-stu-id="12b6d-106">Keys that have been exported are stored in encrypted [*key BLOB*](../secgloss/k-gly.md) structures.</span></span>

<span data-ttu-id="12b6d-107">有兩個特定的情況需要匯出金鑰：</span><span class="sxs-lookup"><span data-stu-id="12b6d-107">There are two specific situations where it is necessary to export keys:</span></span>

-   <span data-ttu-id="12b6d-108">若要儲存 [*工作階段金鑰*](../secgloss/s-gly.md) 以供應用程式稍後使用，例如，應用程式只會加密資料庫檔案，稍後再進行解密。</span><span class="sxs-lookup"><span data-stu-id="12b6d-108">To save a [*session key*](../secgloss/s-gly.md) for later use by an application, if, for example, an application has just encrypted a database file to be decrypted at a later time.</span></span> <span data-ttu-id="12b6d-109">應用程式會負責儲存加密金鑰。</span><span class="sxs-lookup"><span data-stu-id="12b6d-109">The application is responsible for storing the encryption key.</span></span> <span data-ttu-id="12b6d-110">這是必要的，因為 Csp 不會保留會話之間的 [*對稱金鑰*](../secgloss/s-gly.md) 。</span><span class="sxs-lookup"><span data-stu-id="12b6d-110">This is necessary because CSPs do not preserve [*symmetric keys*](../secgloss/s-gly.md) from session to session.</span></span>
-   <span data-ttu-id="12b6d-111">將金鑰傳送給其他人。</span><span class="sxs-lookup"><span data-stu-id="12b6d-111">To send a key to someone else.</span></span> <span data-ttu-id="12b6d-112">如果個別的 Csp 可以直接通訊，但不能這麼做，就會比較容易。</span><span class="sxs-lookup"><span data-stu-id="12b6d-112">This would be easier if the respective CSPs could communicate directly, but they cannot.</span></span> <span data-ttu-id="12b6d-113">因為 Csp 無法通訊，所以必須從一個 CSP 匯出金鑰，並傳輸至目的地應用程式，然後再匯入到目的地 CSP 中。</span><span class="sxs-lookup"><span data-stu-id="12b6d-113">Because CSPs cannot communicate, the key has to be exported from one CSP, transmitted to the destination application, and then imported into the destination CSP.</span></span> <span data-ttu-id="12b6d-114">如果通訊路徑不受信任，此程式可能會變得更複雜。</span><span class="sxs-lookup"><span data-stu-id="12b6d-114">This process can become more complicated if the communication path is not trusted.</span></span>

<span data-ttu-id="12b6d-115">無論是哪一種情況，應用程式都必須將工作階段金鑰儲存在 CSP 外一段時間。</span><span class="sxs-lookup"><span data-stu-id="12b6d-115">In either case, an application must store a session key outside the CSP for a period of time.</span></span> <span data-ttu-id="12b6d-116">如需詳細資訊，請參閱 [儲存工作階段金鑰](procedure-for-storing-a-session-key.md)的程式。</span><span class="sxs-lookup"><span data-stu-id="12b6d-116">For more information, see [Procedure for Storing a Session Key](procedure-for-storing-a-session-key.md).</span></span>

 

 
