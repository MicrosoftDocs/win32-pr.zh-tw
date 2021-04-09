---
description: 代表物件樹狀結構中建立為筆跡分析一部分的節點。
ms.assetid: 44ef4401-cb14-4348-9ed8-b11a40d04940
title: 'ICoNtextNode 介面 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 2dbc9d7a0c1cc6ededf5d59585c806b54d6cfa32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026251"
---
# <a name="icontextnode-interface"></a><span data-ttu-id="fb493-103">ICoNtextNode 介面</span><span class="sxs-lookup"><span data-stu-id="fb493-103">IContextNode interface</span></span>

<span data-ttu-id="fb493-104">代表物件樹狀結構中建立為筆跡分析一部分的節點。</span><span class="sxs-lookup"><span data-stu-id="fb493-104">Represents a node in a tree of objects that are created as part of ink analysis.</span></span>

## <a name="members"></a><span data-ttu-id="fb493-105">成員</span><span class="sxs-lookup"><span data-stu-id="fb493-105">Members</span></span>

<span data-ttu-id="fb493-106">**ICoNtextNode** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="fb493-106">The **IContextNode** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="fb493-107">**ICoNtextNode** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="fb493-107">**IContextNode** also has these types of members:</span></span>

-   [<span data-ttu-id="fb493-108">方法</span><span class="sxs-lookup"><span data-stu-id="fb493-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="fb493-109">方法</span><span class="sxs-lookup"><span data-stu-id="fb493-109">Methods</span></span>

<span data-ttu-id="fb493-110">**ICoNtextNode** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="fb493-110">The **IContextNode** interface has these methods.</span></span>



| <span data-ttu-id="fb493-111">方法</span><span class="sxs-lookup"><span data-stu-id="fb493-111">Method</span></span>                                                                                  | <span data-ttu-id="fb493-112">描述</span><span class="sxs-lookup"><span data-stu-id="fb493-112">Description</span></span>                                                                                                                                                                                                                   |
|:----------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fb493-113">**AddCoNtextLink**</span><span class="sxs-lookup"><span data-stu-id="fb493-113">**AddContextLink**</span></span>](icontextnode-addcontextlink.md)                                   | <span data-ttu-id="fb493-114">將新的 [**ICoNtextLink**](icontextlink.md) 加入至 **ICoNtextNode** 物件的內容連結集合。</span><span class="sxs-lookup"><span data-stu-id="fb493-114">Adds a new [**IContextLink**](icontextlink.md) to the **IContextNode** object's context link collection.</span></span><br/>                                                                                                          |
| [<span data-ttu-id="fb493-115">**AddPropertyData**</span><span class="sxs-lookup"><span data-stu-id="fb493-115">**AddPropertyData**</span></span>](icontextnode-addpropertydata.md)                                 | <span data-ttu-id="fb493-116">新增應用程式特定資料的片段。</span><span class="sxs-lookup"><span data-stu-id="fb493-116">Adds a piece of application-specific data.</span></span><br/>                                                                                                                                                                         |
| [<span data-ttu-id="fb493-117">**確認**</span><span class="sxs-lookup"><span data-stu-id="fb493-117">**Confirm**</span></span>](icontextnode-confirm.md)                                                 | <span data-ttu-id="fb493-118">修改確認類型，以控制 [**IInkAnalyzer**](iinkanalyzer.md) 物件可變更的 **ICoNtextNode** 內容。</span><span class="sxs-lookup"><span data-stu-id="fb493-118">Modifies the confirmation type, which controls what the [**IInkAnalyzer**](iinkanalyzer.md) object can change about the **IContextNode**.</span></span><br/>                                                                         |
| [<span data-ttu-id="fb493-119">**ContainsPropertyData**</span><span class="sxs-lookup"><span data-stu-id="fb493-119">**ContainsPropertyData**</span></span>](icontextnode-containspropertydata.md)                       | <span data-ttu-id="fb493-120">判斷 **ICoNtextNode** 物件是否包含儲存在指定之識別碼下的資料。</span><span class="sxs-lookup"><span data-stu-id="fb493-120">Determines whether the **IContextNode** object contains data stored under the specified identifier.</span></span><br/>                                                                                                                |
| [<span data-ttu-id="fb493-121">**CreatePartiallyPopulatedSubNode**</span><span class="sxs-lookup"><span data-stu-id="fb493-121">**CreatePartiallyPopulatedSubNode**</span></span>](icontextnode-createpartiallypopulatedsubnode.md) | <span data-ttu-id="fb493-122">建立子 **ICoNtextNode** 物件，其中只包含型別、識別碼和位置的資訊。</span><span class="sxs-lookup"><span data-stu-id="fb493-122">Creates a child **IContextNode** object that contains only information on type, identifier, and location.</span></span><br/>                                                                                                          |
| [<span data-ttu-id="fb493-123">**CreateSubNode**</span><span class="sxs-lookup"><span data-stu-id="fb493-123">**CreateSubNode**</span></span>](icontextnode-createsubnode.md)                                     | <span data-ttu-id="fb493-124">建立新的子 **ICoNtextNode** 物件。</span><span class="sxs-lookup"><span data-stu-id="fb493-124">Creates a new child **IContextNode** object.</span></span><br/>                                                                                                                                                                       |
| [<span data-ttu-id="fb493-125">**DeleteCoNtextLink**</span><span class="sxs-lookup"><span data-stu-id="fb493-125">**DeleteContextLink**</span></span>](icontextnode-deletecontextlink.md)                             | <span data-ttu-id="fb493-126">從 **ICoNtextNode** 物件的連結集合中刪除 [**ICoNtextLink**](icontextlink.md)物件。</span><span class="sxs-lookup"><span data-stu-id="fb493-126">Deletes an [**IContextLink**](icontextlink.md) object from the **IContextNode** object's link collection.</span></span><br/>                                                                                                         |
| [<span data-ttu-id="fb493-127">**DeleteSubNode**</span><span class="sxs-lookup"><span data-stu-id="fb493-127">**DeleteSubNode**</span></span>](icontextnode-deletesubnode.md)                                     | <span data-ttu-id="fb493-128">移除子 **ICoNtextNode**。</span><span class="sxs-lookup"><span data-stu-id="fb493-128">Removes a child **IContextNode**.</span></span><br/>                                                                                                                                                                                  |
| [<span data-ttu-id="fb493-129">**GetCoNtextLinks**</span><span class="sxs-lookup"><span data-stu-id="fb493-129">**GetContextLinks**</span></span>](icontextnode-getcontextlinks.md)                                 | <span data-ttu-id="fb493-130">抓取 [**ICoNtextLink**](icontextlink.md) 物件的集合，這些物件表示與其他 **ICoNtextNode** 物件的關聯性。</span><span class="sxs-lookup"><span data-stu-id="fb493-130">Retrieves a collection of [**IContextLink**](icontextlink.md) objects that represents relationships with other **IContextNode** objects.</span></span><br/>                                                                          |
| [<span data-ttu-id="fb493-131">**GetId**</span><span class="sxs-lookup"><span data-stu-id="fb493-131">**GetId**</span></span>](icontextnode-getid.md)                                                     | <span data-ttu-id="fb493-132">捕獲 **ICoNtextNode** 物件的識別碼。</span><span class="sxs-lookup"><span data-stu-id="fb493-132">Retrieves the identifier for the **IContextNode** object.</span></span><br/>                                                                                                                                                          |
| [<span data-ttu-id="fb493-133">**GetLocation**</span><span class="sxs-lookup"><span data-stu-id="fb493-133">**GetLocation**</span></span>](icontextnode-getlocation.md)                                         | <span data-ttu-id="fb493-134">抓取 **ICoNtextNode** 物件的位置和大小。</span><span class="sxs-lookup"><span data-stu-id="fb493-134">Retrieves the position and size of the **IContextNode** object.</span></span><br/>                                                                                                                                                    |
| [<span data-ttu-id="fb493-135">**GetParentNode**</span><span class="sxs-lookup"><span data-stu-id="fb493-135">**GetParentNode**</span></span>](icontextnode-getparentnode.md)                                     | <span data-ttu-id="fb493-136">在內容節點樹狀結構中，捕獲此 **ICoNtextNode** 的父節點。</span><span class="sxs-lookup"><span data-stu-id="fb493-136">Retrieves the parent node of this **IContextNode** in the context node tree.</span></span><br/>                                                                                                                                       |
| [<span data-ttu-id="fb493-137">**GetPartiallyPopulated**</span><span class="sxs-lookup"><span data-stu-id="fb493-137">**GetPartiallyPopulated**</span></span>](icontextnode-getpartiallypopulated.md)                     | <span data-ttu-id="fb493-138">抓取值，這個值會指出 **ICoNtextNode** 物件是否已部分擴展或完整填入。</span><span class="sxs-lookup"><span data-stu-id="fb493-138">Retrieves the value that indicates whether an **IContextNode** object is partially populated or fully populated.</span></span><br/>                                                                                                   |
| [<span data-ttu-id="fb493-139">**GetPropertyData**</span><span class="sxs-lookup"><span data-stu-id="fb493-139">**GetPropertyData**</span></span>](icontextnode-getpropertydata.md)                                 | <span data-ttu-id="fb493-140">取得指定之識別碼的應用程式特定資料或其他屬性資料。</span><span class="sxs-lookup"><span data-stu-id="fb493-140">Retrieves application-specific data or other property data given the specified identifier.</span></span><br/>                                                                                                                         |
| [<span data-ttu-id="fb493-141">**GetPropertyDataIds**</span><span class="sxs-lookup"><span data-stu-id="fb493-141">**GetPropertyDataIds**</span></span>](icontextnode-getpropertydataids.md)                           | <span data-ttu-id="fb493-142">抓取具有屬性資料的識別碼。</span><span class="sxs-lookup"><span data-stu-id="fb493-142">Retrieves the identifiers for which there is property data.</span></span><br/>                                                                                                                                                        |
| [<span data-ttu-id="fb493-143">**GetStrokeCount**</span><span class="sxs-lookup"><span data-stu-id="fb493-143">**GetStrokeCount**</span></span>](icontextnode-getstrokecount.md)                                   | <span data-ttu-id="fb493-144">捕獲與 **ICoNtextNode** 物件相關聯的筆劃數目。</span><span class="sxs-lookup"><span data-stu-id="fb493-144">Retrieves the number of strokes associated with the **IContextNode** object.</span></span><br/>                                                                                                                                       |
| [<span data-ttu-id="fb493-145">**GetStrokeId**</span><span class="sxs-lookup"><span data-stu-id="fb493-145">**GetStrokeId**</span></span>](icontextnode-getstrokeid.md)                                         | <span data-ttu-id="fb493-146">抓取 **ICoNtextNode** 物件內索引值所參考之筆劃的筆觸識別碼。</span><span class="sxs-lookup"><span data-stu-id="fb493-146">Retrieves the stroke identifier for the stroke referenced by an index value within the **IContextNode** object.</span></span><br/>                                                                                                    |
| [<span data-ttu-id="fb493-147">**GetStrokeIds**</span><span class="sxs-lookup"><span data-stu-id="fb493-147">**GetStrokeIds**</span></span>](icontextnode-getstrokeids.md)                                       | <span data-ttu-id="fb493-148">抓取 **ICoNtextNode** 物件內筆劃的識別碼陣列。</span><span class="sxs-lookup"><span data-stu-id="fb493-148">Retrieves an array of identifiers for the strokes within the **IContextNode** object.</span></span><br/>                                                                                                                              |
| [<span data-ttu-id="fb493-149">**GetStrokePacketDataById**</span><span class="sxs-lookup"><span data-stu-id="fb493-149">**GetStrokePacketDataById**</span></span>](icontextnode-getstrokepacketdatabyid.md)                 | <span data-ttu-id="fb493-150">取得陣列，其中包含指定之筆劃的封包屬性資料。</span><span class="sxs-lookup"><span data-stu-id="fb493-150">Retrieves an array containing the packet property data for the specified stroke.</span></span><br/>                                                                                                                                   |
| [<span data-ttu-id="fb493-151">**GetStrokePacketDescriptionById**</span><span class="sxs-lookup"><span data-stu-id="fb493-151">**GetStrokePacketDescriptionById**</span></span>](icontextnode-getstrokepacketdescriptionbyid.md)   | <span data-ttu-id="fb493-152">取得陣列，其中包含指定之筆劃的封包屬性識別碼。</span><span class="sxs-lookup"><span data-stu-id="fb493-152">Retrieves an array containing the packet property identifiers for the specified stroke.</span></span><br/>                                                                                                                            |
| [<span data-ttu-id="fb493-153">**GetSubNodes**</span><span class="sxs-lookup"><span data-stu-id="fb493-153">**GetSubNodes**</span></span>](icontextnode-getsubnodes.md)                                         | <span data-ttu-id="fb493-154">抓取 **ICoNtextNode** 物件的直接子節點。</span><span class="sxs-lookup"><span data-stu-id="fb493-154">Retrieves the direct child nodes of the **IContextNode** object.</span></span><br/>                                                                                                                                                   |
| [<span data-ttu-id="fb493-155">**GetType**</span><span class="sxs-lookup"><span data-stu-id="fb493-155">**GetType**</span></span>](icontextnode-gettype.md)                                                 | <span data-ttu-id="fb493-156">捕獲 **ICoNtextNode** 物件的型別。</span><span class="sxs-lookup"><span data-stu-id="fb493-156">Retrieves the type of the **IContextNode** object.</span></span><br/>                                                                                                                                                                 |
| [<span data-ttu-id="fb493-157">**GetTypeName**</span><span class="sxs-lookup"><span data-stu-id="fb493-157">**GetTypeName**</span></span>](icontextnode-gettypename.md)                                         | <span data-ttu-id="fb493-158">抓取這個 **ICoNtextNode** 的人們看得懂的型別名稱。</span><span class="sxs-lookup"><span data-stu-id="fb493-158">Retrieves a human-readable type name of this **IContextNode**.</span></span><br/>                                                                                                                                                     |
| [<span data-ttu-id="fb493-159">**IsConfirmed**</span><span class="sxs-lookup"><span data-stu-id="fb493-159">**IsConfirmed**</span></span>](icontextnode-isconfirmed.md)                                         | <span data-ttu-id="fb493-160">抓取指出是否已確認 **ICoNtextNode** 物件的值。</span><span class="sxs-lookup"><span data-stu-id="fb493-160">Retrieves a value that indicates whether the **IContextNode** object is confirmed.</span></span> <span data-ttu-id="fb493-161">[**IInkAnalyzer**](iinkanalyzer.md) 無法變更已確認 **ICoNtextNode** 物件的節點類型和相關聯的筆劃。</span><span class="sxs-lookup"><span data-stu-id="fb493-161">[**IInkAnalyzer**](iinkanalyzer.md) cannot change the node type and associated strokes for confirmed **IContextNode** objects.</span></span><br/> |
| [<span data-ttu-id="fb493-162">**LoadPropertiesData**</span><span class="sxs-lookup"><span data-stu-id="fb493-162">**LoadPropertiesData**</span></span>](icontextnode-loadpropertiesdata.md)                           | <span data-ttu-id="fb493-163">針對先前使用 [**ICoNtextNode：： SavePropertiesData**](icontextnode-savepropertiesdata.md)建立的位元組陣列，重新建立應用程式特定和內部屬性資料。</span><span class="sxs-lookup"><span data-stu-id="fb493-163">Recreates the application-specific and internal property data for an array of bytes that was previously created with [**IContextNode::SavePropertiesData**](icontextnode-savepropertiesdata.md).</span></span><br/>                  |
| [<span data-ttu-id="fb493-164">**MoveSubNodeToPosition**</span><span class="sxs-lookup"><span data-stu-id="fb493-164">**MoveSubNodeToPosition**</span></span>](icontextnode-movesubnodetoposition.md)                     | <span data-ttu-id="fb493-165">將指定的子 **ICoNtextNode** 物件重新排序為指定的索引。</span><span class="sxs-lookup"><span data-stu-id="fb493-165">Reorders a specified child **IContextNode** object to the specified index.</span></span><br/>                                                                                                                                         |
| [<span data-ttu-id="fb493-166">**RemovePropertyData**</span><span class="sxs-lookup"><span data-stu-id="fb493-166">**RemovePropertyData**</span></span>](icontextnode-removepropertydata.md)                           | <span data-ttu-id="fb493-167">移除應用程式特定的資料片段。</span><span class="sxs-lookup"><span data-stu-id="fb493-167">Removes a piece of application-specific data.</span></span><br/>                                                                                                                                                                      |
| [<span data-ttu-id="fb493-168">**父**</span><span class="sxs-lookup"><span data-stu-id="fb493-168">**Reparent**</span></span>](icontextnode-reparent.md)                                               | <span data-ttu-id="fb493-169">將這個 **ICoNtextNode** 物件從其父內容節點的子節點集合移至指定的內容節點的子節點集合。</span><span class="sxs-lookup"><span data-stu-id="fb493-169">Moves this **IContextNode** object from its parent context node's subnodes collection to the specified context node's subnodes collection.</span></span><br/>                                                                         |
| [<span data-ttu-id="fb493-170">**ReparentStrokeByIdToNode**</span><span class="sxs-lookup"><span data-stu-id="fb493-170">**ReparentStrokeByIdToNode**</span></span>](icontextnode-reparentstrokebyidtonode.md)               | <span data-ttu-id="fb493-171">將筆劃資料從此 **ICoNtextNode** 移動到指定的 **ICoNtextNode**。</span><span class="sxs-lookup"><span data-stu-id="fb493-171">Moves stroke data from this **IContextNode** to the specified **IContextNode**.</span></span><br/>                                                                                                                                    |
| [<span data-ttu-id="fb493-172">**SavePropertiesData**</span><span class="sxs-lookup"><span data-stu-id="fb493-172">**SavePropertiesData**</span></span>](icontextnode-savepropertiesdata.md)                           | <span data-ttu-id="fb493-173">抓取位元組陣列，其中包含此 **ICoNtextNode** 的應用程式特定和內部屬性資料。</span><span class="sxs-lookup"><span data-stu-id="fb493-173">Retrieves an array of bytes that contains the application-specific and internal property data for this **IContextNode**.</span></span><br/>                                                                                           |
| [<span data-ttu-id="fb493-174">**SetLocation**</span><span class="sxs-lookup"><span data-stu-id="fb493-174">**SetLocation**</span></span>](icontextnode-setlocation.md)                                         | <span data-ttu-id="fb493-175">更新此 **ICoNtextNode** 的位置和大小。</span><span class="sxs-lookup"><span data-stu-id="fb493-175">Updates the position and size of this **IContextNode**.</span></span><br/>                                                                                                                                                            |
| [<span data-ttu-id="fb493-176">**SetPartiallyPopulated**</span><span class="sxs-lookup"><span data-stu-id="fb493-176">**SetPartiallyPopulated**</span></span>](icontextnode-setpartiallypopulated.md)                     | <span data-ttu-id="fb493-177">修改指出此 **ICoNtextNode** 為部分或完整擴展的值。</span><span class="sxs-lookup"><span data-stu-id="fb493-177">Modifies the value that indicates whether this **IContextNode** is partially or fully populated.</span></span><br/>                                                                                                                   |
| [<span data-ttu-id="fb493-178">**SetStrokes**</span><span class="sxs-lookup"><span data-stu-id="fb493-178">**SetStrokes**</span></span>](icontextnode-setstrokes.md)                                           | <span data-ttu-id="fb493-179">將指定的筆觸與這個 **ICoNtextNode** 相關聯。</span><span class="sxs-lookup"><span data-stu-id="fb493-179">Associates the specified strokes with this **IContextNode**.</span></span><br/>                                                                                                                                                       |



 

## <a name="remarks"></a><span data-ttu-id="fb493-180">備註</span><span class="sxs-lookup"><span data-stu-id="fb493-180">Remarks</span></span>

<span data-ttu-id="fb493-181">節點的類型在 [內容節點類型](context-node-types.md) 常數中有描述。</span><span class="sxs-lookup"><span data-stu-id="fb493-181">The types of nodes are described in the [Context Node Types](context-node-types.md) constants.</span></span>

## <a name="examples"></a><span data-ttu-id="fb493-182">範例</span><span class="sxs-lookup"><span data-stu-id="fb493-182">Examples</span></span>

<span data-ttu-id="fb493-183">下列範例顯示檢查 **ICoNtextNode** 的方法;方法會執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="fb493-183">The following example shows a method that examines an **IContextNode**; the method does the following:</span></span>

-   <span data-ttu-id="fb493-184">取得內容節點的型別。</span><span class="sxs-lookup"><span data-stu-id="fb493-184">Gets the context node's type.</span></span> <span data-ttu-id="fb493-185">如果內容節點是未分類的筆墨、分析提示或自訂辨識器節點，則會呼叫 helper 方法來檢查節點類型的特定屬性。</span><span class="sxs-lookup"><span data-stu-id="fb493-185">If the context node is an unclassified ink, analysis hint, or custom recognizer node, it calls a helper method to examine specific properties of the node type.</span></span>
-   <span data-ttu-id="fb493-186">如果節點有子節點，它會藉由呼叫本身來檢查每個子節點。</span><span class="sxs-lookup"><span data-stu-id="fb493-186">If the node has subnodes, it examines each subnode by calling itself.</span></span>
-   <span data-ttu-id="fb493-187">如果節點是筆墨分葉節點，它會藉由呼叫 helper 方法來檢查節點的筆劃資料。</span><span class="sxs-lookup"><span data-stu-id="fb493-187">If the node is an ink leaf node, it examines the stroke data for the node by calling a helper method.</span></span>

<span data-ttu-id="fb493-188">下列 InkAnalysis API 可讓您建立包含筆墨單字和文字單字的行節點。</span><span class="sxs-lookup"><span data-stu-id="fb493-188">Ihe InkAnalysis API allows you to create a line node that contains ink words and text words.</span></span> <span data-ttu-id="fb493-189">不過，剖析器會忽略這些混合節點，並將它們視為外部節點。</span><span class="sxs-lookup"><span data-stu-id="fb493-189">However, the parser will ignore these mixed nodes and will treat them like foreign nodes.</span></span> <span data-ttu-id="fb493-190">這會影響使用者在此混合節點上或周圍書寫時偵測筆墨注釋的剖析精確度。</span><span class="sxs-lookup"><span data-stu-id="fb493-190">This will have impact the parsing accuracy of detecting ink annotations when the end user writes on or around this mixed node.</span></span>


```C++
HRESULT CMyClass::ExploreContextNode(
    IContextNode *pContextNode)
{
    // Check for certain types of context nodes.
    GUID ContextNodeType;
    HRESULT hr = pContextNode->GetType(&ContextNodeType);

    if (SUCCEEDED(hr))
    {
        if (IsEqualGUID(GUID_CNT_UNCLASSIFIEDINK, ContextNodeType))
        {
            // Call a helper method that explores unclassified ink nodes.
            hr = this->ExploreUnclassifiedInkNode(pContextNode);
        }
        else if (IsEqualGUID(GUID_CNT_ANALYSISHINT, ContextNodeType))
        {
            // Call a helper method that explores analysis hint nodes.
            hr = this->ExploreAnalysisHintNode(pContextNode);
        }
        else if (IsEqualGUID(GUID_CNT_CUSTOMRECOGNIZER, ContextNodeType))
        {
            // Call a helper method that explores custom recognizer nodes.
            hr = this->ExploreCustomRecognizerNode(pContextNode);
        }

        if (SUCCEEDED(hr))
        {
            // Check if this node is a branch or a leaf node.
            IContextNodes *pSubNodes = NULL;
            hr = pContextNode->GetSubNodes(&pSubNodes);

            if (SUCCEEDED(hr))
            {
                ULONG ulSubNodeCount;
                hr = pSubNodes->GetCount(&ulSubNodeCount);

                if (SUCCEEDED(hr))
                {
                    if (ulSubNodeCount > 0)
                    {
                        // This node has child nodes; explore each child node.
                        IContextNode *pSubNode = NULL;
                        for (ULONG index=0; index<ulSubNodeCount; index++)
                        {
                            hr = pSubNodes->GetContextNode(index, &pSubNode);

                            if (SUCCEEDED(hr))
                            {
                                // Recursive call to explore the child node of this
                                // context node.
                                hr = this->ExploreContextNode(pSubNode);
                            }

                            // Release this reference to the child context node.
                            if (pSubNode != NULL)
                            {
                                pSubNode->Release();
                                pSubNode = NULL;
                            }

                            if (FAILED(hr))
                            {
                                break;
                            }
                        }
                    }
                    else
                    {
                        // This is a leaf node. Check if it contains stroke data.
                        ULONG ulStrokeCount;
                        hr = pContextNode->GetStrokeCount(&ulStrokeCount);

                        if (SUCCEEDED(hr))
                        {
                            if (ulStrokeCount > 0)
                            {
                                // This node is an ink leaf node; call helper
                                // method that explores available stroke data.
                                hr = this->ExploreNodeStrokeData(pContextNode);
                            }
                        }
                    }
                }
            }

            // Release this reference to the subnodes collection.
            if (pSubNodes != NULL)
            {
                pSubNodes->Release();
                pSubNodes = NULL;
            }
        }
    }

    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="fb493-191">規格需求</span><span class="sxs-lookup"><span data-stu-id="fb493-191">Requirements</span></span>



| <span data-ttu-id="fb493-192">需求</span><span class="sxs-lookup"><span data-stu-id="fb493-192">Requirement</span></span> | <span data-ttu-id="fb493-193">值</span><span class="sxs-lookup"><span data-stu-id="fb493-193">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb493-194">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fb493-194">Minimum supported client</span></span><br/> | <span data-ttu-id="fb493-195">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fb493-195">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="fb493-196">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fb493-196">Minimum supported server</span></span><br/> | <span data-ttu-id="fb493-197">都不支援</span><span class="sxs-lookup"><span data-stu-id="fb493-197">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="fb493-198">標頭</span><span class="sxs-lookup"><span data-stu-id="fb493-198">Header</span></span><br/>                   | <dl> <span data-ttu-id="fb493-199"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="fb493-199"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="fb493-200">DLL</span><span class="sxs-lookup"><span data-stu-id="fb493-200">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fb493-201"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fb493-201"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="fb493-202">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fb493-202">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb493-203">**ICoNtextNodes**</span><span class="sxs-lookup"><span data-stu-id="fb493-203">**IContextNodes**</span></span>](icontextnodes.md)
</dt> <dt>

[<span data-ttu-id="fb493-204">內容節點類型</span><span class="sxs-lookup"><span data-stu-id="fb493-204">Context Node Types</span></span>](context-node-types.md)
</dt> <dt>

[<span data-ttu-id="fb493-205">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="fb493-205">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="fb493-206">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="fb493-206">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

