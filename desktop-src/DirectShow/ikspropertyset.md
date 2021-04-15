---
description: IKsPropertySet 介面最初是設計為在 WDM 驅動程式上設定和抓取裝置屬性的有效方式，使用 KSProxy 將使用者模式 COM 方法呼叫轉譯為 WDM 串流類別驅動程式所使用的核心模式屬性集。 這個介面現在也用來嚴格傳遞軟體元件之間的資訊。在某些情況下，軟體元件必須執行此介面，否則 IKsControl 介面 (記載于 DirectShow DDK) 中。 例如，如果您要撰寫軟體 MPEG-2 解碼器以與 DVD 導覽器搭配使用，您必須執行這些介面的其中一個，也支援導覽器將傳送至該解碼器的 DVD 相關屬性集。 Pin 可能會支援其中一個介面，以允許其他 pin 或篩選器設定或抓取其屬性。請注意，此名稱的另一個介面存在於 dsound .h 標頭檔中。 這兩個介面不相容。 IKsControl 介面（記載于 DirectShow DDK）現在是在 WDM 驅動程式和使用者模式元件之間傳遞屬性集的建議介面。 .
ms.assetid: df26341d-f2d5-4a4e-954e-705e07415808
title: 'IKsPropertySet 介面 (Ksproxy .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IKsPropertySet
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
ms.openlocfilehash: 49a1f897d79a7514600f0c6553f931411aae8993
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104467454"
---
# <a name="ikspropertyset-interface"></a><span data-ttu-id="32aef-109">IKsPropertySet 介面</span><span class="sxs-lookup"><span data-stu-id="32aef-109">IKsPropertySet interface</span></span>

<span data-ttu-id="32aef-110">`IKsPropertySet`介面原本是設計為在 wdm 驅動程式上設定和取出裝置屬性的有效方式，使用 KSProxy 將使用者模式 COM 方法呼叫轉譯為 wdm 串流類別驅動程式所使用的核心模式屬性集。</span><span class="sxs-lookup"><span data-stu-id="32aef-110">The `IKsPropertySet` interface was originally designed as an efficient way to set and retrieve device properties on WDM drivers, using KSProxy to translate the user-mode COM method calls into the kernel-mode property sets used by WDM streaming class drivers.</span></span> <span data-ttu-id="32aef-111">這個介面現在也用來嚴格傳遞軟體元件之間的資訊。</span><span class="sxs-lookup"><span data-stu-id="32aef-111">This interface is now also used to pass information strictly between software components.</span></span>

<span data-ttu-id="32aef-112">在某些情況下，軟體元件必須執行此介面，否則 **IKsControl** 介面 (記載于 DirectShow DDK) 中。</span><span class="sxs-lookup"><span data-stu-id="32aef-112">In some cases, software components must implement either this interface, or else the **IKsControl** interface (documented in the DirectShow DDK).</span></span> <span data-ttu-id="32aef-113">例如，如果您要撰寫軟體 MPEG-2 解碼器以與 [DVD 導覽器](dvd-navigator-filter.md)搭配使用，您必須執行這些介面的其中一個，也支援導覽器將傳送至該解碼器的 DVD 相關屬性集。</span><span class="sxs-lookup"><span data-stu-id="32aef-113">For example, if you are writing a software MPEG-2 decoder for use with the [DVD Navigator](dvd-navigator-filter.md), you must implement one of these interfaces and also support the DVD-related property sets that the Navigator will send to the decoder.</span></span> <span data-ttu-id="32aef-114">Pin 可能會支援其中一個介面，以允許其他 pin 或篩選器設定或抓取其屬性。</span><span class="sxs-lookup"><span data-stu-id="32aef-114">Pins may support one of these interfaces to allow other pins or filters to set or retrieve their properties.</span></span>

> [!Note]  
> <span data-ttu-id="32aef-115">這個名稱的另一個介面存在於 dsound .h 標頭檔中。</span><span class="sxs-lookup"><span data-stu-id="32aef-115">Another interface by this name exists in the dsound.h header file.</span></span> <span data-ttu-id="32aef-116">這兩個介面不相容。</span><span class="sxs-lookup"><span data-stu-id="32aef-116">The two interfaces are not compatible.</span></span> <span data-ttu-id="32aef-117">**IKsControl** 介面（記載于 DirectShow DDK）現在是在 WDM 驅動程式和使用者模式元件之間傳遞屬性集的建議介面。</span><span class="sxs-lookup"><span data-stu-id="32aef-117">The **IKsControl** interface, documented in the DirectShow DDK, is now the recommended interface for passing property sets between WDM drivers and user mode components.</span></span>

 

## <a name="members"></a><span data-ttu-id="32aef-118">成員</span><span class="sxs-lookup"><span data-stu-id="32aef-118">Members</span></span>

<span data-ttu-id="32aef-119">**IKsPropertySet** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="32aef-119">The **IKsPropertySet** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="32aef-120">**IKsPropertySet** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="32aef-120">**IKsPropertySet** also has these types of members:</span></span>

-   [<span data-ttu-id="32aef-121">方法</span><span class="sxs-lookup"><span data-stu-id="32aef-121">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="32aef-122">方法</span><span class="sxs-lookup"><span data-stu-id="32aef-122">Methods</span></span>

<span data-ttu-id="32aef-123">**IKsPropertySet** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="32aef-123">The **IKsPropertySet** interface has these methods.</span></span>



| <span data-ttu-id="32aef-124">方法</span><span class="sxs-lookup"><span data-stu-id="32aef-124">Method</span></span>                                                  | <span data-ttu-id="32aef-125">描述</span><span class="sxs-lookup"><span data-stu-id="32aef-125">Description</span></span>                                                                          |
|:--------------------------------------------------------|:-------------------------------------------------------------------------------------|
| [<span data-ttu-id="32aef-126">**獲取**</span><span class="sxs-lookup"><span data-stu-id="32aef-126">**Get**</span></span>](ikspropertyset-get.md)                       | <span data-ttu-id="32aef-127">抓取屬性集 GUID 和屬性識別碼所識別的屬性。</span><span class="sxs-lookup"><span data-stu-id="32aef-127">Retrieves a property identified by a property set GUID and a property ID.</span></span><br/> |
| [<span data-ttu-id="32aef-128">**QuerySupported**</span><span class="sxs-lookup"><span data-stu-id="32aef-128">**QuerySupported**</span></span>](ikspropertyset-querysupported.md) | <span data-ttu-id="32aef-129">判斷物件是否支援指定的屬性集。</span><span class="sxs-lookup"><span data-stu-id="32aef-129">Determines whether an object supports a specified property set.</span></span><br/>           |
| [<span data-ttu-id="32aef-130">**設定**</span><span class="sxs-lookup"><span data-stu-id="32aef-130">**Set**</span></span>](ikspropertyset-set.md)                       | <span data-ttu-id="32aef-131">設定屬性集 GUID 和屬性識別碼所識別的屬性。</span><span class="sxs-lookup"><span data-stu-id="32aef-131">Sets a property identified by a property set GUID and a property ID.</span></span><br/>      |



 

## <a name="remarks"></a><span data-ttu-id="32aef-132">備註</span><span class="sxs-lookup"><span data-stu-id="32aef-132">Remarks</span></span>

<span data-ttu-id="32aef-133">您必須在 Ksproxy 之前包含 Ks。</span><span class="sxs-lookup"><span data-stu-id="32aef-133">You must include Ks.h before Ksproxy.h.</span></span>

## <a name="requirements"></a><span data-ttu-id="32aef-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="32aef-134">Requirements</span></span>



| <span data-ttu-id="32aef-135">需求</span><span class="sxs-lookup"><span data-stu-id="32aef-135">Requirement</span></span> | <span data-ttu-id="32aef-136">值</span><span class="sxs-lookup"><span data-stu-id="32aef-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="32aef-137">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="32aef-137">Minimum supported client</span></span><br/> | <span data-ttu-id="32aef-138">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="32aef-138">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="32aef-139">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="32aef-139">Minimum supported server</span></span><br/> | <span data-ttu-id="32aef-140">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="32aef-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="32aef-141">標頭</span><span class="sxs-lookup"><span data-stu-id="32aef-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="32aef-142"><dt>Ksproxy。h</dt></span><span class="sxs-lookup"><span data-stu-id="32aef-142"><dt>Ksproxy.h</dt></span></span> </dl>    |
| <span data-ttu-id="32aef-143">程式庫</span><span class="sxs-lookup"><span data-stu-id="32aef-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="32aef-144"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="32aef-144"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32aef-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="32aef-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32aef-146">屬性集</span><span class="sxs-lookup"><span data-stu-id="32aef-146">Property Sets</span></span>](property-sets.md)
</dt> </dl>

 

 
