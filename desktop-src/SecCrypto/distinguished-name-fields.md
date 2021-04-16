---
description: 包含應唯一識別提出要求之人員的資訊。
ms.assetid: f0cc0e1b-370e-4548-97fe-8f6a4005540b
title: 辨別名稱欄位
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28a03495d19608e29aa60f09954c96a10f6c3cde
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104513384"
---
# <a name="distinguished-name-fields"></a><span data-ttu-id="a5f69-103">辨別名稱欄位</span><span class="sxs-lookup"><span data-stu-id="a5f69-103">Distinguished Name Fields</span></span>

<span data-ttu-id="a5f69-104">[*憑證要求*](../secgloss/c-gly.md)包含的資訊應可唯一識別提出要求的人員。</span><span class="sxs-lookup"><span data-stu-id="a5f69-104">A [*certificate request*](../secgloss/c-gly.md) contains information that should uniquely identify the individual making the request.</span></span>

<span data-ttu-id="a5f69-105">\#憑證服務接受的 PKCS 10 格式憑證要求包含識別欄位，稱為辨別名稱 (DN) 欄位。</span><span class="sxs-lookup"><span data-stu-id="a5f69-105">PKCS \#10 format certificate requests that are accepted by Certificate Services contain identification fields that are referred to as Distinguished Name (DN) fields.</span></span> <span data-ttu-id="a5f69-106">這些欄位將包含使用者在使用金鑰管理員、 [憑證註冊控制](certificate-enrollment-control.md)或其他方法建立憑證要求時所輸入的資訊。</span><span class="sxs-lookup"><span data-stu-id="a5f69-106">These fields will contain the information that is input by the user when a certificate request is being created by Key Manager, [Certificate Enrollment Control](certificate-enrollment-control.md), or some other means.</span></span>

<span data-ttu-id="a5f69-107">以下是在憑證要求中完成 DN 欄位的一些指導方針。</span><span class="sxs-lookup"><span data-stu-id="a5f69-107">The following are some guidelines for completion of DN fields in a certificate request.</span></span>



| <span data-ttu-id="a5f69-108">欄位</span><span class="sxs-lookup"><span data-stu-id="a5f69-108">Field</span></span>               | <span data-ttu-id="a5f69-109">描述</span><span class="sxs-lookup"><span data-stu-id="a5f69-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                                      |
|---------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5f69-110">一般名稱</span><span class="sxs-lookup"><span data-stu-id="a5f69-110">Common Name</span></span>         | <span data-ttu-id="a5f69-111">使用者憑證：您應輸入人員的完整名稱。</span><span class="sxs-lookup"><span data-stu-id="a5f69-111">User Certificates: You should enter the person's full name.</span></span> <span data-ttu-id="a5f69-112">電腦憑證：您應輸入 \*伺服器將在其上執行的 DNS 查閱中所使用的完整主機名稱 \* **/** _路徑_ (例如， \*hostname \***。**_範例_*_.com_*) 。</span><span class="sxs-lookup"><span data-stu-id="a5f69-112">Machine Certificates: You should enter the fully qualified *HostName\***/**_Path_ used in DNS lookups that the server will be running on (for example, *HostName\***.**_Example_*_.com_*).</span></span><br/>                                                                                                  |
| <span data-ttu-id="a5f69-113">組織</span><span class="sxs-lookup"><span data-stu-id="a5f69-113">Organization</span></span>        | <span data-ttu-id="a5f69-114">您為 [組織] 欄位指定的名稱應該是您組織中已向適當城市、州或國家/地區授權單位註冊的法定名稱。</span><span class="sxs-lookup"><span data-stu-id="a5f69-114">The name you specify for the Organization field should be the legal name for your organization that is registered with the appropriate city, state, or country/region authority.</span></span> <span data-ttu-id="a5f69-115">組織的法定名稱必須用在 [組織] 欄位中。</span><span class="sxs-lookup"><span data-stu-id="a5f69-115">The legal name of the organization must be used in the Organization field.</span></span>                                                                                                      |
| <span data-ttu-id="a5f69-116">組織單位</span><span class="sxs-lookup"><span data-stu-id="a5f69-116">Organizational Unit</span></span> | <span data-ttu-id="a5f69-117">[組織單位] 欄位可以用來區別組織內的不同部門，例如「網際網路安全性單位」或「人力資源」。</span><span class="sxs-lookup"><span data-stu-id="a5f69-117">The Organizational Unit field can be used to differentiate between different divisions within an organization, for example "Internet Security Unit" or "Human Resources."</span></span> <span data-ttu-id="a5f69-118">您也可以使用此欄位來指定 DBA (執行商務為 .。。) 值。</span><span class="sxs-lookup"><span data-stu-id="a5f69-118">This field is also recommended to be used for specifying a DBA (Doing Business As...) value.</span></span>                                                                                           |
| <span data-ttu-id="a5f69-119">位置</span><span class="sxs-lookup"><span data-stu-id="a5f69-119">Locality</span></span>            | <span data-ttu-id="a5f69-120">[位置] 欄位代表組織所在的城市。</span><span class="sxs-lookup"><span data-stu-id="a5f69-120">The Locality field denotes the city that the organization resides in.</span></span> <span data-ttu-id="a5f69-121">如果組織只有本機的位置，藉由在麻塞諸塞州的州康橋城市的城市職員註冊商務授權，[位置] 欄位必須包含康橋。</span><span class="sxs-lookup"><span data-stu-id="a5f69-121">If the organization has local standing only, by virtue of having a business license registered with the City Clerk for the City of Cambridge in the State of Massachusetts, then the Locality field must contain Cambridge.</span></span>                                                                |
| <span data-ttu-id="a5f69-122">省/市</span><span class="sxs-lookup"><span data-stu-id="a5f69-122">State or Province</span></span>   | <span data-ttu-id="a5f69-123">[省份] 欄位會指定組織實際所在的位置。</span><span class="sxs-lookup"><span data-stu-id="a5f69-123">The State or Province field specifies where the organization is physically located.</span></span> <span data-ttu-id="a5f69-124">如果您的組織已併入特拉華，但是有 DBA (將企業做為 .。。在加州內 ) ，請使用加州。</span><span class="sxs-lookup"><span data-stu-id="a5f69-124">If your organization is incorporated in Delaware but has a DBA (Doing Business As...) within California, use California.</span></span> <span data-ttu-id="a5f69-125">[省份] 欄位不應為縮寫欄位。</span><span class="sxs-lookup"><span data-stu-id="a5f69-125">The State or Province field should not be an abbreviated field.</span></span> <span data-ttu-id="a5f69-126">例如，"CA" 不是有效的狀態名稱。</span><span class="sxs-lookup"><span data-stu-id="a5f69-126">For example, "CA" is not a valid state name.</span></span> <span data-ttu-id="a5f69-127">「加州」是正確的狀態名稱。</span><span class="sxs-lookup"><span data-stu-id="a5f69-127">"California" is the proper state name.</span></span> |
| <span data-ttu-id="a5f69-128">國家/區域</span><span class="sxs-lookup"><span data-stu-id="a5f69-128">Country/region</span></span>      | <span data-ttu-id="a5f69-129">X.500 [*命名配置*](../secgloss/x-gly.md) 標準需要2個字元的國家/地區代碼。</span><span class="sxs-lookup"><span data-stu-id="a5f69-129">The [*X.500*](../secgloss/x-gly.md) Naming Scheme standard requires a 2-character country/region code.</span></span> <span data-ttu-id="a5f69-130">美國的國家/地區代碼是 US;加拿大的國家/地區代碼為 CA。</span><span class="sxs-lookup"><span data-stu-id="a5f69-130">The country/region code for the United States is US; the country/region code for Canada is CA.</span></span>                                                                                                                          |



 

## <a name="related-topics"></a><span data-ttu-id="a5f69-131">相關主題</span><span class="sxs-lookup"><span data-stu-id="a5f69-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a5f69-132">名稱屬性</span><span class="sxs-lookup"><span data-stu-id="a5f69-132">Name Properties</span></span>](name-properties.md)
</dt> </dl>

 

 
