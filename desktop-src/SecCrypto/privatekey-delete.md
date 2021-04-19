---
description: 刪除 PrivateKey 物件所參考的私用金鑰容器。
ms.assetid: 80bbe46b-1ec5-4d47-82b0-5a3177f86389
title: PrivateKey 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PrivateKey.Delete
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: dc5778e631abba9eb8cf122ddb99a4692c988f4b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993974"
---
# <a name="privatekeydelete-method"></a><span data-ttu-id="05b1e-103">PrivateKey 方法</span><span class="sxs-lookup"><span data-stu-id="05b1e-103">PrivateKey.Delete method</span></span>

<span data-ttu-id="05b1e-104">\[**Delete** 方法可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="05b1e-104">\[The **Delete** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="05b1e-105">請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509Certificate2. PrivateKey 屬性**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1)。\]</span><span class="sxs-lookup"><span data-stu-id="05b1e-105">Instead, use the [**X509Certificate2.PrivateKey Property**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="05b1e-106">**Delete** 方法會刪除 [**PrivateKey**](privatekey.md)物件所參考的私用金鑰容器。</span><span class="sxs-lookup"><span data-stu-id="05b1e-106">The **Delete** method deletes the private key container referenced by the [**PrivateKey**](privatekey.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="05b1e-107">語法</span><span class="sxs-lookup"><span data-stu-id="05b1e-107">Syntax</span></span>


```VB
PrivateKey.Delete()
```



## <a name="parameters"></a><span data-ttu-id="05b1e-108">參數</span><span class="sxs-lookup"><span data-stu-id="05b1e-108">Parameters</span></span>

<span data-ttu-id="05b1e-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="05b1e-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="05b1e-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="05b1e-110">Return value</span></span>

<span data-ttu-id="05b1e-111">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="05b1e-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="05b1e-112">備註</span><span class="sxs-lookup"><span data-stu-id="05b1e-112">Remarks</span></span>

> [!IMPORTANT]
> <span data-ttu-id="05b1e-113">這個方法會刪除 [**PrivateKey**](privatekey.md) 物件所參考的私密金鑰容器，以及容器中的所有私密金鑰。</span><span class="sxs-lookup"><span data-stu-id="05b1e-113">This method deletes the private key container referenced by the [**PrivateKey**](privatekey.md) object as well as all private keys in the container.</span></span> <span data-ttu-id="05b1e-114">使用對應至已刪除私密金鑰的公開金鑰加密的任何事物，將無法再解密。</span><span class="sxs-lookup"><span data-stu-id="05b1e-114">Anything encrypted using the public keys corresponding to the deleted private keys will no longer be able to be decrypted.</span></span>

 

<span data-ttu-id="05b1e-115">\_ \_ \_ 從 web 應用程式編寫腳本時，此方法不允許引發 CAPICOM E。</span><span class="sxs-lookup"><span data-stu-id="05b1e-115">This method raises CAPICOM\_E\_NOT\_ALLOWED when it is scripted from a web-based application.</span></span>

## <a name="requirements"></a><span data-ttu-id="05b1e-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="05b1e-116">Requirements</span></span>



| <span data-ttu-id="05b1e-117">需求</span><span class="sxs-lookup"><span data-stu-id="05b1e-117">Requirement</span></span> | <span data-ttu-id="05b1e-118">值</span><span class="sxs-lookup"><span data-stu-id="05b1e-118">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="05b1e-119">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="05b1e-119">Redistributable</span></span><br/> | <span data-ttu-id="05b1e-120">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="05b1e-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="05b1e-121">DLL</span><span class="sxs-lookup"><span data-stu-id="05b1e-121">DLL</span></span><br/>             | <dl> <span data-ttu-id="05b1e-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="05b1e-122"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
