---
description: 抓取編碼的資料。
ms.assetid: 8e07ac14-6859-410f-ab30-84b8d60a94ad
title: EncodedData。 Value 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EncodedData.Value
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e040f78d5c0ccfa3e50729f16b75a0691771980e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001212"
---
# <a name="encodeddatavalue-property"></a><span data-ttu-id="6026b-103">EncodedData。 Value 屬性</span><span class="sxs-lookup"><span data-stu-id="6026b-103">EncodedData.Value property</span></span>

<span data-ttu-id="6026b-104">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="6026b-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="6026b-105">請改用 [**system.string 命名空間中的**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) [**AsnEncodedData 類別**](/dotnet/api/system.security.cryptography.asnencodeddata?view=netcore-3.1)。\]</span><span class="sxs-lookup"><span data-stu-id="6026b-105">Instead, use the [**AsnEncodedData Class**](/dotnet/api/system.security.cryptography.asnencodeddata?view=netcore-3.1) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="6026b-106">**Value** 屬性會捕獲編碼的資料。</span><span class="sxs-lookup"><span data-stu-id="6026b-106">The **Value** property retrieves the encoded data.</span></span> <span data-ttu-id="6026b-107">這是預設屬性。</span><span class="sxs-lookup"><span data-stu-id="6026b-107">This is the default property.</span></span>

<span data-ttu-id="6026b-108">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="6026b-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="6026b-109">語法</span><span class="sxs-lookup"><span data-stu-id="6026b-109">Syntax</span></span>


```VB
EncodedData.Value( _
  [ ByVal EncodingType ] _
) As String
```



## <a name="property-value"></a><span data-ttu-id="6026b-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="6026b-110">Property value</span></span>

<span data-ttu-id="6026b-111">包含已編碼資料的字串。</span><span class="sxs-lookup"><span data-stu-id="6026b-111">A string that contains the encoded data.</span></span>

## <a name="requirements"></a><span data-ttu-id="6026b-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="6026b-112">Requirements</span></span>



| <span data-ttu-id="6026b-113">需求</span><span class="sxs-lookup"><span data-stu-id="6026b-113">Requirement</span></span> | <span data-ttu-id="6026b-114">值</span><span class="sxs-lookup"><span data-stu-id="6026b-114">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6026b-115">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="6026b-115">End of client support</span></span><br/> | <span data-ttu-id="6026b-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6026b-116">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="6026b-117">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="6026b-117">End of server support</span></span><br/> | <span data-ttu-id="6026b-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6026b-118">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="6026b-119">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="6026b-119">Redistributable</span></span><br/>       | <span data-ttu-id="6026b-120">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="6026b-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="6026b-121">DLL</span><span class="sxs-lookup"><span data-stu-id="6026b-121">DLL</span></span><br/>                   | <dl> <span data-ttu-id="6026b-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6026b-122"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
