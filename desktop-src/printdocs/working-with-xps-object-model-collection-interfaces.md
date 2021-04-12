---
description: 描述如何使用集合介面的一般方法。
ms.assetid: 6ea311c0-a155-47de-ad40-62b0cbeb6e8f
title: 使用 XPS OM 集合介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7cda84243347680d91a6f3a5255f7ebf4e66932
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193374"
---
# <a name="working-with-xps-om-collection-interfaces"></a><span data-ttu-id="860c4-103">使用 XPS OM 集合介面</span><span class="sxs-lookup"><span data-stu-id="860c4-103">Working with XPS OM Collection Interfaces</span></span>

<span data-ttu-id="860c4-104">描述如何使用集合介面的一般方法。</span><span class="sxs-lookup"><span data-stu-id="860c4-104">Describes how to use the common methods of the collection interfaces.</span></span>

## <a name="contents"></a><span data-ttu-id="860c4-105">目錄</span><span class="sxs-lookup"><span data-stu-id="860c4-105">Contents</span></span>

<span data-ttu-id="860c4-106">本節所述的方法會顯示在下列清單中。</span><span class="sxs-lookup"><span data-stu-id="860c4-106">The methods described in this section are shown in the list that follows.</span></span> <span data-ttu-id="860c4-107">並非所有的集合介面都支援這些方法，而某些介面也支援此頁面上未描述的方法。</span><span class="sxs-lookup"><span data-stu-id="860c4-107">Not all collection interfaces support each of these methods, and some interfaces also support methods that are not described on this page.</span></span> <span data-ttu-id="860c4-108">如需特定介面所支援的方法清單，請參閱該介面描述的描述。</span><span class="sxs-lookup"><span data-stu-id="860c4-108">For the list of methods supported by a specific interface, refer to the description of that interface's description.</span></span>

<dl>

[<span data-ttu-id="860c4-109">Append 方法</span><span class="sxs-lookup"><span data-stu-id="860c4-109">Append Method</span></span>](#append-method)  
[<span data-ttu-id="860c4-110">GetAt 方法</span><span class="sxs-lookup"><span data-stu-id="860c4-110">GetAt Method</span></span>](#getat-method)  
[<span data-ttu-id="860c4-111">GetCount 方法</span><span class="sxs-lookup"><span data-stu-id="860c4-111">GetCount Method</span></span>](#getcount-method)  
[<span data-ttu-id="860c4-112">InsertAt 方法</span><span class="sxs-lookup"><span data-stu-id="860c4-112">InsertAt Method</span></span>](#insertat-method)  
[<span data-ttu-id="860c4-113">RemoveAt 方法</span><span class="sxs-lookup"><span data-stu-id="860c4-113">RemoveAt Method</span></span>](#removeat-method)  
[<span data-ttu-id="860c4-114">SetAt 方法</span><span class="sxs-lookup"><span data-stu-id="860c4-114">SetAt Method</span></span>](#setat-method)  
</dl>

[<span data-ttu-id="860c4-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="860c4-115">See also</span></span>](#see-also)

## <a name="append-method"></a><span data-ttu-id="860c4-116">Append 方法</span><span class="sxs-lookup"><span data-stu-id="860c4-116">Append Method</span></span>

<span data-ttu-id="860c4-117">將物件附加至集合的結尾。</span><span class="sxs-lookup"><span data-stu-id="860c4-117">Appends an object to the end of the collection.</span></span>

<span data-ttu-id="860c4-118">**泛型語法**</span><span class="sxs-lookup"><span data-stu-id="860c4-118">**Generic Syntax**</span></span>


```C++
HRESULT Append(
  [in]  Object *object
);
```



<span data-ttu-id="860c4-119">**說明**</span><span class="sxs-lookup"><span data-stu-id="860c4-119">**Description**</span></span>

<span data-ttu-id="860c4-120">在集合的結尾，這個方法會附加在參數清單中傳遞的物件，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="860c4-120">To the end of the collection, this method appends an object that is passed in the parameter list, as shown in the following diagram.</span></span>

![顯示附加專案如何將專案加入至集合的圖表](images/generic-append.png)

## <a name="getat-method"></a><span data-ttu-id="860c4-122">GetAt 方法</span><span class="sxs-lookup"><span data-stu-id="860c4-122">GetAt Method</span></span>

<span data-ttu-id="860c4-123">從集合中的指定位置取得物件。</span><span class="sxs-lookup"><span data-stu-id="860c4-123">Gets an object from a specified location in the collection.</span></span>

<span data-ttu-id="860c4-124">**泛型語法**</span><span class="sxs-lookup"><span data-stu-id="860c4-124">**Generic Syntax**</span></span>


```C++
HRESULT GetAt(
  [in]           UINT32 index,
  [out, retval]  Object **object
);
```



<span data-ttu-id="860c4-125">**說明**</span><span class="sxs-lookup"><span data-stu-id="860c4-125">**Description**</span></span>

<span data-ttu-id="860c4-126">將儲存在集合 *位置的物件，寫入至\*\*物件* 所參考的變數。</span><span class="sxs-lookup"><span data-stu-id="860c4-126">Writes the object that is stored at the collection's location specified by *index* to the variable referenced by *object*.</span></span> <span data-ttu-id="860c4-127">這個動作不會變更集合的內容。</span><span class="sxs-lookup"><span data-stu-id="860c4-127">This action does not change the collection's contents.</span></span> <span data-ttu-id="860c4-128">下圖說明此程序。</span><span class="sxs-lookup"><span data-stu-id="860c4-128">The following diagram illustrates this process.</span></span>

![顯示 getat 如何從集合中抓取專案的圖表](images/generic-getat.png)

## <a name="getcount-method"></a><span data-ttu-id="860c4-130">GetCount 方法</span><span class="sxs-lookup"><span data-stu-id="860c4-130">GetCount Method</span></span>

<span data-ttu-id="860c4-131">取得儲存在集合中的物件數目。</span><span class="sxs-lookup"><span data-stu-id="860c4-131">Gets the number of objects stored in the collection.</span></span>

<span data-ttu-id="860c4-132">**泛型語法**</span><span class="sxs-lookup"><span data-stu-id="860c4-132">**Generic Syntax**</span></span>


```C++
HRESULT GetCount(
  [out, retval]  UINT32 *count
);
```



<span data-ttu-id="860c4-133">**說明**</span><span class="sxs-lookup"><span data-stu-id="860c4-133">**Description**</span></span>

<span data-ttu-id="860c4-134">將目前儲存在集合中的物件數目寫入至 *count* 所參考的變數中。</span><span class="sxs-lookup"><span data-stu-id="860c4-134">Writes the number of objects that are currently stored in the collection into the variable referenced by *count*.</span></span> <span data-ttu-id="860c4-135">這個動作不會變更集合的內容。</span><span class="sxs-lookup"><span data-stu-id="860c4-135">This action does not change the collection's contents.</span></span> <span data-ttu-id="860c4-136">下圖說明此程序。</span><span class="sxs-lookup"><span data-stu-id="860c4-136">The following diagram illustrates this process.</span></span>

![此圖顯示 getcount 如何取得集合中的專案數](images/generic-getcount.png)

## <a name="insertat-method"></a><span data-ttu-id="860c4-138">InsertAt 方法</span><span class="sxs-lookup"><span data-stu-id="860c4-138">InsertAt Method</span></span>

<span data-ttu-id="860c4-139">將物件插入集合中指定的位置。</span><span class="sxs-lookup"><span data-stu-id="860c4-139">Inserts an object at a specified location of the collection.</span></span>

<span data-ttu-id="860c4-140">**泛型語法**</span><span class="sxs-lookup"><span data-stu-id="860c4-140">**Generic Syntax**</span></span>


```C++
HRESULT InsertAt(
  [in]  UINT32 index,
  [in]  Object *object
);
```



<span data-ttu-id="860c4-141">**說明**</span><span class="sxs-lookup"><span data-stu-id="860c4-141">**Description**</span></span>

<span data-ttu-id="860c4-142">在 *物件* 中傳遞的物件會插入至集合中 *索引* 所指定的位置。</span><span class="sxs-lookup"><span data-stu-id="860c4-142">The object that is passed in *object* is inserted into the collection at the location specified by *index*.</span></span> <span data-ttu-id="860c4-143">在插入新的 *物件* 之前，此方法會將先前已佔用位置的物件移至 1 *，並移動\*\*索引* 後面的所有介面指標。</span><span class="sxs-lookup"><span data-stu-id="860c4-143">Before inserting the new *object*, this method moves by 1 the object that has previously occupied the location at *index* and moves all interface pointers subsequent to *index*.</span></span> <span data-ttu-id="860c4-144">下圖說明此程序。</span><span class="sxs-lookup"><span data-stu-id="860c4-144">The following diagram illustrates this process.</span></span>

![顯示 insertat 如何將專案加入至集合的圖表](images/generic-insertat.png)

## <a name="removeat-method"></a><span data-ttu-id="860c4-146">RemoveAt 方法</span><span class="sxs-lookup"><span data-stu-id="860c4-146">RemoveAt Method</span></span>

<span data-ttu-id="860c4-147">從集合中的指定位置移除物件。</span><span class="sxs-lookup"><span data-stu-id="860c4-147">Removes the object from a specified location in the collection.</span></span>

<span data-ttu-id="860c4-148">**泛型語法**</span><span class="sxs-lookup"><span data-stu-id="860c4-148">**Generic Syntax**</span></span>


```C++
HRESULT RemoveAt(
  [in]  UINT32 index
);
```



<span data-ttu-id="860c4-149">**說明**</span><span class="sxs-lookup"><span data-stu-id="860c4-149">**Description**</span></span>

<span data-ttu-id="860c4-150">這個方法會從 *索引* 所指定的位置釋出物件，然後藉由減少 *索引* 後面每個指標的索引，來壓縮集合。</span><span class="sxs-lookup"><span data-stu-id="860c4-150">This method releases the object from the location specified by *index*, then compacts the collection by reducing by 1 the index of each pointer subsequent to *index*.</span></span> <span data-ttu-id="860c4-151">下圖說明此程序。</span><span class="sxs-lookup"><span data-stu-id="860c4-151">The following diagram illustrates this process.</span></span>

![顯示 removeat 如何從集合中移除專案的圖表](images/generic-removeat.png)

## <a name="setat-method"></a><span data-ttu-id="860c4-153">SetAt 方法</span><span class="sxs-lookup"><span data-stu-id="860c4-153">SetAt Method</span></span>

<span data-ttu-id="860c4-154">取代集合中位於指定位置的物件。</span><span class="sxs-lookup"><span data-stu-id="860c4-154">Replaces the object at a specified location in the collection.</span></span>

<span data-ttu-id="860c4-155">**泛型語法**</span><span class="sxs-lookup"><span data-stu-id="860c4-155">**Generic Syntax**</span></span>


```C++
HRESULT SetAt(
  [in]  UINT32 index,
  [in]  Object *object
);
```



<span data-ttu-id="860c4-156">**說明**</span><span class="sxs-lookup"><span data-stu-id="860c4-156">**Description**</span></span>

<span data-ttu-id="860c4-157">這個方法會先在 *索引* 所參考的位置釋出物件，然後以 *物件* 中所傳遞的物件來取代該物件。</span><span class="sxs-lookup"><span data-stu-id="860c4-157">This method first releases the object at the location referenced by *index*, then replaces that object with the one that is passed in *object*.</span></span> <span data-ttu-id="860c4-158">下圖說明此程序。</span><span class="sxs-lookup"><span data-stu-id="860c4-158">The following diagram illustrates this process.</span></span>

![此圖顯示 setat 如何取代集合中的專案](images/generic-setat.png)

## <a name="see-also"></a><span data-ttu-id="860c4-160">另請參閱</span><span class="sxs-lookup"><span data-stu-id="860c4-160">See Also</span></span>

<dl>

[<span data-ttu-id="860c4-161">**IXpsOMColorProfileResourceCollection**</span><span class="sxs-lookup"><span data-stu-id="860c4-161">**IXpsOMColorProfileResourceCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcolorprofileresourcecollection)  
[<span data-ttu-id="860c4-162">**IXpsOMDashCollection**</span><span class="sxs-lookup"><span data-stu-id="860c4-162">**IXpsOMDashCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdashcollection)  
[<span data-ttu-id="860c4-163">**IXpsOMDocumentCollection**</span><span class="sxs-lookup"><span data-stu-id="860c4-163">**IXpsOMDocumentCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentcollection)  
[<span data-ttu-id="860c4-164">**IXpsOMFontResourceCollection**</span><span class="sxs-lookup"><span data-stu-id="860c4-164">**IXpsOMFontResourceCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomfontresourcecollection)  
[<span data-ttu-id="860c4-165">**IXpsOMGeometryFigureCollection**</span><span class="sxs-lookup"><span data-stu-id="860c4-165">**IXpsOMGeometryFigureCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigurecollection)  
[<span data-ttu-id="860c4-166">**IXpsOMGradientStopCollection**</span><span class="sxs-lookup"><span data-stu-id="860c4-166">**IXpsOMGradientStopCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgradientstopcollection)  
[<span data-ttu-id="860c4-167">**IXpsOMImageResourceCollection**</span><span class="sxs-lookup"><span data-stu-id="860c4-167">**IXpsOMImageResourceCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimageresourcecollection)  
[<span data-ttu-id="860c4-168">**IXpsOMNameCollection**</span><span class="sxs-lookup"><span data-stu-id="860c4-168">**IXpsOMNameCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomnamecollection)  
[<span data-ttu-id="860c4-169">**IXpsOMPageReferenceCollection**</span><span class="sxs-lookup"><span data-stu-id="860c4-169">**IXpsOMPageReferenceCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereferencecollection)  
[<span data-ttu-id="860c4-170">**IXpsOMPartUriCollection**</span><span class="sxs-lookup"><span data-stu-id="860c4-170">**IXpsOMPartUriCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomparturicollection)  
[<span data-ttu-id="860c4-171">**IXpsOMRemoteDictionaryResourceCollection**</span><span class="sxs-lookup"><span data-stu-id="860c4-171">**IXpsOMRemoteDictionaryResourceCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomremotedictionaryresourcecollection)  
[<span data-ttu-id="860c4-172">**IXpsOMSignatureBlockResourceCollection**</span><span class="sxs-lookup"><span data-stu-id="860c4-172">**IXpsOMSignatureBlockResourceCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomsignatureblockresourcecollection)  
[<span data-ttu-id="860c4-173">**IXpsOMVisualCollection**</span><span class="sxs-lookup"><span data-stu-id="860c4-173">**IXpsOMVisualCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualcollection)  
[<span data-ttu-id="860c4-174">**IXpsSignatureBlockCollection**</span><span class="sxs-lookup"><span data-stu-id="860c4-174">**IXpsSignatureBlockCollection**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignatureblockcollection)  
[<span data-ttu-id="860c4-175">**IXpsSignatureCollection**</span><span class="sxs-lookup"><span data-stu-id="860c4-175">**IXpsSignatureCollection**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturecollection)  
[<span data-ttu-id="860c4-176">**IXpsSignatureRequestCollection**</span><span class="sxs-lookup"><span data-stu-id="860c4-176">**IXpsSignatureRequestCollection**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturerequestcollection)  
</dl>

 

 



