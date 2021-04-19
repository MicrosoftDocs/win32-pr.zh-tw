---
description: 建立指定之字串的雜湊。
ms.assetid: 8d3e16e7-7b93-410c-b771-7684d1bf2160
title: HashedData 雜湊方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HashedData.Hash
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: d36973340a7dbf67f8a8b0d1aa4cd5738ef97d74
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990122"
---
# <a name="hasheddatahash-method"></a><span data-ttu-id="09e3a-103">HashedData 雜湊方法</span><span class="sxs-lookup"><span data-stu-id="09e3a-103">HashedData.Hash method</span></span>

<span data-ttu-id="09e3a-104">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="09e3a-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="09e3a-105">請改用 [**system.string 命名空間中的**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) [**HashAlgorithm 類別**](/previous-versions/windows/)。\]</span><span class="sxs-lookup"><span data-stu-id="09e3a-105">Instead, use the [**HashAlgorithm Class**](/previous-versions/windows/) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="09e3a-106">**雜湊** 方法會建立指定之字串的雜湊。</span><span class="sxs-lookup"><span data-stu-id="09e3a-106">The **Hash** method creates a hash of the specified string.</span></span>

## <a name="syntax"></a><span data-ttu-id="09e3a-107">語法</span><span class="sxs-lookup"><span data-stu-id="09e3a-107">Syntax</span></span>


```VB
HashedData.Hash( _
  ByVal newVal _
)
```



## <a name="parameters"></a><span data-ttu-id="09e3a-108">參數</span><span class="sxs-lookup"><span data-stu-id="09e3a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09e3a-109">*newVal*</span><span class="sxs-lookup"><span data-stu-id="09e3a-109">*newVal*</span></span> 
</dt> <dd>

<span data-ttu-id="09e3a-110">包含要雜湊之值的字串。</span><span class="sxs-lookup"><span data-stu-id="09e3a-110">String that contains the value to hash.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="09e3a-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="09e3a-111">Return value</span></span>

<span data-ttu-id="09e3a-112">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="09e3a-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="09e3a-113">備註</span><span class="sxs-lookup"><span data-stu-id="09e3a-113">Remarks</span></span>

<span data-ttu-id="09e3a-114">若要建立大量資料的雜湊，請呼叫每個資料片段的 **雜湊** 方法。</span><span class="sxs-lookup"><span data-stu-id="09e3a-114">To create the hash of a large amount of data, call the **Hash** method for each piece of data.</span></span> <span data-ttu-id="09e3a-115">在讀取屬性之前，會將每個資料片段的雜湊串連至 [**Value**](hasheddata-value.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="09e3a-115">The hash of each piece of data is concatenated to the [**Value**](hasheddata-value.md) property until the property is read.</span></span> <span data-ttu-id="09e3a-116">當讀取屬性時，會重設 **Value** 屬性的內容。</span><span class="sxs-lookup"><span data-stu-id="09e3a-116">The contents of the **Value** property are reset when the property is read.</span></span>

## <a name="requirements"></a><span data-ttu-id="09e3a-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="09e3a-117">Requirements</span></span>



| <span data-ttu-id="09e3a-118">需求</span><span class="sxs-lookup"><span data-stu-id="09e3a-118">Requirement</span></span> | <span data-ttu-id="09e3a-119">值</span><span class="sxs-lookup"><span data-stu-id="09e3a-119">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="09e3a-120">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="09e3a-120">End of client support</span></span><br/> | <span data-ttu-id="09e3a-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="09e3a-121">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="09e3a-122">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="09e3a-122">End of server support</span></span><br/> | <span data-ttu-id="09e3a-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="09e3a-123">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="09e3a-124">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="09e3a-124">Redistributable</span></span><br/>       | <span data-ttu-id="09e3a-125">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="09e3a-125">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="09e3a-126">DLL</span><span class="sxs-lookup"><span data-stu-id="09e3a-126">DLL</span></span><br/>                   | <dl> <span data-ttu-id="09e3a-127"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="09e3a-127"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
