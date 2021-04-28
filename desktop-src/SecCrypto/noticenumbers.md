---
description: NoticeNumbers 物件-表示擴充物件的集合。
ms.assetid: b0d69df9-12c4-4872-b883-b029c4350502
title: NoticeNumbers 物件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NoticeNumbers
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: b2bd6e653eabe9b25588fd29517ac94e0c878fdb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090756"
---
# <a name="noticenumbers-object"></a><span data-ttu-id="06342-103">NoticeNumbers 物件</span><span class="sxs-lookup"><span data-stu-id="06342-103">NoticeNumbers object</span></span>

<span data-ttu-id="06342-104">\[**NoticeNumbers** 物件可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="06342-104">\[The **NoticeNumbers** object is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="06342-105">如需詳細資訊，請參閱 [**限定詞**](qualifier.md)。\]</span><span class="sxs-lookup"><span data-stu-id="06342-105">For more information, see [**Qualifier**](qualifier.md).\]</span></span>

<span data-ttu-id="06342-106">**NoticeNumbers** 物件代表 [**延伸**](extension.md)物件的集合。</span><span class="sxs-lookup"><span data-stu-id="06342-106">The **NoticeNumbers** object represents a collection of [**Extension**](extension.md) objects.</span></span> <span data-ttu-id="06342-107">每個 [**擴充**](extension.md) 物件都代表一個使用者聲明編號。</span><span class="sxs-lookup"><span data-stu-id="06342-107">Each [**Extension**](extension.md) object represents a user notice number.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="06342-108">使用時機</span><span class="sxs-lookup"><span data-stu-id="06342-108">When to use</span></span>

<span data-ttu-id="06342-109">**NoticeNumbers** 物件是用來執行下列工作：</span><span class="sxs-lookup"><span data-stu-id="06342-109">The **NoticeNumbers** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="06342-110">取得集合中的 [**擴充**](extension.md) 物件數目。</span><span class="sxs-lookup"><span data-stu-id="06342-110">Retrieve the number of [**Extension**](extension.md) objects in the collection.</span></span>
-   <span data-ttu-id="06342-111">從集合中取出特定的 [**擴充**](extension.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="06342-111">Retrieve a specific [**Extension**](extension.md) object from the collection.</span></span>
-   <span data-ttu-id="06342-112">逐一查看集合。</span><span class="sxs-lookup"><span data-stu-id="06342-112">Iterate through the collection.</span></span>

## <a name="members"></a><span data-ttu-id="06342-113">成員</span><span class="sxs-lookup"><span data-stu-id="06342-113">Members</span></span>

<span data-ttu-id="06342-114">**NoticeNumbers** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="06342-114">The **NoticeNumbers** object has these types of members:</span></span>

-   [<span data-ttu-id="06342-115">屬性</span><span class="sxs-lookup"><span data-stu-id="06342-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="06342-116">屬性</span><span class="sxs-lookup"><span data-stu-id="06342-116">Properties</span></span>

<span data-ttu-id="06342-117">**NoticeNumbers** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="06342-117">The **NoticeNumbers** object has these properties.</span></span>



| <span data-ttu-id="06342-118">屬性</span><span class="sxs-lookup"><span data-stu-id="06342-118">Property</span></span>                                              | <span data-ttu-id="06342-119">存取類型</span><span class="sxs-lookup"><span data-stu-id="06342-119">Access type</span></span>          | <span data-ttu-id="06342-120">Description</span><span class="sxs-lookup"><span data-stu-id="06342-120">Description</span></span>                                                                                                                                                                                                                     |
|:------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="06342-121">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="06342-121">**\_NewEnum**</span></span>](noticenumbers-newenum.md)<br/> | <span data-ttu-id="06342-122">唯讀</span><span class="sxs-lookup"><span data-stu-id="06342-122">Read-only</span></span><br/> | <span data-ttu-id="06342-123">在可以用來列舉集合的物件上，抓取 [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) 介面。</span><span class="sxs-lookup"><span data-stu-id="06342-123">Retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="06342-124">這個屬性會在 Visual Basic Scripting Edition (VBScript) 中隱藏。</span><span class="sxs-lookup"><span data-stu-id="06342-124">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span><br/> |
| [<span data-ttu-id="06342-125">**計數**</span><span class="sxs-lookup"><span data-stu-id="06342-125">**Count**</span></span>](noticenumbers-count.md)<br/>       | <span data-ttu-id="06342-126">唯讀</span><span class="sxs-lookup"><span data-stu-id="06342-126">Read-only</span></span><br/> | <span data-ttu-id="06342-127">抓取集合中的 [**擴充**](extension.md) 物件數目。</span><span class="sxs-lookup"><span data-stu-id="06342-127">Retrieves the number of [**Extension**](extension.md) objects in the collection.</span></span><br/>                                                                                                                                    |
| [<span data-ttu-id="06342-128">**項目**</span><span class="sxs-lookup"><span data-stu-id="06342-128">**Item**</span></span>](noticenumbers-item.md)<br/>         | <span data-ttu-id="06342-129">唯讀</span><span class="sxs-lookup"><span data-stu-id="06342-129">Read-only</span></span><br/> | <span data-ttu-id="06342-130">抓取 [**擴充**](extension.md) 物件，該物件代表集合的索引聲明編號。</span><span class="sxs-lookup"><span data-stu-id="06342-130">Retrieves the [**Extension**](extension.md) object that represents the indexed notice number of the collection.</span></span><br/> <span data-ttu-id="06342-131">這是預設屬性。</span><span class="sxs-lookup"><span data-stu-id="06342-131">This is the default property.</span></span><br/>                                                            |



 

## <a name="remarks"></a><span data-ttu-id="06342-132">備註</span><span class="sxs-lookup"><span data-stu-id="06342-132">Remarks</span></span>

<span data-ttu-id="06342-133">無法建立 **NoticeNumbers** 物件。</span><span class="sxs-lookup"><span data-stu-id="06342-133">The **NoticeNumbers** object cannot be created.</span></span>

<span data-ttu-id="06342-134">NoticeNumbers 物件是在 [**NoticeNumbers**](qualifier-noticenumbers.md) 屬性中使用。</span><span class="sxs-lookup"><span data-stu-id="06342-134">The NoticeNumbers object is used in the [**Qualifier.NoticeNumbers**](qualifier-noticenumbers.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="06342-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="06342-135">Requirements</span></span>



| <span data-ttu-id="06342-136">需求</span><span class="sxs-lookup"><span data-stu-id="06342-136">Requirement</span></span> | <span data-ttu-id="06342-137">值</span><span class="sxs-lookup"><span data-stu-id="06342-137">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="06342-138">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="06342-138">Redistributable</span></span><br/> | <span data-ttu-id="06342-139">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="06342-139">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="06342-140">DLL</span><span class="sxs-lookup"><span data-stu-id="06342-140">DLL</span></span><br/>             | <dl> <span data-ttu-id="06342-141"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="06342-141"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
