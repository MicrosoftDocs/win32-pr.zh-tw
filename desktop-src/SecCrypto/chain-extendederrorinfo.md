---
description: 傳回字串，其中包含有關已編制索引之專案的其他錯誤資訊。
ms.assetid: 4f0d5289-c414-4e2b-b612-be8ce1d98b12
title: IChain2：： ExtendedErrorInfo 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Chain.ExtendedErrorInfo
- IChain2.ExtendedErrorInfo
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: f8a7840d0f54ea7e93ad9998d5e8772a2ae411f2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994139"
---
# <a name="ichain2extendederrorinfo-method"></a><span data-ttu-id="4b703-103">IChain2：： ExtendedErrorInfo 方法</span><span class="sxs-lookup"><span data-stu-id="4b703-103">IChain2::ExtendedErrorInfo method</span></span>

<span data-ttu-id="4b703-104">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="4b703-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="4b703-105">請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509Chain 類別**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1)。\]</span><span class="sxs-lookup"><span data-stu-id="4b703-105">Instead, use the [**X509Chain Class**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="4b703-106">**ExtendedErrorInfo** 方法會傳回字串，其中包含有關已編制索引之專案的其他錯誤資訊。</span><span class="sxs-lookup"><span data-stu-id="4b703-106">The **ExtendedErrorInfo** method returns a string that contains additional error information about the indexed entry.</span></span>

<span data-ttu-id="4b703-107">此方法是在 CAPICOM 2.0 中引進。</span><span class="sxs-lookup"><span data-stu-id="4b703-107">This method is introduced in CAPICOM 2.0.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b703-108">語法</span><span class="sxs-lookup"><span data-stu-id="4b703-108">Syntax</span></span>


```VB
Chain.ExtendedErrorInfo( _
  [ ByVal Index ] _
)
```



## <a name="parameters"></a><span data-ttu-id="4b703-109">參數</span><span class="sxs-lookup"><span data-stu-id="4b703-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4b703-110">*索引* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="4b703-110">*Index* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4b703-111">**Long** ，代表專案的索引。</span><span class="sxs-lookup"><span data-stu-id="4b703-111">A **Long** representing the index of the entry.</span></span> <span data-ttu-id="4b703-112">預設值為1，這會在鏈中傳回終端憑證的錯誤資訊。</span><span class="sxs-lookup"><span data-stu-id="4b703-112">The default value is 1, which returns error information for the end certificate in the chain.</span></span> <span data-ttu-id="4b703-113">Certificate **。 Count** 會傳回有關鏈根憑證的資訊。</span><span class="sxs-lookup"><span data-stu-id="4b703-113">**Certificates.Count** returns information about the root certificate of the chain.</span></span> <span data-ttu-id="4b703-114">0會傳回整個鏈的延伸錯誤資訊。</span><span class="sxs-lookup"><span data-stu-id="4b703-114">0 returns extended error information for the entire chain.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4b703-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="4b703-115">Return value</span></span>

<span data-ttu-id="4b703-116">字串，包含擴充的錯誤資訊。</span><span class="sxs-lookup"><span data-stu-id="4b703-116">A string that contains the extended error information.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b703-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="4b703-117">Requirements</span></span>



| <span data-ttu-id="4b703-118">需求</span><span class="sxs-lookup"><span data-stu-id="4b703-118">Requirement</span></span> | <span data-ttu-id="4b703-119">值</span><span class="sxs-lookup"><span data-stu-id="4b703-119">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4b703-120">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="4b703-120">End of client support</span></span><br/> | <span data-ttu-id="4b703-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4b703-121">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="4b703-122">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="4b703-122">End of server support</span></span><br/> | <span data-ttu-id="4b703-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4b703-123">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="4b703-124">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="4b703-124">Redistributable</span></span><br/>       | <span data-ttu-id="4b703-125">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="4b703-125">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="4b703-126">DLL</span><span class="sxs-lookup"><span data-stu-id="4b703-126">DLL</span></span><br/>                   | <dl> <span data-ttu-id="4b703-127"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4b703-127"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4b703-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4b703-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b703-129">**鏈**</span><span class="sxs-lookup"><span data-stu-id="4b703-129">**Chain**</span></span>](chain.md)
</dt> </dl>

 

 
