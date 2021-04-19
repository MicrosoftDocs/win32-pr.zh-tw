---
description: IX509SCEPEnrollment 介面會公開下列方法。
ms.assetid: B45B68D2-A14D-4D14-AF5F-1A1BB9921A0D
title: IX509SCEPEnrollment 方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a33c3bdee14b865211b53649075dec6d4617a4c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975782"
---
# <a name="ix509scepenrollment-methods"></a><span data-ttu-id="f2bc6-103">IX509SCEPEnrollment 方法</span><span class="sxs-lookup"><span data-stu-id="f2bc6-103">IX509SCEPEnrollment Methods</span></span>

<span data-ttu-id="f2bc6-104">[**IX509SCEPEnrollment**](/windows/desktop/api/Certenroll/nn-certenroll-ix509scepenrollment)介面會公開下列方法。</span><span class="sxs-lookup"><span data-stu-id="f2bc6-104">The [**IX509SCEPEnrollment**](/windows/desktop/api/Certenroll/nn-certenroll-ix509scepenrollment) interface exposes the following methods.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="f2bc6-105">本節內容</span><span class="sxs-lookup"><span data-stu-id="f2bc6-105">In this section</span></span>



| <span data-ttu-id="f2bc6-106">主題</span><span class="sxs-lookup"><span data-stu-id="f2bc6-106">Topic</span></span>                                                                                                              | <span data-ttu-id="f2bc6-107">描述</span><span class="sxs-lookup"><span data-stu-id="f2bc6-107">Description</span></span>                                                                                                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f2bc6-108">**CreateRequestMessage 方法**</span><span class="sxs-lookup"><span data-stu-id="f2bc6-108">**CreateRequestMessage method**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-createrequestmessage)<br/>                         | <span data-ttu-id="f2bc6-109">建立含有挑戰密碼的 PKCS10 要求訊息。</span><span class="sxs-lookup"><span data-stu-id="f2bc6-109">Create a PKCS10 request message with a challenge password.</span></span> <span data-ttu-id="f2bc6-110">要求訊息位於以 SCEP 伺服器加密憑證加密，並且由伺服器簽署憑證簽署的封包 PKCS7 中。</span><span class="sxs-lookup"><span data-stu-id="f2bc6-110">The request message is in an enveloped PKCS7 encrypted with the SCEP server encryption certificate and signed by the server signing certificate.</span></span><br/> |
| [<span data-ttu-id="f2bc6-111">**CreateRetrieveCertificateMessage 方法**</span><span class="sxs-lookup"><span data-stu-id="f2bc6-111">**CreateRetrieveCertificateMessage method**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-createretrievecertificatemessage)<br/> | <span data-ttu-id="f2bc6-112">取出先前發行的憑證。</span><span class="sxs-lookup"><span data-stu-id="f2bc6-112">Retrieve a previously issued certificate.</span></span><br/>                                                                                                                                                                   |
| [<span data-ttu-id="f2bc6-113">**CreateRetrievePendingMessage 方法**</span><span class="sxs-lookup"><span data-stu-id="f2bc6-113">**CreateRetrievePendingMessage method**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-createretrievependingmessage)<br/>         | <span data-ttu-id="f2bc6-114">為憑證輪詢建立訊息 (手動註冊) 。</span><span class="sxs-lookup"><span data-stu-id="f2bc6-114">Create a message for certificate polling (manual enrollment).</span></span><br/>                                                                                                                                               |
| [<span data-ttu-id="f2bc6-115">**DeleteRequest 方法**</span><span class="sxs-lookup"><span data-stu-id="f2bc6-115">**DeleteRequest method**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-deleterequest)<br/>                                       | <span data-ttu-id="f2bc6-116">刪除針對要求所建立的任何憑證或金鑰。</span><span class="sxs-lookup"><span data-stu-id="f2bc6-116">Delete any certificates or keys created for the request.</span></span><br/>                                                                                                                                                    |
| [<span data-ttu-id="f2bc6-117">**Initialize 方法**</span><span class="sxs-lookup"><span data-stu-id="f2bc6-117">**Initialize method**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-initialize)<br/>                                             | <span data-ttu-id="f2bc6-118">初始化實例以準備新的要求。</span><span class="sxs-lookup"><span data-stu-id="f2bc6-118">Initialize the instance in preparation for a new request.</span></span><br/>                                                                                                                                                   |
| [<span data-ttu-id="f2bc6-119">**InitializeForPending 方法**</span><span class="sxs-lookup"><span data-stu-id="f2bc6-119">**InitializeForPending method**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-initializeforpending)<br/>                         | <span data-ttu-id="f2bc6-120">初始化實例，以準備產生訊息以取得已發行的憑證，或為簽發者安裝先前要求的回應。</span><span class="sxs-lookup"><span data-stu-id="f2bc6-120">Initialize the instance to prepare to generate a message to either retrieve an issued certificate, or install a response for a previous request by the issuer.</span></span><br/>                                              |
| [<span data-ttu-id="f2bc6-121">**ProcessResponseMessage 方法**</span><span class="sxs-lookup"><span data-stu-id="f2bc6-121">**ProcessResponseMessage method**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-processresponsemessage)<br/>                     | <span data-ttu-id="f2bc6-122">處理回應訊息並傳回訊息的處置。</span><span class="sxs-lookup"><span data-stu-id="f2bc6-122">Process a response message and return the disposition of the message.</span></span><br/>                                                                                                                                       |



 

 

 




