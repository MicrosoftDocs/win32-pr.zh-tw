---
description: 抓取布林值，指出是否將延伸標記為重大。
ms.assetid: 71f55d63-a51c-472c-81fc-59212c97bb34
title: IsCritical 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Extension.IsCritical
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 61e53f869a7063e029cb629b8b2fff4cff025b31
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995679"
---
# <a name="extensioniscritical-property"></a><span data-ttu-id="893e4-103">IsCritical 屬性</span><span class="sxs-lookup"><span data-stu-id="893e4-103">Extension.IsCritical property</span></span>

<span data-ttu-id="893e4-104">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="893e4-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="893e4-105">請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509Extension 類別**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1)。\]</span><span class="sxs-lookup"><span data-stu-id="893e4-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="893e4-106">**IsCritical** 屬性會抓取布林值，指出延伸模組是否標記為重大。</span><span class="sxs-lookup"><span data-stu-id="893e4-106">The **IsCritical** property retrieves a Boolean value that indicates whether the extension is marked critical.</span></span>

## <a name="syntax"></a><span data-ttu-id="893e4-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="893e4-107">Syntax</span></span>


```VB
Extension.IsCritical As Boolean
```



## <a name="property-value"></a><span data-ttu-id="893e4-108">屬性值</span><span class="sxs-lookup"><span data-stu-id="893e4-108">Property value</span></span>

<span data-ttu-id="893e4-109">若 **為 true**，則會將延伸標示為「重大」。</span><span class="sxs-lookup"><span data-stu-id="893e4-109">If **true**, the extension is marked critical.</span></span>

## <a name="requirements"></a><span data-ttu-id="893e4-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="893e4-110">Requirements</span></span>



| <span data-ttu-id="893e4-111">需求</span><span class="sxs-lookup"><span data-stu-id="893e4-111">Requirement</span></span> | <span data-ttu-id="893e4-112">值</span><span class="sxs-lookup"><span data-stu-id="893e4-112">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="893e4-113">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="893e4-113">End of client support</span></span><br/> | <span data-ttu-id="893e4-114">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="893e4-114">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="893e4-115">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="893e4-115">End of server support</span></span><br/> | <span data-ttu-id="893e4-116">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="893e4-116">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="893e4-117">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="893e4-117">Redistributable</span></span><br/>       | <span data-ttu-id="893e4-118">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="893e4-118">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="893e4-119">DLL</span><span class="sxs-lookup"><span data-stu-id="893e4-119">DLL</span></span><br/>                   | <dl> <span data-ttu-id="893e4-120"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="893e4-120"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
