---
description: 憑證範例。 建立 api 認證的應用程式、安裝 SSL 憑證、伺服器憑證、透過媒體（例如網際網路或內部網路）建立不安全的憑證。
ms.assetid: 8d4add69-53f7-4e78-b9ea-e5915411f42f
title: 憑證註冊 API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 490880e395a71b557fc05fcf6168132201bc1b91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511552"
---
# <a name="certificate-enrollment-api"></a><span data-ttu-id="0fcd7-104">憑證註冊 API</span><span class="sxs-lookup"><span data-stu-id="0fcd7-104">Certificate Enrollment API</span></span>

## <a name="purpose"></a><span data-ttu-id="0fcd7-105">目的</span><span class="sxs-lookup"><span data-stu-id="0fcd7-105">Purpose</span></span>

<span data-ttu-id="0fcd7-106">憑證註冊 API 可以用來建立用戶端應用程式，以要求憑證並安裝憑證回應。</span><span class="sxs-lookup"><span data-stu-id="0fcd7-106">The Certificate Enrollment API can be used to create a client application to request a certificate and install a certificate response.</span></span> <span data-ttu-id="0fcd7-107">此 API 會在從 Windows Vista 開始 CertEnroll.dll 中執行;它會取代 Xenroll.dll。</span><span class="sxs-lookup"><span data-stu-id="0fcd7-107">This API is implemented in CertEnroll.dll beginning with Windows Vista; it replaces Xenroll.dll.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="0fcd7-108">開發人員對象</span><span class="sxs-lookup"><span data-stu-id="0fcd7-108">Developer audience</span></span>

<span data-ttu-id="0fcd7-109">憑證註冊 API 適用于應用程式開發人員，這些應用程式可讓使用者透過不安全的媒體（例如網際網路或內部網路）建立、要求及取出憑證。</span><span class="sxs-lookup"><span data-stu-id="0fcd7-109">The Certificate Enrollment API is for use by developers of applications that will enable users to create, request, and retrieve certificates over media, such as the Internet or an intranet, that are not inherently secure.</span></span> <span data-ttu-id="0fcd7-110">開發人員應該熟悉 C 和 c + + 程式設計語言、元件物件模型 (COM) 和以 Windows 為基礎的程式設計環境。</span><span class="sxs-lookup"><span data-stu-id="0fcd7-110">Developers should be familiar with the C and C++ programming languages, the Component Object Model (COM), and the Windows-based programming environment.</span></span> <span data-ttu-id="0fcd7-111">雖然並非必要，但建議您瞭解密碼編譯和公開金鑰基礎結構。</span><span class="sxs-lookup"><span data-stu-id="0fcd7-111">Although not required, an understanding of cryptography and public key infrastructure is advised.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="0fcd7-112">執行階段需求求</span><span class="sxs-lookup"><span data-stu-id="0fcd7-112">Run-time requirements</span></span>

<span data-ttu-id="0fcd7-113">從 Windows Server 2008 和 Windows Vista 開始支援憑證註冊 API。</span><span class="sxs-lookup"><span data-stu-id="0fcd7-113">The Certificate Enrollment API is supported beginning with Windows Server 2008 and Windows Vista.</span></span> <span data-ttu-id="0fcd7-114">如需特定程式設計專案之執行時間需求的詳細資訊，請參閱該元素之 [參考] 頁面的 [需求] 區段。</span><span class="sxs-lookup"><span data-stu-id="0fcd7-114">For information about run-time requirements for a particular programming element, see the Requirements section of the reference page for that element.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="0fcd7-115">本節內容</span><span class="sxs-lookup"><span data-stu-id="0fcd7-115">In this section</span></span>



| <span data-ttu-id="0fcd7-116">主題</span><span class="sxs-lookup"><span data-stu-id="0fcd7-116">Topic</span></span>                                                                                       | <span data-ttu-id="0fcd7-117">描述</span><span class="sxs-lookup"><span data-stu-id="0fcd7-117">Description</span></span>                                                                                                                                                            |
|---------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0fcd7-118">關於憑證註冊 API</span><span class="sxs-lookup"><span data-stu-id="0fcd7-118">About the Certificate Enrollment API</span></span>](about-the-certificate-enrollment-api.md)<br/> | <span data-ttu-id="0fcd7-119">討論有關憑證要求的重要概念。</span><span class="sxs-lookup"><span data-stu-id="0fcd7-119">Key concepts about certificate requests are discussed.</span></span><br/>                                                                                                      |
| [<span data-ttu-id="0fcd7-120">使用憑證註冊 API</span><span class="sxs-lookup"><span data-stu-id="0fcd7-120">Using the Certificate Enrollment API</span></span>](using-the-certificate-enrollment-api.md)<br/> | <span data-ttu-id="0fcd7-121">如何使用憑證註冊 API 擴充 Active Directory 憑證服務的功能。</span><span class="sxs-lookup"><span data-stu-id="0fcd7-121">How to use the Certificate Enrollment API to extend the capabilities of Active Directory Certificate Services.</span></span><br/>                                              |
| [<span data-ttu-id="0fcd7-122">憑證註冊 API 參考</span><span class="sxs-lookup"><span data-stu-id="0fcd7-122">Certificate Enrollment API Reference</span></span>](certificate-enrollment-api-reference.md)<br/> | <span data-ttu-id="0fcd7-123">介面、列舉和其他程式設計專案的詳細描述，這些專案可以用來註冊憑證階層中的使用者或電腦。</span><span class="sxs-lookup"><span data-stu-id="0fcd7-123">Detailed descriptions of interfaces, enumerations, and other programming elements that can be used to enroll a user or computer in a certificate hierarchy.</span></span><br/> |



 

 

 




