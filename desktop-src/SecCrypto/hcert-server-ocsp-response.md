---
description: 表示與伺服器憑證鏈相關聯之 OCSP 回應的控制碼。
ms.assetid: baf173f1-99dc-49f9-9a17-fee79b393db7
title: 'HCERT_SERVER_OCSP_RESPONSE (Wincrypt) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ceab319b5d8370dd15ef3dcd288124e4f2adf9ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851299"
---
# <a name="hcert_server_ocsp_response"></a><span data-ttu-id="6f04b-103">HCERT \_ SERVER \_ OCSP \_ 回應</span><span class="sxs-lookup"><span data-stu-id="6f04b-103">HCERT\_SERVER\_OCSP\_RESPONSE</span></span>

<span data-ttu-id="6f04b-104">**HCERT \_ SERVER \_ OCSP \_ 回應** 資料類型代表與伺服器憑證鏈相關聯之 OCSP 回應的控制碼。</span><span class="sxs-lookup"><span data-stu-id="6f04b-104">The **HCERT\_SERVER\_OCSP\_RESPONSE** data type represents a handle to an OCSP response associated with a server certificate chain.</span></span>

<span data-ttu-id="6f04b-105">下列 Api 會使用此類型。</span><span class="sxs-lookup"><span data-stu-id="6f04b-105">This type is used by the following APIs.</span></span>

-   [<span data-ttu-id="6f04b-106">**CertOpenServerOcspResponse**</span><span class="sxs-lookup"><span data-stu-id="6f04b-106">**CertOpenServerOcspResponse**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenserverocspresponse)
-   [<span data-ttu-id="6f04b-107">**CertAddRefServerOcspResponse**</span><span class="sxs-lookup"><span data-stu-id="6f04b-107">**CertAddRefServerOcspResponse**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddrefserverocspresponse)
-   [<span data-ttu-id="6f04b-108">**CertCloseServerOcspResponse**</span><span class="sxs-lookup"><span data-stu-id="6f04b-108">**CertCloseServerOcspResponse**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certcloseserverocspresponse)
-   [<span data-ttu-id="6f04b-109">**CertGetServerOcspResponseCoNtext**</span><span class="sxs-lookup"><span data-stu-id="6f04b-109">**CertGetServerOcspResponseContext**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetserverocspresponsecontext)


```C++
typedef VOID* HCERT_SERVER_OCSP_RESPONSE;
```



## <a name="requirements"></a><span data-ttu-id="6f04b-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="6f04b-110">Requirements</span></span>



| <span data-ttu-id="6f04b-111">需求</span><span class="sxs-lookup"><span data-stu-id="6f04b-111">Requirement</span></span> | <span data-ttu-id="6f04b-112">值</span><span class="sxs-lookup"><span data-stu-id="6f04b-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6f04b-113">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6f04b-113">Minimum supported client</span></span><br/> | <span data-ttu-id="6f04b-114">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6f04b-114">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6f04b-115">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6f04b-115">Minimum supported server</span></span><br/> | <span data-ttu-id="6f04b-116">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6f04b-116">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6f04b-117">標頭</span><span class="sxs-lookup"><span data-stu-id="6f04b-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="6f04b-118"><dt>Wincrypt。h</dt></span><span class="sxs-lookup"><span data-stu-id="6f04b-118"><dt>Wincrypt.h</dt></span></span> </dl> |



 

 




