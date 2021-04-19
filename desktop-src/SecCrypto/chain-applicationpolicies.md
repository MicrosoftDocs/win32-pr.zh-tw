---
description: 傳回 Oid 集合，這個集合表示對鏈有效的應用程式原則 Oid。
ms.assetid: 4e4a7dce-5004-4b80-b132-3cdc0c048cde
title: IChain2：： ApplicationPolicies 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Chain.ApplicationPolicies
- IChain2.ApplicationPolicies
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: a90eb7a493bfe81f5c4a38f773b0307380002b6b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000993"
---
# <a name="ichain2applicationpolicies-method"></a><span data-ttu-id="c8366-103">IChain2：： ApplicationPolicies 方法</span><span class="sxs-lookup"><span data-stu-id="c8366-103">IChain2::ApplicationPolicies method</span></span>

<span data-ttu-id="c8366-104">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="c8366-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="c8366-105">請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509Chain 類別**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1)。\]</span><span class="sxs-lookup"><span data-stu-id="c8366-105">Instead, use the [**X509Chain Class**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="c8366-106">**ApplicationPolicies** 方法會傳回 [**oid**](oids.md)集合，以代表對鏈有效的應用程式原則 oid。</span><span class="sxs-lookup"><span data-stu-id="c8366-106">The **ApplicationPolicies** method returns an [**OIDs**](oids.md) collection that represents the application policy OIDs valid for the chain.</span></span>

<span data-ttu-id="c8366-107">此方法是在 CAPICOM 2.0 中引進。</span><span class="sxs-lookup"><span data-stu-id="c8366-107">This method is introduced in CAPICOM 2.0.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8366-108">語法</span><span class="sxs-lookup"><span data-stu-id="c8366-108">Syntax</span></span>


```VB
Chain.ApplicationPolicies()
```



## <a name="parameters"></a><span data-ttu-id="c8366-109">參數</span><span class="sxs-lookup"><span data-stu-id="c8366-109">Parameters</span></span>

<span data-ttu-id="c8366-110">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="c8366-110">This method has no parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8366-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="c8366-111">Requirements</span></span>



| <span data-ttu-id="c8366-112">需求</span><span class="sxs-lookup"><span data-stu-id="c8366-112">Requirement</span></span> | <span data-ttu-id="c8366-113">值</span><span class="sxs-lookup"><span data-stu-id="c8366-113">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c8366-114">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="c8366-114">End of client support</span></span><br/> | <span data-ttu-id="c8366-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c8366-115">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="c8366-116">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="c8366-116">End of server support</span></span><br/> | <span data-ttu-id="c8366-117">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c8366-117">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="c8366-118">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="c8366-118">Redistributable</span></span><br/>       | <span data-ttu-id="c8366-119">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="c8366-119">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="c8366-120">DLL</span><span class="sxs-lookup"><span data-stu-id="c8366-120">DLL</span></span><br/>                   | <dl> <span data-ttu-id="c8366-121"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c8366-121"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
