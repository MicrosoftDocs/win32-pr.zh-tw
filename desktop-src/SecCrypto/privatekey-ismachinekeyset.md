---
description: 傳回布林值，指出私密金鑰是否屬於電腦金鑰集。
ms.assetid: ea13ba68-30ae-4aa4-b490-29fd4542c621
title: PrivateKey. IsMachineKeyset 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PrivateKey.IsMachineKeyset
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 2a42e3f932b8294d9671b7901437151d9fbbe5a8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993249"
---
# <a name="privatekeyismachinekeyset-method"></a><span data-ttu-id="6434c-103">PrivateKey. IsMachineKeyset 方法</span><span class="sxs-lookup"><span data-stu-id="6434c-103">PrivateKey.IsMachineKeyset method</span></span>

<span data-ttu-id="6434c-104">\[**IsMachineKeyset** 方法可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="6434c-104">\[The **IsMachineKeyset** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="6434c-105">請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509Certificate2. PrivateKey 屬性**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1)。\]</span><span class="sxs-lookup"><span data-stu-id="6434c-105">Instead, use the [**X509Certificate2.PrivateKey Property**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="6434c-106">**IsMachineKeyset** 方法會傳回布林值，指出私密金鑰是否屬於電腦金鑰集。</span><span class="sxs-lookup"><span data-stu-id="6434c-106">The **IsMachineKeyset** method returns a Boolean value that indicates whether the private key belongs to a machine key set.</span></span>

## <a name="syntax"></a><span data-ttu-id="6434c-107">語法</span><span class="sxs-lookup"><span data-stu-id="6434c-107">Syntax</span></span>


```VB
PrivateKey.IsMachineKeyset()
```



## <a name="parameters"></a><span data-ttu-id="6434c-108">參數</span><span class="sxs-lookup"><span data-stu-id="6434c-108">Parameters</span></span>

<span data-ttu-id="6434c-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="6434c-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6434c-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="6434c-110">Return value</span></span>

<span data-ttu-id="6434c-111">若為 true，則私密金鑰屬於電腦金鑰集。</span><span class="sxs-lookup"><span data-stu-id="6434c-111">If true, the private key belongs to a machine key set.</span></span>

## <a name="remarks"></a><span data-ttu-id="6434c-112">備註</span><span class="sxs-lookup"><span data-stu-id="6434c-112">Remarks</span></span>

<span data-ttu-id="6434c-113">此方法的傳回值相依于 (CSP) 使用的 [*密碼編譯服務提供者*](../secgloss/c-gly.md) 。</span><span class="sxs-lookup"><span data-stu-id="6434c-113">The return value of this method is dependent on the [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) used.</span></span> <span data-ttu-id="6434c-114">如果使用 Microsoft CSP，則這個方法會傳回信任的值。</span><span class="sxs-lookup"><span data-stu-id="6434c-114">This method will return a trustworthy value if a Microsoft CSP is used.</span></span> <span data-ttu-id="6434c-115">如果 CSP 不是 Microsoft CSP，則傳回值無法信任為正確。</span><span class="sxs-lookup"><span data-stu-id="6434c-115">If the CSP is not a Microsoft CSP, the return value cannot be trusted to be accurate.</span></span>

## <a name="requirements"></a><span data-ttu-id="6434c-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="6434c-116">Requirements</span></span>



| <span data-ttu-id="6434c-117">需求</span><span class="sxs-lookup"><span data-stu-id="6434c-117">Requirement</span></span> | <span data-ttu-id="6434c-118">值</span><span class="sxs-lookup"><span data-stu-id="6434c-118">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6434c-119">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="6434c-119">Redistributable</span></span><br/> | <span data-ttu-id="6434c-120">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="6434c-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="6434c-121">DLL</span><span class="sxs-lookup"><span data-stu-id="6434c-121">DLL</span></span><br/>             | <dl> <span data-ttu-id="6434c-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6434c-122"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6434c-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6434c-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6434c-124">**PrivateKey**</span><span class="sxs-lookup"><span data-stu-id="6434c-124">**PrivateKey**</span></span>](privatekey.md)
</dt> </dl>

 

 
