---
description: 傳回 Oid 集合，這個集合表示對鏈有效的憑證原則 Oid。
ms.assetid: 18200003-f4f1-4cf3-af9a-bc223151ff68
title: IChain2：： CertificatePolicies 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Chain.CertificatePolicies
- IChain2.CertificatePolicies
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e37abce9ea1aec5eb8adaf1d8eceeb3fac284fa3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993932"
---
# <a name="ichain2certificatepolicies-method"></a><span data-ttu-id="e6d3e-103">IChain2：： CertificatePolicies 方法</span><span class="sxs-lookup"><span data-stu-id="e6d3e-103">IChain2::CertificatePolicies method</span></span>

<span data-ttu-id="e6d3e-104">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="e6d3e-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="e6d3e-105">請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509Chain 類別**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1)。\]</span><span class="sxs-lookup"><span data-stu-id="e6d3e-105">Instead, use the [**X509Chain Class**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="e6d3e-106">**CertificatePolicies** 方法會傳回 [**oid**](oids.md)集合，以代表對鏈有效的憑證原則 oid。</span><span class="sxs-lookup"><span data-stu-id="e6d3e-106">The **CertificatePolicies** method returns an [**OIDs**](oids.md) collection that represents the certificate policy OIDs valid for the chain.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6d3e-107">語法</span><span class="sxs-lookup"><span data-stu-id="e6d3e-107">Syntax</span></span>


```VB
Chain.CertificatePolicies()
```



## <a name="parameters"></a><span data-ttu-id="e6d3e-108">參數</span><span class="sxs-lookup"><span data-stu-id="e6d3e-108">Parameters</span></span>

<span data-ttu-id="e6d3e-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="e6d3e-109">This method has no parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6d3e-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="e6d3e-110">Requirements</span></span>



| <span data-ttu-id="e6d3e-111">需求</span><span class="sxs-lookup"><span data-stu-id="e6d3e-111">Requirement</span></span> | <span data-ttu-id="e6d3e-112">值</span><span class="sxs-lookup"><span data-stu-id="e6d3e-112">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e6d3e-113">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="e6d3e-113">End of client support</span></span><br/> | <span data-ttu-id="e6d3e-114">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e6d3e-114">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="e6d3e-115">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="e6d3e-115">End of server support</span></span><br/> | <span data-ttu-id="e6d3e-116">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e6d3e-116">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="e6d3e-117">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="e6d3e-117">Redistributable</span></span><br/>       | <span data-ttu-id="e6d3e-118">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="e6d3e-118">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="e6d3e-119">DLL</span><span class="sxs-lookup"><span data-stu-id="e6d3e-119">DLL</span></span><br/>                   | <dl> <span data-ttu-id="e6d3e-120"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e6d3e-120"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
