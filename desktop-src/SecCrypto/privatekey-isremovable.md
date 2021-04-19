---
description: 傳回布林值，指出私密金鑰是否位於卸除式存放裝置中。
ms.assetid: 9371d7cf-65b2-4c0f-a387-195a058d6a8b
title: PrivateKey. IsRemovable 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PrivateKey.IsRemovable
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 6684d40302746a736701b824685a54faeff5354a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996411"
---
# <a name="privatekeyisremovable-method"></a><span data-ttu-id="a512f-103">PrivateKey. IsRemovable 方法</span><span class="sxs-lookup"><span data-stu-id="a512f-103">PrivateKey.IsRemovable method</span></span>

<span data-ttu-id="a512f-104">\[**IsRemovable** 方法可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="a512f-104">\[The **IsRemovable** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="a512f-105">請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509Certificate2. PrivateKey 屬性**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1)。\]</span><span class="sxs-lookup"><span data-stu-id="a512f-105">Instead, use the [**X509Certificate2.PrivateKey Property**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="a512f-106">**IsRemovable** 方法會傳回布林值，指出私密金鑰是否位於卸除式存放裝置中。</span><span class="sxs-lookup"><span data-stu-id="a512f-106">The **IsRemovable** method returns a Boolean value that indicates whether the private key is in removable storage.</span></span>

## <a name="syntax"></a><span data-ttu-id="a512f-107">語法</span><span class="sxs-lookup"><span data-stu-id="a512f-107">Syntax</span></span>


```VB
PrivateKey.IsRemovable()
```



## <a name="parameters"></a><span data-ttu-id="a512f-108">參數</span><span class="sxs-lookup"><span data-stu-id="a512f-108">Parameters</span></span>

<span data-ttu-id="a512f-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="a512f-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a512f-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="a512f-110">Return value</span></span>

<span data-ttu-id="a512f-111">若為 true，則私密金鑰位於卸除式存放裝置中。</span><span class="sxs-lookup"><span data-stu-id="a512f-111">If true, the private key is in removable storage.</span></span>

## <a name="remarks"></a><span data-ttu-id="a512f-112">備註</span><span class="sxs-lookup"><span data-stu-id="a512f-112">Remarks</span></span>

<span data-ttu-id="a512f-113">此方法的傳回值相依于 (CSP) 使用的 [*密碼編譯服務提供者*](../secgloss/c-gly.md) 。</span><span class="sxs-lookup"><span data-stu-id="a512f-113">The return value of this method is dependent on the [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) used.</span></span> <span data-ttu-id="a512f-114">如果使用 Microsoft CSP，則這個方法會傳回信任的值。</span><span class="sxs-lookup"><span data-stu-id="a512f-114">This method will return a trustworthy value if a Microsoft CSP is used.</span></span> <span data-ttu-id="a512f-115">如果 CSP 不是 Microsoft CSP，則傳回值無法信任為正確。</span><span class="sxs-lookup"><span data-stu-id="a512f-115">If the CSP is not a Microsoft CSP, the return value cannot be trusted to be accurate.</span></span>

## <a name="requirements"></a><span data-ttu-id="a512f-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="a512f-116">Requirements</span></span>



| <span data-ttu-id="a512f-117">需求</span><span class="sxs-lookup"><span data-stu-id="a512f-117">Requirement</span></span> | <span data-ttu-id="a512f-118">值</span><span class="sxs-lookup"><span data-stu-id="a512f-118">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a512f-119">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="a512f-119">Redistributable</span></span><br/> | <span data-ttu-id="a512f-120">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="a512f-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="a512f-121">DLL</span><span class="sxs-lookup"><span data-stu-id="a512f-121">DLL</span></span><br/>             | <dl> <span data-ttu-id="a512f-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a512f-122"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a512f-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a512f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a512f-124">**PrivateKey**</span><span class="sxs-lookup"><span data-stu-id="a512f-124">**PrivateKey**</span></span>](privatekey.md)
</dt> </dl>

 

 
