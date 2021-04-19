---
description: ICertAdmin2 介面會公開下列方法。
ms.assetid: F6E0D863-5A78-48D5-8AED-DAEF80101B7E
title: ICertAdmin2 方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 619e2afc9ee8e5e2eeab91893394e21e6c33ba14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987306"
---
# <a name="icertadmin2-methods"></a><span data-ttu-id="4cebd-103">ICertAdmin2 方法</span><span class="sxs-lookup"><span data-stu-id="4cebd-103">ICertAdmin2 Methods</span></span>

<span data-ttu-id="4cebd-104">[**ICertAdmin2**](/windows/desktop/api/Certadm/nn-certadm-icertadmin2)介面會公開下列方法。</span><span class="sxs-lookup"><span data-stu-id="4cebd-104">The [**ICertAdmin2**](/windows/desktop/api/Certadm/nn-certadm-icertadmin2) interface exposes the following methods.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="4cebd-105">本節內容</span><span class="sxs-lookup"><span data-stu-id="4cebd-105">In this section</span></span>

-   [<span data-ttu-id="4cebd-106">**DeleteRow 方法**</span><span class="sxs-lookup"><span data-stu-id="4cebd-106">**DeleteRow Method**</span></span>](/windows/desktop/api/Certadm/nf-certadm-icertadmin2-deleterow)
-   [<span data-ttu-id="4cebd-107">**DenyRequest 方法**</span><span class="sxs-lookup"><span data-stu-id="4cebd-107">**DenyRequest Method**</span></span>](/windows/desktop/api/Certadm/nf-certadm-icertadmin-denyrequest)
-   [<span data-ttu-id="4cebd-108">**GetArchivedKey 方法**</span><span class="sxs-lookup"><span data-stu-id="4cebd-108">**GetArchivedKey Method**</span></span>](/windows/desktop/api/Certadm/nf-certadm-icertadmin2-getarchivedkey)
-   [<span data-ttu-id="4cebd-109">**GetCAProperty 方法**</span><span class="sxs-lookup"><span data-stu-id="4cebd-109">**GetCAProperty Method**</span></span>](/windows/desktop/api/Certadm/nf-certadm-icertadmin2-getcaproperty)
-   [<span data-ttu-id="4cebd-110">**GetCAPropertyDisplayName 方法**</span><span class="sxs-lookup"><span data-stu-id="4cebd-110">**GetCAPropertyDisplayName Method**</span></span>](/windows/desktop/api/Certadm/nf-certadm-icertadmin2-getcapropertydisplayname)
-   [<span data-ttu-id="4cebd-111">**GetCAPropertyFlags 方法**</span><span class="sxs-lookup"><span data-stu-id="4cebd-111">**GetCAPropertyFlags Method**</span></span>](/windows/desktop/api/Certadm/nf-certadm-icertadmin2-getcapropertyflags)
-   [<span data-ttu-id="4cebd-112">**GetConfigEntry 方法**</span><span class="sxs-lookup"><span data-stu-id="4cebd-112">**GetConfigEntry Method**</span></span>](/windows/desktop/api/Certadm/nf-certadm-icertadmin2-getconfigentry)
-   [<span data-ttu-id="4cebd-113">**GetCRL 方法**</span><span class="sxs-lookup"><span data-stu-id="4cebd-113">**GetCRL Method**</span></span>](/windows/desktop/api/Certadm/nf-certadm-icertadmin-getcrl)
-   [<span data-ttu-id="4cebd-114">**GetMyRoles 方法**</span><span class="sxs-lookup"><span data-stu-id="4cebd-114">**GetMyRoles Method**</span></span>](/windows/desktop/api/Certadm/nf-certadm-icertadmin2-getmyroles)
-   [<span data-ttu-id="4cebd-115">**GetRevocationReason 方法**</span><span class="sxs-lookup"><span data-stu-id="4cebd-115">**GetRevocationReason Method**</span></span>](/windows/desktop/api/Certadm/nf-certadm-icertadmin-getrevocationreason)
-   [<span data-ttu-id="4cebd-116">**ImportCertificate 方法**</span><span class="sxs-lookup"><span data-stu-id="4cebd-116">**ImportCertificate Method**</span></span>](/windows/desktop/api/Certadm/nf-certadm-icertadmin-importcertificate)
-   [<span data-ttu-id="4cebd-117">**ImportKey 方法**</span><span class="sxs-lookup"><span data-stu-id="4cebd-117">**ImportKey Method**</span></span>](/windows/desktop/api/Certadm/nf-certadm-icertadmin2-importkey)
-   [<span data-ttu-id="4cebd-118">**IsValidCertificate 方法**</span><span class="sxs-lookup"><span data-stu-id="4cebd-118">**IsValidCertificate Method**</span></span>](/windows/desktop/api/Certadm/nf-certadm-icertadmin-isvalidcertificate)
-   [<span data-ttu-id="4cebd-119">**PublishCRL 方法**</span><span class="sxs-lookup"><span data-stu-id="4cebd-119">**PublishCRL Method**</span></span>](/windows/desktop/api/Certadm/nf-certadm-icertadmin-publishcrl)
-   [<span data-ttu-id="4cebd-120">**PublishCRLs 方法**</span><span class="sxs-lookup"><span data-stu-id="4cebd-120">**PublishCRLs Method**</span></span>](/windows/desktop/api/Certadm/nf-certadm-icertadmin2-publishcrls)
-   [<span data-ttu-id="4cebd-121">**ResubmitRequest 方法**</span><span class="sxs-lookup"><span data-stu-id="4cebd-121">**ResubmitRequest Method**</span></span>](/windows/desktop/api/Certadm/nf-certadm-icertadmin-resubmitrequest)
-   [<span data-ttu-id="4cebd-122">**RevokeCertificate 方法**</span><span class="sxs-lookup"><span data-stu-id="4cebd-122">**RevokeCertificate Method**</span></span>](/windows/desktop/api/Certadm/nf-certadm-icertadmin-revokecertificate)
-   [<span data-ttu-id="4cebd-123">**SetCAProperty 方法**</span><span class="sxs-lookup"><span data-stu-id="4cebd-123">**SetCAProperty Method**</span></span>](/windows/desktop/api/Certadm/nf-certadm-icertadmin2-setcaproperty)
-   [<span data-ttu-id="4cebd-124">**SetCertificateExtension 方法**</span><span class="sxs-lookup"><span data-stu-id="4cebd-124">**SetCertificateExtension Method**</span></span>](/windows/desktop/api/Certadm/nf-certadm-icertadmin-setcertificateextension)
-   [<span data-ttu-id="4cebd-125">**SetConfigEntry 方法**</span><span class="sxs-lookup"><span data-stu-id="4cebd-125">**SetConfigEntry Method**</span></span>](/windows/desktop/api/Certadm/nf-certadm-icertadmin2-setconfigentry)
-   [<span data-ttu-id="4cebd-126">**SetRequestAttributes 方法**</span><span class="sxs-lookup"><span data-stu-id="4cebd-126">**SetRequestAttributes Method**</span></span>](/windows/desktop/api/Certadm/nf-certadm-icertadmin-setrequestattributes)

 

 



