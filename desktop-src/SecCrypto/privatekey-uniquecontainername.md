---
description: 抓取唯一的私密金鑰容器名稱。
ms.assetid: 2f1315b7-0b12-45d6-8dac-80331bd84ffd
title: PrivateKey. UniqueContainerName 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PrivateKey.UniqueContainerName
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 9db721f8d3cc67bd8ec9252f299bffa6e077f086
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977603"
---
# <a name="privatekeyuniquecontainername-property"></a><span data-ttu-id="ae317-103">PrivateKey. UniqueContainerName 屬性</span><span class="sxs-lookup"><span data-stu-id="ae317-103">PrivateKey.UniqueContainerName property</span></span>

<span data-ttu-id="ae317-104">\[**UniqueContainerName** 屬性可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="ae317-104">\[The **UniqueContainerName** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="ae317-105">請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509Certificate2. PrivateKey 屬性**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1)。\]</span><span class="sxs-lookup"><span data-stu-id="ae317-105">Instead, use the [**X509Certificate2.PrivateKey Property**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="ae317-106">**UniqueContainerName** 屬性會抓取唯一的私密金鑰容器名稱。</span><span class="sxs-lookup"><span data-stu-id="ae317-106">The **UniqueContainerName** property retrieves the unique private key container name.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae317-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="ae317-107">Syntax</span></span>


```VB
PrivateKey.UniqueContainerName As String
```



## <a name="property-value"></a><span data-ttu-id="ae317-108">屬性值</span><span class="sxs-lookup"><span data-stu-id="ae317-108">Property value</span></span>

<span data-ttu-id="ae317-109">包含唯一私用金鑰容器名稱的字串。</span><span class="sxs-lookup"><span data-stu-id="ae317-109">A string that contains the unique private key container name.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae317-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="ae317-110">Requirements</span></span>



| <span data-ttu-id="ae317-111">需求</span><span class="sxs-lookup"><span data-stu-id="ae317-111">Requirement</span></span> | <span data-ttu-id="ae317-112">值</span><span class="sxs-lookup"><span data-stu-id="ae317-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ae317-113">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="ae317-113">Redistributable</span></span><br/> | <span data-ttu-id="ae317-114">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="ae317-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="ae317-115">DLL</span><span class="sxs-lookup"><span data-stu-id="ae317-115">DLL</span></span><br/>             | <dl> <span data-ttu-id="ae317-116"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ae317-116"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ae317-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ae317-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae317-118">**PrivateKey**</span><span class="sxs-lookup"><span data-stu-id="ae317-118">**PrivateKey**</span></span>](privatekey.md)
</dt> </dl>

 

 
