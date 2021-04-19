---
title: IWMPStringCollection Item 方法
description: Item 方法會傳回指定索引處的字串。
ms.assetid: 77546cb2-eda5-4bb8-97b9-55270461815f
keywords:
- Item 方法 Windows Media Player
- Item 方法 Windows Media Player，IWMPStringCollection 介面
- IWMPStringCollection 介面 Windows Media Player，Item 方法
topic_type:
- apiref
api_name:
- IWMPStringCollection.Item
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f69bdc63448699a595238b9907f4b1253209ad06
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989779"
---
# <a name="iwmpstringcollectionitem-method"></a><span data-ttu-id="29e39-106">IWMPStringCollection：： Item 方法</span><span class="sxs-lookup"><span data-stu-id="29e39-106">IWMPStringCollection::Item method</span></span>

<span data-ttu-id="29e39-107">**Item** 方法會傳回指定索引處的字串。</span><span class="sxs-lookup"><span data-stu-id="29e39-107">The **Item** method returns the string at the specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="29e39-108">語法</span><span class="sxs-lookup"><span data-stu-id="29e39-108">Syntax</span></span>


```CSharp
public System.String Item(
  System.Int32 lIndex
);
```


```VB

Public Function Item( _
  ByVal lIndex As System.Int32 _
) As System.String
Implements IWMPStringCollection.Item
```





## <a name="parameters"></a><span data-ttu-id="29e39-109">參數</span><span class="sxs-lookup"><span data-stu-id="29e39-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29e39-110">*lIndex* \[在\]</span><span class="sxs-lookup"><span data-stu-id="29e39-110">*lIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29e39-111">作為索引的 **system.object** 。</span><span class="sxs-lookup"><span data-stu-id="29e39-111">A **System.Int32** that is the index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="29e39-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="29e39-112">Return value</span></span>

<span data-ttu-id="29e39-113">System.string **，它** 是位於指定索引位置的字串。</span><span class="sxs-lookup"><span data-stu-id="29e39-113">A **System.String** that is the string at the specified index.</span></span>

## <a name="remarks"></a><span data-ttu-id="29e39-114">備註</span><span class="sxs-lookup"><span data-stu-id="29e39-114">Remarks</span></span>

<span data-ttu-id="29e39-115">**IWMPStringCollection** 介面是用來取得屬性可用的值集。</span><span class="sxs-lookup"><span data-stu-id="29e39-115">The **IWMPStringCollection** interface is used to retrieve the set of values available for an attribute.</span></span> <span data-ttu-id="29e39-116">例如，您可以使用 **IWMPMediaCollection. getAttributeStringCollection** 方法來取得 **IWMPStringCollection** 介面，代表音訊媒體類型內內容類型屬性的所有值。</span><span class="sxs-lookup"><span data-stu-id="29e39-116">For example, the **IWMPMediaCollection.getAttributeStringCollection** method can be used to retrieve an **IWMPStringCollection** interface representing all the values for the Genre attribute within the Audio media type.</span></span> <span data-ttu-id="29e39-117">然後，可以使用 Item 方法來逐一查看 [ **內容** 類型] 屬性的所有可能值。</span><span class="sxs-lookup"><span data-stu-id="29e39-117">The **Item** method can then be used to iterate through all of the possible values for the Genre attribute.</span></span>

<span data-ttu-id="29e39-118">若要使用此方法，需要有程式庫的讀取權限。</span><span class="sxs-lookup"><span data-stu-id="29e39-118">To use this method, read access to the library is required.</span></span> <span data-ttu-id="29e39-119">如需詳細資訊，請參閱連結 [庫存取](library-access.md)。</span><span class="sxs-lookup"><span data-stu-id="29e39-119">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="29e39-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="29e39-120">Requirements</span></span>



| <span data-ttu-id="29e39-121">需求</span><span class="sxs-lookup"><span data-stu-id="29e39-121">Requirement</span></span> | <span data-ttu-id="29e39-122">值</span><span class="sxs-lookup"><span data-stu-id="29e39-122">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="29e39-123">版本</span><span class="sxs-lookup"><span data-stu-id="29e39-123">Version</span></span><br/>   | <span data-ttu-id="29e39-124">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="29e39-124">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="29e39-125">命名空間</span><span class="sxs-lookup"><span data-stu-id="29e39-125">Namespace</span></span><br/> | <span data-ttu-id="29e39-126">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="29e39-126">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="29e39-127">組件</span><span class="sxs-lookup"><span data-stu-id="29e39-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="29e39-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="29e39-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="29e39-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="29e39-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29e39-130">**IWMPMediaCollection. getAttributeStringCollection (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="29e39-130">**IWMPMediaCollection.getAttributeStringCollection (VB and C#)**</span></span>](wmplibiwmpmediacollection-iwmpmediacollection-getattributestringcollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="29e39-131">**IWMPSettings2. mediaAccessRights (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="29e39-131">**IWMPSettings2.mediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="29e39-132">**IWMPSettings2. requestMediaAccessRights (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="29e39-132">**IWMPSettings2.requestMediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="29e39-133">**IWMPStringCollection 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="29e39-133">**IWMPStringCollection Interface (VB and C#)**</span></span>](iwmpstringcollection--vb-and-c.md)
</dt> </dl>

 

 





