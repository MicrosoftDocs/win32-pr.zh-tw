---
description: 抓取私密金鑰容器名稱。
ms.assetid: ecc0b4ba-4e2b-49e9-8358-8c498e1d6ae0
title: PrivateKey 容器屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PrivateKey.ContainerName
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 0e9506b9390dc8b09e6326232e53c72d01749f34
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976286"
---
# <a name="privatekeycontainername-property"></a><span data-ttu-id="1e9e9-103">PrivateKey 容器屬性</span><span class="sxs-lookup"><span data-stu-id="1e9e9-103">PrivateKey.ContainerName property</span></span>

<span data-ttu-id="1e9e9-104">\[[ **容器** ] 屬性可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="1e9e9-104">\[The **ContainerName** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="1e9e9-105">請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509Certificate2. PrivateKey 屬性**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1)。\]</span><span class="sxs-lookup"><span data-stu-id="1e9e9-105">Instead, use the [**X509Certificate2.PrivateKey Property**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="1e9e9-106">**容器** 屬性會抓取私密金鑰容器名稱。</span><span class="sxs-lookup"><span data-stu-id="1e9e9-106">The **ContainerName** property retrieves the private key container name.</span></span> <span data-ttu-id="1e9e9-107">這是預設屬性。</span><span class="sxs-lookup"><span data-stu-id="1e9e9-107">This is the default property.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e9e9-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="1e9e9-108">Syntax</span></span>


```VB
PrivateKey.ContainerName As String
```



## <a name="property-value"></a><span data-ttu-id="1e9e9-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="1e9e9-109">Property value</span></span>

<span data-ttu-id="1e9e9-110">包含私密金鑰容器名稱的字串。</span><span class="sxs-lookup"><span data-stu-id="1e9e9-110">A string that contains the private key container name.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e9e9-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="1e9e9-111">Requirements</span></span>



| <span data-ttu-id="1e9e9-112">需求</span><span class="sxs-lookup"><span data-stu-id="1e9e9-112">Requirement</span></span> | <span data-ttu-id="1e9e9-113">值</span><span class="sxs-lookup"><span data-stu-id="1e9e9-113">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1e9e9-114">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="1e9e9-114">Redistributable</span></span><br/> | <span data-ttu-id="1e9e9-115">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="1e9e9-115">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="1e9e9-116">DLL</span><span class="sxs-lookup"><span data-stu-id="1e9e9-116">DLL</span></span><br/>             | <dl> <span data-ttu-id="1e9e9-117"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1e9e9-117"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e9e9-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1e9e9-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e9e9-119">**PrivateKey**</span><span class="sxs-lookup"><span data-stu-id="1e9e9-119">**PrivateKey**</span></span>](privatekey.md)
</dt> </dl>

 

 
