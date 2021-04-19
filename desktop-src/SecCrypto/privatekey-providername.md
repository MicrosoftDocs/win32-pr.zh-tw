---
description: 抓取 (CSP) 的密碼編譯服務提供者的名稱。
ms.assetid: b06d2839-0eaa-4f3f-99f7-d77e001fe4ea
title: PrivateKey. ProviderName 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PrivateKey.ProviderName
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 528117db072b80ab6d9203b8b2fc2786175499ae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990819"
---
# <a name="privatekeyprovidername-property"></a><span data-ttu-id="4fcde-103">PrivateKey. ProviderName 屬性</span><span class="sxs-lookup"><span data-stu-id="4fcde-103">PrivateKey.ProviderName property</span></span>

<span data-ttu-id="4fcde-104">\[[ **ProviderName** ] 屬性可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="4fcde-104">\[The **ProviderName** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="4fcde-105">請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509Certificate2. PrivateKey 屬性**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1)。\]</span><span class="sxs-lookup"><span data-stu-id="4fcde-105">Instead, use the [**X509Certificate2.PrivateKey Property**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="4fcde-106">**ProviderName** 屬性會抓取 (CSP) 的 [*密碼編譯服務提供者*](../secgloss/c-gly.md)的名稱。</span><span class="sxs-lookup"><span data-stu-id="4fcde-106">The **ProviderName** property retrieves the name of the [*cryptographic service provider*](../secgloss/c-gly.md) (CSP).</span></span>

## <a name="syntax"></a><span data-ttu-id="4fcde-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="4fcde-107">Syntax</span></span>


```VB
PrivateKey.ProviderName As String
```



## <a name="property-value"></a><span data-ttu-id="4fcde-108">屬性值</span><span class="sxs-lookup"><span data-stu-id="4fcde-108">Property value</span></span>

<span data-ttu-id="4fcde-109">包含 CSP 名稱的字串。</span><span class="sxs-lookup"><span data-stu-id="4fcde-109">A string that contains the name of the CSP.</span></span>

## <a name="requirements"></a><span data-ttu-id="4fcde-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="4fcde-110">Requirements</span></span>



| <span data-ttu-id="4fcde-111">需求</span><span class="sxs-lookup"><span data-stu-id="4fcde-111">Requirement</span></span> | <span data-ttu-id="4fcde-112">值</span><span class="sxs-lookup"><span data-stu-id="4fcde-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4fcde-113">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="4fcde-113">Redistributable</span></span><br/> | <span data-ttu-id="4fcde-114">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="4fcde-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="4fcde-115">DLL</span><span class="sxs-lookup"><span data-stu-id="4fcde-115">DLL</span></span><br/>             | <dl> <span data-ttu-id="4fcde-116"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4fcde-116"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4fcde-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4fcde-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4fcde-118">**PrivateKey**</span><span class="sxs-lookup"><span data-stu-id="4fcde-118">**PrivateKey**</span></span>](privatekey.md)
</dt> </dl>

 

 
