---
description: 設定或抓取布林值，指出憑證是否已封存。
ms.assetid: a6526b0e-e76b-4f03-a6ba-9e380e362364
title: Certificate. 封存的屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.Archived
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e1d8cdea3e43bbe10ee87f8f4aa605740a15e6ac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106997754"
---
# <a name="certificatearchived-property"></a><span data-ttu-id="44e30-103">Certificate. 封存的屬性</span><span class="sxs-lookup"><span data-stu-id="44e30-103">Certificate.Archived property</span></span>

<span data-ttu-id="44e30-104">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="44e30-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="44e30-105">請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509Certificate2 類別**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2?view=netcore-3.1)。\]</span><span class="sxs-lookup"><span data-stu-id="44e30-105">Instead, use the [**X509Certificate2 Class**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="44e30-106">封存 **的屬性會** 設定或抓取布林值，指出憑證是否已封存。</span><span class="sxs-lookup"><span data-stu-id="44e30-106">The **Archived** property sets or retrieves a Boolean value that indicates whether the certificate is archived.</span></span>

<span data-ttu-id="44e30-107">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="44e30-107">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="44e30-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="44e30-108">Syntax</span></span>


```VB
Certificate.Archived As Boolean
```



## <a name="property-value"></a><span data-ttu-id="44e30-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="44e30-109">Property value</span></span>

<span data-ttu-id="44e30-110">指出憑證是否已封存的布林值。</span><span class="sxs-lookup"><span data-stu-id="44e30-110">A Boolean value that indicates whether the certificate is archived.</span></span> <span data-ttu-id="44e30-111">若 **為 true**，則表示憑證已封存。</span><span class="sxs-lookup"><span data-stu-id="44e30-111">If **true**, the certificate is archived.</span></span> <span data-ttu-id="44e30-112">請注意，將值從 **false** 變更為 **true** 會封存憑證。</span><span class="sxs-lookup"><span data-stu-id="44e30-112">Note that changing the value from **false** to **true** archives the certificate.</span></span>

## <a name="remarks"></a><span data-ttu-id="44e30-113">備註</span><span class="sxs-lookup"><span data-stu-id="44e30-113">Remarks</span></span>

<span data-ttu-id="44e30-114">\_ \_ \_ 從 web 應用程式編寫腳本時，這個屬性不允許引發 CAPICOM E。</span><span class="sxs-lookup"><span data-stu-id="44e30-114">This property raises CAPICOM\_E\_NOT\_ALLOWED when it is scripted from a web-based application.</span></span>

> [!Note]  
> <span data-ttu-id="44e30-115">憑證管理使用者介面中看不到封存的憑證。</span><span class="sxs-lookup"><span data-stu-id="44e30-115">An archived certificate is not visible in the certificate management user interface.</span></span> <span data-ttu-id="44e30-116">此外，封存的憑證將不會包含在 [**存放區中。**](store-open.md) 除非 \_ \_ \_ \_ 已指定 [CAPICOM 存放區開啟包含封存]，否則會開啟方法。</span><span class="sxs-lookup"><span data-stu-id="44e30-116">Also, archived certificates will not be included in the [**Store.Open**](store-open.md) method unless CAPICOM\_STORE\_OPEN\_INCLUDE\_ARCHIVED is specified.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="44e30-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="44e30-117">Requirements</span></span>



| <span data-ttu-id="44e30-118">需求</span><span class="sxs-lookup"><span data-stu-id="44e30-118">Requirement</span></span> | <span data-ttu-id="44e30-119">值</span><span class="sxs-lookup"><span data-stu-id="44e30-119">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="44e30-120">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="44e30-120">End of client support</span></span><br/> | <span data-ttu-id="44e30-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="44e30-121">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="44e30-122">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="44e30-122">End of server support</span></span><br/> | <span data-ttu-id="44e30-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="44e30-123">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="44e30-124">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="44e30-124">Redistributable</span></span><br/>       | <span data-ttu-id="44e30-125">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="44e30-125">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="44e30-126">DLL</span><span class="sxs-lookup"><span data-stu-id="44e30-126">DLL</span></span><br/>                   | <dl> <span data-ttu-id="44e30-127"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="44e30-127"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
