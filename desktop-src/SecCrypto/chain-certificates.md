---
description: '[憑證] 屬性會抓取代表鏈中憑證的憑證集合。 這是預設屬性。'
ms.assetid: c3e6953f-35e5-469a-a1aa-e3a4ebe21ac3
title: IChain2：： certificate 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IChain2.Certificates
- IChain2.get_Certificates
- IChain.Certificates
- IChain.get_Certificates
- Chain.Certificates
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: a166f1d0dfa7f027058be65c3371d5c055cdb7bd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990050"
---
# <a name="ichain2certificates-property"></a><span data-ttu-id="05daa-104">IChain2：： certificate 屬性</span><span class="sxs-lookup"><span data-stu-id="05daa-104">IChain2::Certificates property</span></span>

<span data-ttu-id="05daa-105">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="05daa-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="05daa-106">請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509Chain 類別**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1)。\]</span><span class="sxs-lookup"><span data-stu-id="05daa-106">Instead, use the [**X509Chain Class**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="05daa-107">[ **憑證** ] 屬性會抓取代表鏈中憑證的 [**憑證**](certificates.md) 集合。</span><span class="sxs-lookup"><span data-stu-id="05daa-107">The **Certificates** property retrieves a [**Certificates**](certificates.md) collection that represents the certificates in the chain.</span></span> <span data-ttu-id="05daa-108">這是預設屬性。</span><span class="sxs-lookup"><span data-stu-id="05daa-108">This is the default property.</span></span>

<span data-ttu-id="05daa-109">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="05daa-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="05daa-110">語法</span><span class="sxs-lookup"><span data-stu-id="05daa-110">Syntax</span></span>


```VB
Chain.Certificates As Certificates
```



## <a name="property-value"></a><span data-ttu-id="05daa-111">屬性值</span><span class="sxs-lookup"><span data-stu-id="05daa-111">Property value</span></span>

<span data-ttu-id="05daa-112">用來取得鏈中每個憑證相關資訊的 [**憑證**](certificates.md) 集合。</span><span class="sxs-lookup"><span data-stu-id="05daa-112">A [**Certificates**](certificates.md) collection that is used to retrieve information about each certificate in the chain.</span></span> <span data-ttu-id="05daa-113">傳回之集合中的第一個憑證（certificate **. Item** (1) ）是鏈的最終憑證。</span><span class="sxs-lookup"><span data-stu-id="05daa-113">The first certificate in the returned collection, **Certificates.Item**(1), is the end certificate of the chain.</span></span> <span data-ttu-id="05daa-114">集合中的最後一個憑證（certificate **.** (Certificate **. Count**) ，是此鏈的 [*根憑證*](../secgloss/r-gly.md) 。</span><span class="sxs-lookup"><span data-stu-id="05daa-114">The last certificate in the collection, **Certificates.Item**(**Certificates.Count**), is the [*root certificate*](../secgloss/r-gly.md) of the chain.</span></span>

## <a name="requirements"></a><span data-ttu-id="05daa-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="05daa-115">Requirements</span></span>



| <span data-ttu-id="05daa-116">需求</span><span class="sxs-lookup"><span data-stu-id="05daa-116">Requirement</span></span> | <span data-ttu-id="05daa-117">值</span><span class="sxs-lookup"><span data-stu-id="05daa-117">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="05daa-118">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="05daa-118">End of client support</span></span><br/> | <span data-ttu-id="05daa-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="05daa-119">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="05daa-120">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="05daa-120">End of server support</span></span><br/> | <span data-ttu-id="05daa-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="05daa-121">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="05daa-122">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="05daa-122">Redistributable</span></span><br/>       | <span data-ttu-id="05daa-123">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="05daa-123">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="05daa-124">DLL</span><span class="sxs-lookup"><span data-stu-id="05daa-124">DLL</span></span><br/>                   | <dl> <span data-ttu-id="05daa-125"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="05daa-125"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
