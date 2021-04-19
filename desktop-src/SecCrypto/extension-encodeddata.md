---
description: 抓取延伸模組的編碼資料。
ms.assetid: 79811557-6d7e-4d19-bcbb-1f79455dd286
title: EncodedData 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Extension.EncodedData
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 2153c97d523693a0a1ea13f92135a17591ce68d6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982569"
---
# <a name="extensionencodeddata-property"></a><span data-ttu-id="09897-103">EncodedData 屬性</span><span class="sxs-lookup"><span data-stu-id="09897-103">Extension.EncodedData property</span></span>

<span data-ttu-id="09897-104">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="09897-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="09897-105">請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509Extension 類別**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1)。\]</span><span class="sxs-lookup"><span data-stu-id="09897-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="09897-106">**EncodedData** 屬性會抓取擴充功能的編碼資料。</span><span class="sxs-lookup"><span data-stu-id="09897-106">The **EncodedData** property retrieves the encoded data for the extension.</span></span>

## <a name="syntax"></a><span data-ttu-id="09897-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="09897-107">Syntax</span></span>


```VB
Extension.EncodedData As EncodedData
```



## <a name="property-value"></a><span data-ttu-id="09897-108">屬性值</span><span class="sxs-lookup"><span data-stu-id="09897-108">Property value</span></span>

<span data-ttu-id="09897-109">代表憑證延伸之資料的 [**EncodedData**](encodeddata.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="09897-109">An [**EncodedData**](encodeddata.md) object that represents the data of the certificate extension.</span></span>

## <a name="requirements"></a><span data-ttu-id="09897-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="09897-110">Requirements</span></span>



| <span data-ttu-id="09897-111">需求</span><span class="sxs-lookup"><span data-stu-id="09897-111">Requirement</span></span> | <span data-ttu-id="09897-112">值</span><span class="sxs-lookup"><span data-stu-id="09897-112">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="09897-113">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="09897-113">End of client support</span></span><br/> | <span data-ttu-id="09897-114">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="09897-114">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="09897-115">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="09897-115">End of server support</span></span><br/> | <span data-ttu-id="09897-116">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="09897-116">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="09897-117">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="09897-117">Redistributable</span></span><br/>       | <span data-ttu-id="09897-118">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="09897-118">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="09897-119">DLL</span><span class="sxs-lookup"><span data-stu-id="09897-119">DLL</span></span><br/>                   | <dl> <span data-ttu-id="09897-120"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="09897-120"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
