---
description: IX509SCEPEnrollment 介面會公開下列屬性。
ms.assetid: 53BE8DE9-87AC-41D1-B1B5-2FEC72F5FCEA
title: IX509SCEPEnrollment 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2fd9b4cbf9df87f898e61ce0220243044b24607d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "107001397"
---
# <a name="ix509scepenrollment-properties"></a><span data-ttu-id="3b572-103">IX509SCEPEnrollment 屬性</span><span class="sxs-lookup"><span data-stu-id="3b572-103">IX509SCEPEnrollment Properties</span></span>

<span data-ttu-id="3b572-104">[**IX509SCEPEnrollment**](/windows/desktop/api/Certenroll/nn-certenroll-ix509scepenrollment)介面會公開下列屬性。</span><span class="sxs-lookup"><span data-stu-id="3b572-104">The [**IX509SCEPEnrollment**](/windows/desktop/api/Certenroll/nn-certenroll-ix509scepenrollment) interface exposes the following properties.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="3b572-105">本節內容</span><span class="sxs-lookup"><span data-stu-id="3b572-105">In this section</span></span>



| <span data-ttu-id="3b572-106">主題</span><span class="sxs-lookup"><span data-stu-id="3b572-106">Topic</span></span>                                                                                              | <span data-ttu-id="3b572-107">描述</span><span class="sxs-lookup"><span data-stu-id="3b572-107">Description</span></span>                                                                                                                                            |
|----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3b572-108">**Certificate 屬性**</span><span class="sxs-lookup"><span data-stu-id="3b572-108">**Certificate property**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-get_certificate)<br/>                         | <span data-ttu-id="3b572-109">取得要求的憑證。</span><span class="sxs-lookup"><span data-stu-id="3b572-109">Gets the certificate for the request.</span></span><br/>                                                                                                       |
| [<span data-ttu-id="3b572-110">**Enrollment.certificatefriendlyname 屬性**</span><span class="sxs-lookup"><span data-stu-id="3b572-110">**CertificateFriendlyName property**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-get_certificatefriendlyname)<br/> | <span data-ttu-id="3b572-111">取得或設定憑證的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="3b572-111">Gets or sets the friendly name for the certificate.</span></span><br/>                                                                                         |
| [<span data-ttu-id="3b572-112">**FailInfo 屬性**</span><span class="sxs-lookup"><span data-stu-id="3b572-112">**FailInfo property**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-get_failinfo)<br/>                               | <span data-ttu-id="3b572-113">取得 [**ProcessResponseMessage**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-processresponsemessage) 方法偵測到失敗環境時的資訊。</span><span class="sxs-lookup"><span data-stu-id="3b572-113">Gets information when the [**ProcessResponseMessage**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-processresponsemessage) method detects a failed environment.</span></span><br/> |
| [<span data-ttu-id="3b572-114">**OldCertificate 屬性**</span><span class="sxs-lookup"><span data-stu-id="3b572-114">**OldCertificate property**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-get_oldcertificate)<br/>                   | <span data-ttu-id="3b572-115">取得或設定要求要取代的舊憑證。</span><span class="sxs-lookup"><span data-stu-id="3b572-115">Gets or sets an old certificate that a request is intended to replace.</span></span><br/>                                                                      |
| [<span data-ttu-id="3b572-116">**要求屬性**</span><span class="sxs-lookup"><span data-stu-id="3b572-116">**Request property**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-get_request)<br/>                                 | <span data-ttu-id="3b572-117">取得內部 PKCS10 要求。</span><span class="sxs-lookup"><span data-stu-id="3b572-117">Gets the inner PKCS10 request.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="3b572-118">**ServerCapabilities 屬性**</span><span class="sxs-lookup"><span data-stu-id="3b572-118">**ServerCapabilities property**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-put_servercapabilities)<br/>           | <span data-ttu-id="3b572-119">為要求設定慣用的雜湊和加密演算法。</span><span class="sxs-lookup"><span data-stu-id="3b572-119">Sets the preferred hash and encryption algorithms for the request.</span></span><br/>                                                                          |
| [<span data-ttu-id="3b572-120">**SignerCertificate 屬性**</span><span class="sxs-lookup"><span data-stu-id="3b572-120">**SignerCertificate property**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-get_signercertificate)<br/>             | <span data-ttu-id="3b572-121">取得或設定要求的簽署者憑證。</span><span class="sxs-lookup"><span data-stu-id="3b572-121">Gets or sets the signer certificate for the request.</span></span><br/>                                                                                        |
| [<span data-ttu-id="3b572-122">**無訊息屬性**</span><span class="sxs-lookup"><span data-stu-id="3b572-122">**Silent property**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-put_silent)<br/>                                   | <span data-ttu-id="3b572-123">取得或設定是否要在要求期間允許 UI。</span><span class="sxs-lookup"><span data-stu-id="3b572-123">Gets or sets whether to allow UI during the request.</span></span><br/>                                                                                        |
| [<span data-ttu-id="3b572-124">**Status 屬性**</span><span class="sxs-lookup"><span data-stu-id="3b572-124">**Status property**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-get_status)<br/>                                   | <span data-ttu-id="3b572-125">取得要求的狀態。</span><span class="sxs-lookup"><span data-stu-id="3b572-125">Gets the status of the request.</span></span><br/>                                                                                                             |
| [<span data-ttu-id="3b572-126">**TransactionId 屬性**</span><span class="sxs-lookup"><span data-stu-id="3b572-126">**TransactionId property**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-get_transactionid)<br/>                     | <span data-ttu-id="3b572-127">取得或設定要求的交易識別碼。</span><span class="sxs-lookup"><span data-stu-id="3b572-127">Gets or sets the transaction id for the request.</span></span><br/>                                                                                            |



 

 

 




