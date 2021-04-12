---
description: IX509EndorsementKey 介面會公開下列方法。
ms.assetid: 536E5DE6-FF14-45C8-9227-68AF673E5FDC
title: IX509EndorsementKey 方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3c1eb6a96cd555d4b0a0fdcd2ad52ccf80ec4aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195076"
---
# <a name="ix509endorsementkey-methods"></a><span data-ttu-id="f0496-103">IX509EndorsementKey 方法</span><span class="sxs-lookup"><span data-stu-id="f0496-103">IX509EndorsementKey Methods</span></span>

<span data-ttu-id="f0496-104">[**IX509EndorsementKey**](/windows/desktop/api/Certenroll/nn-certenroll-ix509endorsementkey)介面會公開下列方法。</span><span class="sxs-lookup"><span data-stu-id="f0496-104">The [**IX509EndorsementKey**](/windows/desktop/api/Certenroll/nn-certenroll-ix509endorsementkey) interface exposes the following methods.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="f0496-105">本節內容</span><span class="sxs-lookup"><span data-stu-id="f0496-105">In this section</span></span>



| <span data-ttu-id="f0496-106">主題</span><span class="sxs-lookup"><span data-stu-id="f0496-106">Topic</span></span>                                                                                        | <span data-ttu-id="f0496-107">描述</span><span class="sxs-lookup"><span data-stu-id="f0496-107">Description</span></span>                                                                                                                                                                                                                                                                                         |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f0496-108">**AddCertificate 方法**</span><span class="sxs-lookup"><span data-stu-id="f0496-108">**AddCertificate method**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-addcertificate)<br/>               | <span data-ttu-id="f0496-109">將簽署金鑰憑證新增至支援簽署金鑰 (KSP) 的金鑰儲存提供者。</span><span class="sxs-lookup"><span data-stu-id="f0496-109">Add an endorsement key certificate to the key storage provider (KSP) that supports endorsement keys.</span></span><br/>                                                                                                                                                                                     |
| [<span data-ttu-id="f0496-110">**Close 方法**</span><span class="sxs-lookup"><span data-stu-id="f0496-110">**Close method**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-close)<br/>                                 | <span data-ttu-id="f0496-111">關閉簽署金鑰。</span><span class="sxs-lookup"><span data-stu-id="f0496-111">Closes the endorsement key.</span></span> <span data-ttu-id="f0496-112">您只能在成功呼叫 [**Open**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-open)方法之後呼叫 [**Close**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-close)方法。</span><span class="sxs-lookup"><span data-stu-id="f0496-112">You can only call the [**Close**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-close) method after the [**Open**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-open) method has been successfully called.</span></span><br/>                                                                                              |
| [<span data-ttu-id="f0496-113">**ExportPublicKey 方法**</span><span class="sxs-lookup"><span data-stu-id="f0496-113">**ExportPublicKey method**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-exportpublickey)<br/>             | <span data-ttu-id="f0496-114">匯出簽署公開金鑰。</span><span class="sxs-lookup"><span data-stu-id="f0496-114">Exports the endorsement public key.</span></span><br/>                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="f0496-115">**GetCertificateByIndex 方法**</span><span class="sxs-lookup"><span data-stu-id="f0496-115">**GetCertificateByIndex method**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-getcertificatebyindex)<br/> | <span data-ttu-id="f0496-116">取得與指定索引之金鑰儲存提供者的簽署金鑰相關聯的簽署憑證。</span><span class="sxs-lookup"><span data-stu-id="f0496-116">Gets the endorsement certificate associated with the endorsement key from the key storage provider for the specified index.</span></span><br/>                                                                                                                                                              |
| [<span data-ttu-id="f0496-117">**GetCertificateCount 方法**</span><span class="sxs-lookup"><span data-stu-id="f0496-117">**GetCertificateCount method**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-getcertificatecount)<br/>     | <span data-ttu-id="f0496-118">取得金鑰儲存提供者中簽署憑證的計數。</span><span class="sxs-lookup"><span data-stu-id="f0496-118">Gets the count of the endorsement certificates in the key storage provider.</span></span><br/>                                                                                                                                                                                                              |
| [<span data-ttu-id="f0496-119">**Open 方法**</span><span class="sxs-lookup"><span data-stu-id="f0496-119">**Open method**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-open)<br/>                                   | <span data-ttu-id="f0496-120">開啟簽署金鑰。</span><span class="sxs-lookup"><span data-stu-id="f0496-120">Opens the endorsement key.</span></span> <span data-ttu-id="f0496-121">簽署金鑰必須先開啟，您才能從簽署金鑰取得資訊、新增或移除憑證，或匯出簽署金鑰。</span><span class="sxs-lookup"><span data-stu-id="f0496-121">The endorsement key must be open before you can retrieve an information from the endorsement key, add or remove certificates, or export the endorsement key.</span></span><br/>                                                                                                  |
| [<span data-ttu-id="f0496-122">**RemoveCertificate 方法**</span><span class="sxs-lookup"><span data-stu-id="f0496-122">**RemoveCertificate method**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-removecertificate)<br/>         | <span data-ttu-id="f0496-123">從金鑰儲存提供者移除簽署金鑰相關的簽署憑證。</span><span class="sxs-lookup"><span data-stu-id="f0496-123">Removes an endorsement certificate related to the endorsement key from the key storage provider.</span></span> <span data-ttu-id="f0496-124">您只能在成功呼叫 [**Open**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-open)方法之後呼叫 [**RemoveCertificate**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-removecertificate)方法。</span><span class="sxs-lookup"><span data-stu-id="f0496-124">You can only call the [**RemoveCertificate**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-removecertificate) method after the [**Open**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-open) method has been successfully called.</span></span><br/> |



 

 

 




