---
description: 抓取金鑰規格。
ms.assetid: 93c909cb-b1d1-4c2b-a66c-9d3f6dd9b340
title: PrivateKey. KeySpec 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PrivateKey.KeySpec
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: f9d0ba55ca48d5257a038845f84374544b7615b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999635"
---
# <a name="privatekeykeyspec-property"></a><span data-ttu-id="d6a3e-103">PrivateKey. KeySpec 屬性</span><span class="sxs-lookup"><span data-stu-id="d6a3e-103">PrivateKey.KeySpec property</span></span>

<span data-ttu-id="d6a3e-104">\[**KeySpec** 屬性可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="d6a3e-104">\[The **KeySpec** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="d6a3e-105">請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509Certificate2. PrivateKey 屬性**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1)。\]</span><span class="sxs-lookup"><span data-stu-id="d6a3e-105">Instead, use the [**X509Certificate2.PrivateKey Property**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="d6a3e-106">**KeySpec** 屬性會捕獲金鑰規格。</span><span class="sxs-lookup"><span data-stu-id="d6a3e-106">The **KeySpec** property retrieves the key specification.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6a3e-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="d6a3e-107">Syntax</span></span>


```VB
PrivateKey.KeySpec As CAPICOM_KEY_SPEC
```



## <a name="property-value"></a><span data-ttu-id="d6a3e-108">屬性值</span><span class="sxs-lookup"><span data-stu-id="d6a3e-108">Property value</span></span>

<span data-ttu-id="d6a3e-109">表示金鑰規格之 [**CAPICOM \_ 金鑰 \_ 規格**](capicom-key-spec.md) 列舉的值。</span><span class="sxs-lookup"><span data-stu-id="d6a3e-109">A value of the [**CAPICOM\_KEY\_SPEC**](capicom-key-spec.md) enumeration that indicates the key specification.</span></span> <span data-ttu-id="d6a3e-110">下表顯示可能的值。</span><span class="sxs-lookup"><span data-stu-id="d6a3e-110">The following table shows the possible values.</span></span>



| <span data-ttu-id="d6a3e-111">值</span><span class="sxs-lookup"><span data-stu-id="d6a3e-111">Value</span></span>                                                                                                                                                                                                        | <span data-ttu-id="d6a3e-112">意義</span><span class="sxs-lookup"><span data-stu-id="d6a3e-112">Meaning</span></span>                                                    |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <span id="CAPICOM_KEY_SPEC_KEYEXCHANGE"></span><span id="capicom_key_spec_keyexchange"></span><dl> <span data-ttu-id="d6a3e-113"><dt>**CAPICOM \_ 金鑰 \_ 規格 \_ KEYEXCHANGE**</dt></span><span class="sxs-lookup"><span data-stu-id="d6a3e-113"><dt>**CAPICOM\_KEY\_SPEC\_KEYEXCHANGE**</dt></span></span> </dl> | <span data-ttu-id="d6a3e-114">金鑰可用於加密和簽署。</span><span class="sxs-lookup"><span data-stu-id="d6a3e-114">The key can be used for encryption and signing.</span></span><br/> |
| <span id="CAPICOM_KEY_SPEC_SIGNATURE"></span><span id="capicom_key_spec_signature"></span><dl> <span data-ttu-id="d6a3e-115"><dt>**CAPICOM \_ 金鑰 \_ 規格簽章 \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d6a3e-115"><dt>**CAPICOM\_KEY\_SPEC\_SIGNATURE**</dt></span></span> </dl>       | <span data-ttu-id="d6a3e-116">金鑰只能用於簽署。</span><span class="sxs-lookup"><span data-stu-id="d6a3e-116">The key can be used only for signing.</span></span><br/>           |



 

## <a name="requirements"></a><span data-ttu-id="d6a3e-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="d6a3e-117">Requirements</span></span>



| <span data-ttu-id="d6a3e-118">需求</span><span class="sxs-lookup"><span data-stu-id="d6a3e-118">Requirement</span></span> | <span data-ttu-id="d6a3e-119">值</span><span class="sxs-lookup"><span data-stu-id="d6a3e-119">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d6a3e-120">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="d6a3e-120">Redistributable</span></span><br/> | <span data-ttu-id="d6a3e-121">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="d6a3e-121">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="d6a3e-122">DLL</span><span class="sxs-lookup"><span data-stu-id="d6a3e-122">DLL</span></span><br/>             | <dl> <span data-ttu-id="d6a3e-123"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d6a3e-123"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d6a3e-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d6a3e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6a3e-125">**PrivateKey**</span><span class="sxs-lookup"><span data-stu-id="d6a3e-125">**PrivateKey**</span></span>](privatekey.md)
</dt> </dl>

 

 
