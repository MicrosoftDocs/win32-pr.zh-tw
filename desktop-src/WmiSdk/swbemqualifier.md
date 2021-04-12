---
description: 您可以使用 SWbemQualifier 物件的屬性來代表 WMI 類別、實例、屬性或方法參數的單一限定詞。 VBScript CreateObject 呼叫無法建立這個物件。
ms.assetid: b5dbe98a-e1d8-4679-a563-c88760d08b79
ms.tgt_platform: multiple
title: 'SWbemQualifier 物件 (>wbemdisp.tlb) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemQualifier
- ISWbemQualifier
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 5e9a49832ffa1e38fbe6ee0f71e1f6a39c1b0ba2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192056"
---
# <a name="swbemqualifier-object"></a><span data-ttu-id="17a64-104">SWbemQualifier 物件</span><span class="sxs-lookup"><span data-stu-id="17a64-104">SWbemQualifier object</span></span>

<span data-ttu-id="17a64-105">您可以使用 **SWbemQualifier** 物件的屬性來代表 WMI 類別、實例、屬性或方法參數的單一限定詞。</span><span class="sxs-lookup"><span data-stu-id="17a64-105">You can use the properties of the **SWbemQualifier** object to represent a single qualifier of a WMI class, instance, property, or method parameter.</span></span> <span data-ttu-id="17a64-106">VBScript [CreateObject](creating-an-object-using-vbscript.md) 呼叫無法建立這個物件。</span><span class="sxs-lookup"><span data-stu-id="17a64-106">This object cannot be created by the VBScript [CreateObject](creating-an-object-using-vbscript.md) call.</span></span>

## <a name="members"></a><span data-ttu-id="17a64-107">成員</span><span class="sxs-lookup"><span data-stu-id="17a64-107">Members</span></span>

<span data-ttu-id="17a64-108">**SWbemQualifier** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="17a64-108">The **SWbemQualifier** object has these types of members:</span></span>

-   [<span data-ttu-id="17a64-109">屬性</span><span class="sxs-lookup"><span data-stu-id="17a64-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="17a64-110">屬性</span><span class="sxs-lookup"><span data-stu-id="17a64-110">Properties</span></span>

<span data-ttu-id="17a64-111">**SWbemQualifier** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="17a64-111">The **SWbemQualifier** object has these properties.</span></span>



| <span data-ttu-id="17a64-112">屬性</span><span class="sxs-lookup"><span data-stu-id="17a64-112">Property</span></span>                                                                       | <span data-ttu-id="17a64-113">存取類型</span><span class="sxs-lookup"><span data-stu-id="17a64-113">Access type</span></span>           | <span data-ttu-id="17a64-114">Description</span><span class="sxs-lookup"><span data-stu-id="17a64-114">Description</span></span>                                                                                           |
|:-------------------------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="17a64-115">**IsAmended**</span><span class="sxs-lookup"><span data-stu-id="17a64-115">**IsAmended**</span></span>](swbemqualifier-isamended.md)<br/>                       | <span data-ttu-id="17a64-116">唯讀</span><span class="sxs-lookup"><span data-stu-id="17a64-116">Read-only</span></span><br/>  | <span data-ttu-id="17a64-117">布林值，指出是否已使用合併作業來當地語系化此限定詞。</span><span class="sxs-lookup"><span data-stu-id="17a64-117">Boolean value that indicates if this qualifier has been localized using a merge operation.</span></span><br/> |
| [<span data-ttu-id="17a64-118">**IsLocal**</span><span class="sxs-lookup"><span data-stu-id="17a64-118">**IsLocal**</span></span>](swbemqualifier-islocal.md)<br/>                           | <span data-ttu-id="17a64-119">唯讀</span><span class="sxs-lookup"><span data-stu-id="17a64-119">Read-only</span></span><br/>  | <span data-ttu-id="17a64-120">指出此限定詞是否為本機的布林值。</span><span class="sxs-lookup"><span data-stu-id="17a64-120">Boolean value that indicates if this qualifier is local.</span></span><br/>                                   |
| [<span data-ttu-id="17a64-121">**IsOverridable**</span><span class="sxs-lookup"><span data-stu-id="17a64-121">**IsOverridable**</span></span>](swbemqualifier-isoverridable.md)<br/>               | <span data-ttu-id="17a64-122">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="17a64-122">Read/write</span></span><br/> | <span data-ttu-id="17a64-123">指出是否可以在傳播時覆寫此限定詞的布林值。</span><span class="sxs-lookup"><span data-stu-id="17a64-123">Boolean value that indicates if this qualifier can be overridden when propagated.</span></span><br/>          |
| [<span data-ttu-id="17a64-124">**Name**</span><span class="sxs-lookup"><span data-stu-id="17a64-124">**Name**</span></span>](swbemqualifier-name.md)<br/>                                 | <span data-ttu-id="17a64-125">唯讀</span><span class="sxs-lookup"><span data-stu-id="17a64-125">Read-only</span></span><br/>  | <span data-ttu-id="17a64-126">此辨識符號的名稱。</span><span class="sxs-lookup"><span data-stu-id="17a64-126">Name of this qualifier.</span></span><br/>                                                                    |
| [<span data-ttu-id="17a64-127">**PropagatesToInstance**</span><span class="sxs-lookup"><span data-stu-id="17a64-127">**PropagatesToInstance**</span></span>](swbemqualifier-propagatestoinstance.md)<br/> | <span data-ttu-id="17a64-128">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="17a64-128">Read/write</span></span><br/> | <span data-ttu-id="17a64-129">布林值，指出此限定詞是否可以傳播至實例。</span><span class="sxs-lookup"><span data-stu-id="17a64-129">Boolean value that indicates if this qualifier can be propagated to an instance.</span></span><br/>           |
| [<span data-ttu-id="17a64-130">**PropagatesToSubClass**</span><span class="sxs-lookup"><span data-stu-id="17a64-130">**PropagatesToSubClass**</span></span>](swbemqualifier-propagatestosubclass.md)<br/> | <span data-ttu-id="17a64-131">唯讀</span><span class="sxs-lookup"><span data-stu-id="17a64-131">Read-only</span></span><br/>  | <span data-ttu-id="17a64-132">指出是否可以將此限定詞傳播至子類別的布林值。</span><span class="sxs-lookup"><span data-stu-id="17a64-132">Boolean value that indicates if this qualifier can be propagated to a subclass.</span></span><br/>            |
| [<span data-ttu-id="17a64-133">**值**</span><span class="sxs-lookup"><span data-stu-id="17a64-133">**Value**</span></span>](swbemqualifier-value.md)<br/>                               | <span data-ttu-id="17a64-134">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="17a64-134">Read/write</span></span><br/> | <span data-ttu-id="17a64-135">此辨識符號的變異值。</span><span class="sxs-lookup"><span data-stu-id="17a64-135">Variant value of this qualifier.</span></span> <span data-ttu-id="17a64-136">這是此物件的預設屬性。</span><span class="sxs-lookup"><span data-stu-id="17a64-136">This is the default property of this object.</span></span><br/>              |



 

## <a name="requirements"></a><span data-ttu-id="17a64-137">規格需求</span><span class="sxs-lookup"><span data-stu-id="17a64-137">Requirements</span></span>



| <span data-ttu-id="17a64-138">需求</span><span class="sxs-lookup"><span data-stu-id="17a64-138">Requirement</span></span> | <span data-ttu-id="17a64-139">值</span><span class="sxs-lookup"><span data-stu-id="17a64-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="17a64-140">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="17a64-140">Minimum supported client</span></span><br/> | <span data-ttu-id="17a64-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="17a64-141">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="17a64-142">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="17a64-142">Minimum supported server</span></span><br/> | <span data-ttu-id="17a64-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="17a64-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="17a64-144">標頭</span><span class="sxs-lookup"><span data-stu-id="17a64-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="17a64-145"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="17a64-145"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="17a64-146">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="17a64-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="17a64-147"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="17a64-147"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="17a64-148">DLL</span><span class="sxs-lookup"><span data-stu-id="17a64-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="17a64-149"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="17a64-149"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="17a64-150">CLSID</span><span class="sxs-lookup"><span data-stu-id="17a64-150">CLSID</span></span><br/>                    | <span data-ttu-id="17a64-151">CLSID \_ SWbemQualifier</span><span class="sxs-lookup"><span data-stu-id="17a64-151">CLSID\_SWbemQualifier</span></span><br/>                                                        |
| <span data-ttu-id="17a64-152">IID</span><span class="sxs-lookup"><span data-stu-id="17a64-152">IID</span></span><br/>                      | <span data-ttu-id="17a64-153">IID \_ ISWbemQualifier</span><span class="sxs-lookup"><span data-stu-id="17a64-153">IID\_ISWbemQualifier</span></span><br/>                                                         |



## <a name="see-also"></a><span data-ttu-id="17a64-154">另請參閱</span><span class="sxs-lookup"><span data-stu-id="17a64-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17a64-155">腳本 API 物件</span><span class="sxs-lookup"><span data-stu-id="17a64-155">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> </dl>

 

 




