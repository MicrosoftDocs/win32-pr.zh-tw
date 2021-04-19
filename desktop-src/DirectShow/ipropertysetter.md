---
description: IPropertySetter 介面會設定 DirectShow 編輯服務 (DES) 效果或轉換的屬性。若要使用這個介面，請 (CLSID PropertySetter) 建立屬性 setter 物件的實例 \_ ，然後呼叫 IAMTimelineObj：： SetPropertySetter 方法，將它與效果或轉換產生關聯。 如需詳細資訊，請參閱使用效果和轉換。應用程式通常只需要呼叫 IPropertySetter：： ClearProps 方法來清除現有的屬性，並使用 IPropertySetter：： AddProp 方法來加入新的屬性。 其他 DES 元件會呼叫此介面上的其他方法。
ms.assetid: bee2abf2-0abc-4890-b1f2-7d0011444fbd
title: 'IPropertySetter 介面 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8f8aaadea2f0fb63287775294a7c61f01b3730df
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990684"
---
# <a name="ipropertysetter-interface"></a><span data-ttu-id="91d9d-105">IPropertySetter 介面</span><span class="sxs-lookup"><span data-stu-id="91d9d-105">IPropertySetter interface</span></span>

> [!Note]  
> <span data-ttu-id="91d9d-106">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="91d9d-106">\[Deprecated.</span></span> <span data-ttu-id="91d9d-107">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="91d9d-107">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="91d9d-108">`IPropertySetter`介面會設定[DirectShow 編輯服務](directshow-editing-services.md) (DES) 效果或轉換的屬性。</span><span class="sxs-lookup"><span data-stu-id="91d9d-108">The `IPropertySetter` interface sets properties on an effect or transition in [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span>

<span data-ttu-id="91d9d-109">若要使用這個介面，請 (CLSID PropertySetter) 建立屬性 setter 物件的實例 \_ ，然後呼叫 [**IAMTimelineObj：： SetPropertySetter**](iamtimelineobj-setpropertysetter.md) 方法，將它與效果或轉換產生關聯。</span><span class="sxs-lookup"><span data-stu-id="91d9d-109">To use this interface, create an instance of a property setter object (CLSID\_PropertySetter), and associate it with an effect or transition by calling the [**IAMTimelineObj::SetPropertySetter**](iamtimelineobj-setpropertysetter.md) method.</span></span> <span data-ttu-id="91d9d-110">如需詳細資訊，請參閱 [使用效果和轉換](working-with-effects-and-transitions.md)。</span><span class="sxs-lookup"><span data-stu-id="91d9d-110">For more information, see [Working with Effects and Transitions](working-with-effects-and-transitions.md).</span></span>

<span data-ttu-id="91d9d-111">通常，應用程式只需要呼叫 [**IPropertySetter：： ClearProps**](ipropertysetter-clearprops.md) 方法來清除現有的屬性，並使用 [**IPropertySetter：： AddProp**](ipropertysetter-addprop.md) 方法來加入新的屬性。</span><span class="sxs-lookup"><span data-stu-id="91d9d-111">Usually an application needs to call only the [**IPropertySetter::ClearProps**](ipropertysetter-clearprops.md) method to clear existing properties, and the [**IPropertySetter::AddProp**](ipropertysetter-addprop.md) method to add new properties.</span></span> <span data-ttu-id="91d9d-112">其他 DES 元件會呼叫此介面上的其他方法。</span><span class="sxs-lookup"><span data-stu-id="91d9d-112">The other methods on this interface are called by other DES components.</span></span>

## <a name="members"></a><span data-ttu-id="91d9d-113">成員</span><span class="sxs-lookup"><span data-stu-id="91d9d-113">Members</span></span>

<span data-ttu-id="91d9d-114">**IPropertySetter** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="91d9d-114">The **IPropertySetter** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="91d9d-115">**IPropertySetter** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="91d9d-115">**IPropertySetter** also has these types of members:</span></span>

-   [<span data-ttu-id="91d9d-116">方法</span><span class="sxs-lookup"><span data-stu-id="91d9d-116">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="91d9d-117">方法</span><span class="sxs-lookup"><span data-stu-id="91d9d-117">Methods</span></span>

<span data-ttu-id="91d9d-118">**IPropertySetter** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="91d9d-118">The **IPropertySetter** interface has these methods.</span></span>



| <span data-ttu-id="91d9d-119">方法</span><span class="sxs-lookup"><span data-stu-id="91d9d-119">Method</span></span>                                               | <span data-ttu-id="91d9d-120">描述</span><span class="sxs-lookup"><span data-stu-id="91d9d-120">Description</span></span>                                                                                                                                   |
|:-----------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="91d9d-121">**AddProp**</span><span class="sxs-lookup"><span data-stu-id="91d9d-121">**AddProp**</span></span>](ipropertysetter-addprop.md)           | <span data-ttu-id="91d9d-122">將屬性加入至屬性 setter，以及定義時間範圍內屬性值的時間值配對陣列。</span><span class="sxs-lookup"><span data-stu-id="91d9d-122">Adds a property to the property setter, with an array of time-value pairs defining the value of the property over a range of time.</span></span><br/> |
| [<span data-ttu-id="91d9d-123">**ClearProps**</span><span class="sxs-lookup"><span data-stu-id="91d9d-123">**ClearProps**</span></span>](ipropertysetter-clearprops.md)     | <span data-ttu-id="91d9d-124">清除屬性 setter 中的所有屬性資料。</span><span class="sxs-lookup"><span data-stu-id="91d9d-124">Clears all property data from the property setter.</span></span><br/>                                                                                 |
| [<span data-ttu-id="91d9d-125">**CloneProps**</span><span class="sxs-lookup"><span data-stu-id="91d9d-125">**CloneProps**</span></span>](ipropertysetter-cloneprops.md)     | <span data-ttu-id="91d9d-126">從這個屬性 setter 複製一組屬性，並將其加入至新的屬性 setter。</span><span class="sxs-lookup"><span data-stu-id="91d9d-126">Clones a set of properties from this property setter and adds them to a new property setter.</span></span><br/>                                       |
| [<span data-ttu-id="91d9d-127">**FreeProps**</span><span class="sxs-lookup"><span data-stu-id="91d9d-127">**FreeProps**</span></span>](ipropertysetter-freeprops.md)       | <span data-ttu-id="91d9d-128">釋放 [**IPropertySetter：： GetProps**](ipropertysetter-getprops.md) 方法所配置的資源。</span><span class="sxs-lookup"><span data-stu-id="91d9d-128">Frees resources allocated by the [**IPropertySetter::GetProps**](ipropertysetter-getprops.md) method.</span></span><br/>                             |
| [<span data-ttu-id="91d9d-129">**GetProps**</span><span class="sxs-lookup"><span data-stu-id="91d9d-129">**GetProps**</span></span>](ipropertysetter-getprops.md)         | <span data-ttu-id="91d9d-130">抓取這個物件上設定的屬性，以及其對應的值。</span><span class="sxs-lookup"><span data-stu-id="91d9d-130">Retrieves the properties set on this object, with their corresponding values.</span></span><br/>                                                      |
| [<span data-ttu-id="91d9d-131">**LoadFromBlob**</span><span class="sxs-lookup"><span data-stu-id="91d9d-131">**LoadFromBlob**</span></span>](ipropertysetter-loadfromblob.md) | <span data-ttu-id="91d9d-132">從持續性格式載入屬性資料。</span><span class="sxs-lookup"><span data-stu-id="91d9d-132">Loads property data from a persistence format.</span></span><br/>                                                                                     |
| [<span data-ttu-id="91d9d-133">**LoadXML**</span><span class="sxs-lookup"><span data-stu-id="91d9d-133">**LoadXML**</span></span>](ipropertysetter-loadxml.md)           | <span data-ttu-id="91d9d-134">載入以可延伸標記語言 (XML)  (XML) 表示的屬性資料。</span><span class="sxs-lookup"><span data-stu-id="91d9d-134">Loads property data expressed in Extensible Markup Language (XML).</span></span><br/>                                                                 |
| [<span data-ttu-id="91d9d-135">**PrintXML**</span><span class="sxs-lookup"><span data-stu-id="91d9d-135">**PrintXML**</span></span>](ipropertysetter-printxml.md)         | <span data-ttu-id="91d9d-136">將屬性資料轉換成 XML 字串。</span><span class="sxs-lookup"><span data-stu-id="91d9d-136">Converts property data into an XML string.</span></span><br/>                                                                                         |
| [<span data-ttu-id="91d9d-137">**SaveToBlob**</span><span class="sxs-lookup"><span data-stu-id="91d9d-137">**SaveToBlob**</span></span>](ipropertysetter-savetoblob.md)     | <span data-ttu-id="91d9d-138">將屬性資料儲存至保存格式。</span><span class="sxs-lookup"><span data-stu-id="91d9d-138">Saves the property data to a persistence format.</span></span><br/>                                                                                   |
| [<span data-ttu-id="91d9d-139">**SetProps**</span><span class="sxs-lookup"><span data-stu-id="91d9d-139">**SetProps**</span></span>](ipropertysetter-setprops.md)         | <span data-ttu-id="91d9d-140">將目標物件的屬性設定為指定時間的適當狀態。</span><span class="sxs-lookup"><span data-stu-id="91d9d-140">Sets the properties of the target object to the appropriate state for the specified time.</span></span><br/>                                          |



 

## <a name="remarks"></a><span data-ttu-id="91d9d-141">備註</span><span class="sxs-lookup"><span data-stu-id="91d9d-141">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="91d9d-142">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="91d9d-142">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="91d9d-143">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="91d9d-143">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="91d9d-144">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="91d9d-144">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="91d9d-145">規格需求</span><span class="sxs-lookup"><span data-stu-id="91d9d-145">Requirements</span></span>



| <span data-ttu-id="91d9d-146">需求</span><span class="sxs-lookup"><span data-stu-id="91d9d-146">Requirement</span></span> | <span data-ttu-id="91d9d-147">值</span><span class="sxs-lookup"><span data-stu-id="91d9d-147">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="91d9d-148">標頭</span><span class="sxs-lookup"><span data-stu-id="91d9d-148">Header</span></span><br/>  | <dl> <span data-ttu-id="91d9d-149"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="91d9d-149"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="91d9d-150">程式庫</span><span class="sxs-lookup"><span data-stu-id="91d9d-150">Library</span></span><br/> | <dl> <span data-ttu-id="91d9d-151"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="91d9d-151"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 
