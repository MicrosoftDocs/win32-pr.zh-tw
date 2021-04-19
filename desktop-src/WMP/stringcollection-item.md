---
title: StringCollection 專案方法
description: Item 方法會在指定的索引處捕獲字串。
ms.assetid: 5f6afff2-3ecc-4b28-8c67-f859f5440d4f
keywords:
- item 方法 Windows Media Player
- item 方法 Windows Media Player，StringCollection 類別
- StringCollection 類別 Windows Media Player，item 方法
topic_type:
- apiref
api_name:
- StringCollection.item
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4244ad194ff3426dab81baddc0b7188214e0360
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106979896"
---
# <a name="stringcollectionitem-method"></a><span data-ttu-id="80add-106">StringCollection 專案方法</span><span class="sxs-lookup"><span data-stu-id="80add-106">StringCollection.item method</span></span>

<span data-ttu-id="80add-107">**Item** 方法會在指定的索引處捕獲字串。</span><span class="sxs-lookup"><span data-stu-id="80add-107">The **item** method retrieves the string at the specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="80add-108">語法</span><span class="sxs-lookup"><span data-stu-id="80add-108">Syntax</span></span>


```JScript
strRetVal = StringCollection.item(
  index
)
```



## <a name="parameters"></a><span data-ttu-id="80add-109">參數</span><span class="sxs-lookup"><span data-stu-id="80add-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80add-110">*索引* \[在\]</span><span class="sxs-lookup"><span data-stu-id="80add-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80add-111">包含索引的 (**長**) **數目**。</span><span class="sxs-lookup"><span data-stu-id="80add-111">**Number** (**long**) containing the index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="80add-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="80add-112">Return value</span></span>

<span data-ttu-id="80add-113">這個方法會傳回 **字串**。</span><span class="sxs-lookup"><span data-stu-id="80add-113">This method returns a **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="80add-114">備註</span><span class="sxs-lookup"><span data-stu-id="80add-114">Remarks</span></span>

<span data-ttu-id="80add-115">**StringCollection** 物件是用來取得屬性可用的值集。</span><span class="sxs-lookup"><span data-stu-id="80add-115">The **StringCollection** object is used to retrieve the set of values available for an attribute.</span></span> <span data-ttu-id="80add-116">例如， *MediaCollection*。**getAttributeStringCollection** 方法可以用來取出 **StringCollection** 物件，代表音訊媒體類型內內容類型屬性的所有值。</span><span class="sxs-lookup"><span data-stu-id="80add-116">For example, the *MediaCollection*.**getAttributeStringCollection** method can be used to retrieve a **StringCollection** object representing all the values for the Genre attribute within the Audio media type.</span></span> <span data-ttu-id="80add-117">然後，可以使用 item 屬性來逐一查看 [ **內容** 類型] 屬性的所有可能值。</span><span class="sxs-lookup"><span data-stu-id="80add-117">The **item** property can then be used to iterate through all of the possible values for the Genre attribute.</span></span>

<span data-ttu-id="80add-118">若要使用此方法，需要有程式庫的讀取權限。</span><span class="sxs-lookup"><span data-stu-id="80add-118">To use this method, read access to the library is required.</span></span> <span data-ttu-id="80add-119">如需詳細資訊，請參閱連結 [庫存取](library-access.md)。</span><span class="sxs-lookup"><span data-stu-id="80add-119">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="80add-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="80add-120">Requirements</span></span>



| <span data-ttu-id="80add-121">需求</span><span class="sxs-lookup"><span data-stu-id="80add-121">Requirement</span></span> | <span data-ttu-id="80add-122">值</span><span class="sxs-lookup"><span data-stu-id="80add-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="80add-123">版本</span><span class="sxs-lookup"><span data-stu-id="80add-123">Version</span></span><br/> | <span data-ttu-id="80add-124">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="80add-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="80add-125">DLL</span><span class="sxs-lookup"><span data-stu-id="80add-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="80add-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="80add-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="80add-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="80add-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80add-128">**MediaCollection.getAttributeStringCollection**</span><span class="sxs-lookup"><span data-stu-id="80add-128">**MediaCollection.getAttributeStringCollection**</span></span>](mediacollection-getattributestringcollection.md)
</dt> <dt>

[<span data-ttu-id="80add-129">**設定. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="80add-129">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="80add-130">**設定. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="80add-130">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="80add-131">**StringCollection 物件**</span><span class="sxs-lookup"><span data-stu-id="80add-131">**StringCollection Object**</span></span>](stringcollection-object.md)
</dt> </dl>

 

 





