---
title: StringCollection. getAttributeCountByType 方法
description: GetAttributeCountByType 方法會抓取與指定的 StringCollection 專案索引、屬性名稱和語言相關聯的屬性數目。
ms.assetid: 3671b7b7-d6d4-4049-8710-d0f34c740b1e
keywords:
- getAttributeCountByType 方法 Windows Media Player
- getAttributeCountByType 方法 Windows Media Player，StringCollection 類別
- StringCollection 類別 Windows Media Player，getAttributeCountByType 方法
topic_type:
- apiref
api_name:
- StringCollection.getAttributeCountByType
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2acf2d7a1f8849f9bd0e83ead3880ca90d2d6149
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000827"
---
# <a name="stringcollectiongetattributecountbytype-method"></a><span data-ttu-id="816fc-106">StringCollection. getAttributeCountByType 方法</span><span class="sxs-lookup"><span data-stu-id="816fc-106">StringCollection.getAttributeCountByType method</span></span>

<span data-ttu-id="816fc-107">**GetAttributeCountByType** 方法會抓取與指定的 **StringCollection** 專案索引、屬性名稱和語言相關聯的屬性數目。</span><span class="sxs-lookup"><span data-stu-id="816fc-107">The **getAttributeCountByType** method retrieves the number of attributes associated with the specified **StringCollection** item index, attribute name, and language.</span></span>

## <a name="syntax"></a><span data-ttu-id="816fc-108">語法</span><span class="sxs-lookup"><span data-stu-id="816fc-108">Syntax</span></span>


```JScript
retVal = StringCollection.getAttributeCountByType(
  index,
  name,
  language
)
```



## <a name="parameters"></a><span data-ttu-id="816fc-109">參數</span><span class="sxs-lookup"><span data-stu-id="816fc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="816fc-110">*索引* \[在\]</span><span class="sxs-lookup"><span data-stu-id="816fc-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="816fc-111">**Number** (**long**) 指定要從中取得屬性之 **StringCollection** 專案的以零為基底的索引。</span><span class="sxs-lookup"><span data-stu-id="816fc-111">**Number** (**long**) specifying the zero-based index of the **StringCollection** item from which to get the attribute.</span></span>

</dd> <dt>

<span data-ttu-id="816fc-112">*名稱* \[在\]</span><span class="sxs-lookup"><span data-stu-id="816fc-112">*name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="816fc-113">包含屬性名稱的 **字串**。</span><span class="sxs-lookup"><span data-stu-id="816fc-113">**String** containing the name of the attribute.</span></span>

</dd> <dt>

<span data-ttu-id="816fc-114">*語言* \[在\]</span><span class="sxs-lookup"><span data-stu-id="816fc-114">*language* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="816fc-115">包含語言的 **字串**。</span><span class="sxs-lookup"><span data-stu-id="816fc-115">**String** containing the language.</span></span> <span data-ttu-id="816fc-116">如果值設定為 null 或空字串 ( "" ) ，則會使用目前的地區設定字串。</span><span class="sxs-lookup"><span data-stu-id="816fc-116">If the value is set to null or the empty string (""), the current locale string is used.</span></span> <span data-ttu-id="816fc-117">否則，此值必須是有效的 RFC 1766 語言字串，例如 "en-us"。</span><span class="sxs-lookup"><span data-stu-id="816fc-117">Otherwise, the value must be a valid RFC 1766 language string such as "en-us".</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="816fc-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="816fc-118">Return value</span></span>

<span data-ttu-id="816fc-119">這個方法會傳回 **數位** (**long**) 。</span><span class="sxs-lookup"><span data-stu-id="816fc-119">This method returns a **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="816fc-120">備註</span><span class="sxs-lookup"><span data-stu-id="816fc-120">Remarks</span></span>

<span data-ttu-id="816fc-121">這個方法是用來判斷對應至特定 **StringCollection** 專案特定屬性名稱的屬性數目。</span><span class="sxs-lookup"><span data-stu-id="816fc-121">This method is used to determine the number of attributes corresponding to a particular attribute name for a particular **StringCollection** item.</span></span> <span data-ttu-id="816fc-122">然後，您可以將索引編號傳遞給 **StringCollection. getItemInfoByType** 方法的第四個參數。</span><span class="sxs-lookup"><span data-stu-id="816fc-122">Index numbers can then be passed to the fourth parameter of the **StringCollection.getItemInfoByType** method.</span></span>

<span data-ttu-id="816fc-123">若要使用此方法，需要有程式庫的讀取權限。</span><span class="sxs-lookup"><span data-stu-id="816fc-123">To use this method, read access to the library is required.</span></span> <span data-ttu-id="816fc-124">如需詳細資訊，請參閱連結 [庫存取](library-access.md)。</span><span class="sxs-lookup"><span data-stu-id="816fc-124">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="816fc-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="816fc-125">Requirements</span></span>



| <span data-ttu-id="816fc-126">需求</span><span class="sxs-lookup"><span data-stu-id="816fc-126">Requirement</span></span> | <span data-ttu-id="816fc-127">值</span><span class="sxs-lookup"><span data-stu-id="816fc-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="816fc-128">版本</span><span class="sxs-lookup"><span data-stu-id="816fc-128">Version</span></span><br/> | <span data-ttu-id="816fc-129">Windows Media Player 11。</span><span class="sxs-lookup"><span data-stu-id="816fc-129">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="816fc-130">DLL</span><span class="sxs-lookup"><span data-stu-id="816fc-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="816fc-131"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="816fc-131"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="816fc-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="816fc-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="816fc-133">**StringCollection 物件**</span><span class="sxs-lookup"><span data-stu-id="816fc-133">**StringCollection Object**</span></span>](stringcollection-object.md)
</dt> </dl>

 

 





