---
description: 在成功呼叫 Hash 方法之後，取得雜湊的資料。
ms.assetid: 02ba92d2-38eb-4c01-99b9-11676e7d49ff
title: HashedData。 Value 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HashedData.Value
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 496bdd76400c746ae3209a2e3c99b6cf4e5bc4b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982943"
---
# <a name="hasheddatavalue-property"></a><span data-ttu-id="19c2c-103">HashedData。 Value 屬性</span><span class="sxs-lookup"><span data-stu-id="19c2c-103">HashedData.Value property</span></span>

<span data-ttu-id="19c2c-104">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="19c2c-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="19c2c-105">請改用 [**system.string 命名空間中的**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) [**HashAlgorithm 類別**](/previous-versions/windows/)。\]</span><span class="sxs-lookup"><span data-stu-id="19c2c-105">Instead, use the [**HashAlgorithm Class**](/previous-versions/windows/) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="19c2c-106">**Value** 屬性會在成功呼叫 [**Hash**](hasheddata-hash.md)方法之後，取得雜湊的資料。</span><span class="sxs-lookup"><span data-stu-id="19c2c-106">The **Value** property retrieves the hashed data after successful calls to the [**Hash**](hasheddata-hash.md) method.</span></span> <span data-ttu-id="19c2c-107">雜湊值會以十六進位格式傳回。</span><span class="sxs-lookup"><span data-stu-id="19c2c-107">The hash value is returned in hexadecimal format.</span></span> <span data-ttu-id="19c2c-108">這是預設屬性。</span><span class="sxs-lookup"><span data-stu-id="19c2c-108">This is the default property.</span></span>

## <a name="syntax"></a><span data-ttu-id="19c2c-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="19c2c-109">Syntax</span></span>


```VB
HashedData.Value As String
```



## <a name="property-value"></a><span data-ttu-id="19c2c-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="19c2c-110">Property value</span></span>

<span data-ttu-id="19c2c-111">字串，包含十六進位格式的雜湊資料。</span><span class="sxs-lookup"><span data-stu-id="19c2c-111">A string that contains the hashed data in hexadecimal format.</span></span>

## <a name="remarks"></a><span data-ttu-id="19c2c-112">備註</span><span class="sxs-lookup"><span data-stu-id="19c2c-112">Remarks</span></span>

<span data-ttu-id="19c2c-113">若要建立大量資料的雜湊，請呼叫每個資料片段的 [**雜湊**](hasheddata-hash.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="19c2c-113">To create the hash of a large amount of data, call the [**Hash**](hasheddata-hash.md) method for each piece of data.</span></span> <span data-ttu-id="19c2c-114">在讀取屬性之前，會將每個資料片段的雜湊串連至 **Value** 屬性。</span><span class="sxs-lookup"><span data-stu-id="19c2c-114">The hash of each piece of data is concatenated to the **Value** property until the property is read.</span></span> <span data-ttu-id="19c2c-115">當讀取屬性時，會重設 **Value** 屬性的內容。</span><span class="sxs-lookup"><span data-stu-id="19c2c-115">The contents of the **Value** property are reset when the property is read.</span></span>

## <a name="requirements"></a><span data-ttu-id="19c2c-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="19c2c-116">Requirements</span></span>



| <span data-ttu-id="19c2c-117">需求</span><span class="sxs-lookup"><span data-stu-id="19c2c-117">Requirement</span></span> | <span data-ttu-id="19c2c-118">值</span><span class="sxs-lookup"><span data-stu-id="19c2c-118">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="19c2c-119">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="19c2c-119">End of client support</span></span><br/> | <span data-ttu-id="19c2c-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="19c2c-120">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="19c2c-121">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="19c2c-121">End of server support</span></span><br/> | <span data-ttu-id="19c2c-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="19c2c-122">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="19c2c-123">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="19c2c-123">Redistributable</span></span><br/>       | <span data-ttu-id="19c2c-124">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="19c2c-124">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="19c2c-125">DLL</span><span class="sxs-lookup"><span data-stu-id="19c2c-125">DLL</span></span><br/>                   | <dl> <span data-ttu-id="19c2c-126"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="19c2c-126"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19c2c-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="19c2c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19c2c-128">**HashedData**</span><span class="sxs-lookup"><span data-stu-id="19c2c-128">**HashedData**</span></span>](hasheddata.md)
</dt> </dl>

 

 
