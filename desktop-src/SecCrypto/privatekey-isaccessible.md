---
description: 傳回布林值，指出是否可存取私密金鑰。
ms.assetid: ee5e89af-745e-4a4d-9943-fecbaee5d3e3
title: PrivateKey. IsAccessible 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PrivateKey.IsAccessible
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 9997fad702ab1eddbf4c60fa2304df8185ef4c63
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976164"
---
# <a name="privatekeyisaccessible-method"></a><span data-ttu-id="9175f-103">PrivateKey. IsAccessible 方法</span><span class="sxs-lookup"><span data-stu-id="9175f-103">PrivateKey.IsAccessible method</span></span>

<span data-ttu-id="9175f-104">\[**IsAccessible** 方法可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="9175f-104">\[The **IsAccessible** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="9175f-105">請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509Certificate2. PrivateKey 屬性**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1)。\]</span><span class="sxs-lookup"><span data-stu-id="9175f-105">Instead, use the [**X509Certificate2.PrivateKey Property**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="9175f-106">**IsAccessible** 方法會傳回布林值，指出是否可存取私密金鑰。</span><span class="sxs-lookup"><span data-stu-id="9175f-106">The **IsAccessible** method returns a Boolean value that indicates whether the private key is accessible.</span></span>

## <a name="syntax"></a><span data-ttu-id="9175f-107">語法</span><span class="sxs-lookup"><span data-stu-id="9175f-107">Syntax</span></span>


```VB
PrivateKey.IsAccessible()
```



## <a name="parameters"></a><span data-ttu-id="9175f-108">參數</span><span class="sxs-lookup"><span data-stu-id="9175f-108">Parameters</span></span>

<span data-ttu-id="9175f-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="9175f-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9175f-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="9175f-110">Return value</span></span>

<span data-ttu-id="9175f-111">若為 true，則可存取私密金鑰。</span><span class="sxs-lookup"><span data-stu-id="9175f-111">If true, the private key is accessible.</span></span>

## <a name="remarks"></a><span data-ttu-id="9175f-112">備註</span><span class="sxs-lookup"><span data-stu-id="9175f-112">Remarks</span></span>

<span data-ttu-id="9175f-113">此方法的傳回值相依于 (CSP) 使用的 [*密碼編譯服務提供者*](../secgloss/c-gly.md) 。</span><span class="sxs-lookup"><span data-stu-id="9175f-113">The return value of this method is dependent on the [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) used.</span></span> <span data-ttu-id="9175f-114">如果使用 Microsoft CSP，則這個方法會傳回信任的值。</span><span class="sxs-lookup"><span data-stu-id="9175f-114">This method will return a trustworthy value if a Microsoft CSP is used.</span></span> <span data-ttu-id="9175f-115">如果 CSP 不是 Microsoft CSP，則傳回值無法信任為正確。</span><span class="sxs-lookup"><span data-stu-id="9175f-115">If the CSP is not a Microsoft CSP, the return value cannot be trusted to be accurate.</span></span>

## <a name="requirements"></a><span data-ttu-id="9175f-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="9175f-116">Requirements</span></span>



| <span data-ttu-id="9175f-117">需求</span><span class="sxs-lookup"><span data-stu-id="9175f-117">Requirement</span></span> | <span data-ttu-id="9175f-118">值</span><span class="sxs-lookup"><span data-stu-id="9175f-118">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9175f-119">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="9175f-119">Redistributable</span></span><br/> | <span data-ttu-id="9175f-120">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="9175f-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="9175f-121">DLL</span><span class="sxs-lookup"><span data-stu-id="9175f-121">DLL</span></span><br/>             | <dl> <span data-ttu-id="9175f-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9175f-122"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9175f-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9175f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9175f-124">**PrivateKey**</span><span class="sxs-lookup"><span data-stu-id="9175f-124">**PrivateKey**</span></span>](privatekey.md)
</dt> </dl>

 

 
