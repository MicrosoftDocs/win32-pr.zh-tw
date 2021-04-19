---
description: 抓取封包訊息的收件者集合。
ms.assetid: de9cbf8e-f34c-4e08-89aa-b5ac842aa599
title: EnvelopedData [收件者] 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnvelopedData.Recipients
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: f047b4a8c579fb7f327b7410965a326c4a2f255d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995273"
---
# <a name="envelopeddatarecipients-property"></a><span data-ttu-id="96771-103">EnvelopedData [收件者] 屬性</span><span class="sxs-lookup"><span data-stu-id="96771-103">EnvelopedData.Recipients property</span></span>

<span data-ttu-id="96771-104">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="96771-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="96771-105">相反地，請使用 [**EnvelopedCms 類別**](/dotnet/api/system.security.cryptography.pkcs.envelopedcms?view=dotnet-plat-ext-3.1&preserve-view=true)，以使用 [**system.servicemodel 命名空間。**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true)\]</span><span class="sxs-lookup"><span data-stu-id="96771-105">Instead, use the [**EnvelopedCms Class**](/dotnet/api/system.security.cryptography.pkcs.envelopedcms?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="96771-106">收件 **者屬性會** 抓取封包訊息的收件者集合。</span><span class="sxs-lookup"><span data-stu-id="96771-106">The **Recipients** property retrieves the collection of recipients of the enveloped message.</span></span>

## <a name="syntax"></a><span data-ttu-id="96771-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="96771-107">Syntax</span></span>


```VB
EnvelopedData.Recipients As Recipients
```



## <a name="property-value"></a><span data-ttu-id="96771-108">屬性值</span><span class="sxs-lookup"><span data-stu-id="96771-108">Property value</span></span>

<span data-ttu-id="96771-109">代表封包訊息收件者的收件 [**者集合。**](recipients.md)</span><span class="sxs-lookup"><span data-stu-id="96771-109">A [**Recipients**](recipients.md) collection that represents the recipients of the enveloped message.</span></span>

## <a name="requirements"></a><span data-ttu-id="96771-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="96771-110">Requirements</span></span>



| <span data-ttu-id="96771-111">需求</span><span class="sxs-lookup"><span data-stu-id="96771-111">Requirement</span></span> | <span data-ttu-id="96771-112">值</span><span class="sxs-lookup"><span data-stu-id="96771-112">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="96771-113">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="96771-113">End of client support</span></span><br/> | <span data-ttu-id="96771-114">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="96771-114">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="96771-115">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="96771-115">End of server support</span></span><br/> | <span data-ttu-id="96771-116">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="96771-116">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="96771-117">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="96771-117">Redistributable</span></span><br/>       | <span data-ttu-id="96771-118">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="96771-118">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="96771-119">DLL</span><span class="sxs-lookup"><span data-stu-id="96771-119">DLL</span></span><br/>                   | <dl> <span data-ttu-id="96771-120"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="96771-120"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96771-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="96771-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96771-122">**EnvelopedData**</span><span class="sxs-lookup"><span data-stu-id="96771-122">**EnvelopedData**</span></span>](envelopeddata.md)
</dt> </dl>

 

 
