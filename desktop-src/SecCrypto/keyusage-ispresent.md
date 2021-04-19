---
description: 抓取布林值，指出 KeyUsage 延伸是否存在。
ms.assetid: d666049a-4b40-42b6-8c2d-c27a1bb4c48a
title: KeyUsage. IsPresent 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KeyUsage.IsPresent
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: f70754c15a248cda69f93fcab2a0052bd8351261
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106986143"
---
# <a name="keyusageispresent-property"></a><span data-ttu-id="33340-103">KeyUsage. IsPresent 屬性</span><span class="sxs-lookup"><span data-stu-id="33340-103">KeyUsage.IsPresent property</span></span>

<span data-ttu-id="33340-104">\[**IsPresent** 屬性可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="33340-104">\[The **IsPresent** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="33340-105">請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509EnhancedKeyUsageExtension 類別**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1)。\]</span><span class="sxs-lookup"><span data-stu-id="33340-105">Instead, use the [**X509EnhancedKeyUsageExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="33340-106">**IsPresent** 屬性會抓取布林值，指出 [**KeyUsage**](keyusage.md)延伸是否存在。</span><span class="sxs-lookup"><span data-stu-id="33340-106">The **IsPresent** property retrieves a Boolean value that indicates whether the [**KeyUsage**](keyusage.md) extension is present.</span></span>

<span data-ttu-id="33340-107">這個屬性是 [**KeyUsage**](keyusage.md) 物件的預設屬性。</span><span class="sxs-lookup"><span data-stu-id="33340-107">This property is the default property of the [**KeyUsage**](keyusage.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="33340-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="33340-108">Syntax</span></span>


```VB
KeyUsage.IsPresent As Boolean
```



## <a name="property-value"></a><span data-ttu-id="33340-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="33340-109">Property value</span></span>

<span data-ttu-id="33340-110">若 **為 true**，則表示 KeyUsage 延伸模組存在。</span><span class="sxs-lookup"><span data-stu-id="33340-110">If **true**, the KeyUsage extension is present.</span></span>

## <a name="requirements"></a><span data-ttu-id="33340-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="33340-111">Requirements</span></span>



| <span data-ttu-id="33340-112">需求</span><span class="sxs-lookup"><span data-stu-id="33340-112">Requirement</span></span> | <span data-ttu-id="33340-113">值</span><span class="sxs-lookup"><span data-stu-id="33340-113">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="33340-114">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="33340-114">Redistributable</span></span><br/> | <span data-ttu-id="33340-115">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="33340-115">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="33340-116">DLL</span><span class="sxs-lookup"><span data-stu-id="33340-116">DLL</span></span><br/>             | <dl> <span data-ttu-id="33340-117"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="33340-117"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33340-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="33340-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33340-119">**KeyUsage**</span><span class="sxs-lookup"><span data-stu-id="33340-119">**KeyUsage**</span></span>](keyusage.md)
</dt> </dl>

 

 
