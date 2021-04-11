---
title: 選擇性方法
description: 選擇性方法
ms.assetid: 8cdb5686-177c-48c9-8315-e5921520007c
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 904aad26ecfba6396c9911b247443f9a956bca7f
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104093340"
---
# <a name="optional-methods"></a><span data-ttu-id="b0f75-103">選擇性方法</span><span class="sxs-lookup"><span data-stu-id="b0f75-103">Optional Methods</span></span>

<span data-ttu-id="b0f75-104">OLE 元件可以執行介面，而不會在介面中執行每個方法的所有語義，而是在適當的情況下傳回 E \_ >notimpl 或 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="b0f75-104">An OLE component can implement an interface without implementing all the semantics of every method in the interface, instead returning E\_NOTIMPL or S\_OK as appropriate.</span></span> <span data-ttu-id="b0f75-105">下表描述 ActiveX 控制項容器不需要執行的這些方法 (也就是控制項容器可以傳回 E \_ >notimpl) 。</span><span class="sxs-lookup"><span data-stu-id="b0f75-105">The following table describes those methods that an ActiveX control container is not required to implement (i.e. the control container can return E\_NOTIMPL).</span></span>

<span data-ttu-id="b0f75-106">下表說明選用的方法;請注意，方法必須仍然存在，但是可以直接傳回 E \_ >notimpl，而不是實作為實際的語法。</span><span class="sxs-lookup"><span data-stu-id="b0f75-106">The table below describes optional methods; note that the method must still exist, but can simply return E\_NOTIMPL instead of implementing real semantics.</span></span> <span data-ttu-id="b0f75-107">請注意，來自以下未列出之強制介面的任何方法都必須視為強制性，而且可能不會傳回 E \_ >notimpl。</span><span class="sxs-lookup"><span data-stu-id="b0f75-107">Note that any method from a mandatory interface that is not listed below must be considered mandatory and may not return E\_NOTIMPL.</span></span>

## <a name="ioleclientsite"></a><span data-ttu-id="b0f75-108">IOleClientSite</span><span class="sxs-lookup"><span data-stu-id="b0f75-108">IOleClientSite</span></span>



| <span data-ttu-id="b0f75-109">方法</span><span class="sxs-lookup"><span data-stu-id="b0f75-109">Method</span></span>                                                     | <span data-ttu-id="b0f75-110">註解</span><span class="sxs-lookup"><span data-stu-id="b0f75-110">Comments</span></span>                                                                                                 |
|------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b0f75-111">**SaveObject**</span><span class="sxs-lookup"><span data-stu-id="b0f75-111">**SaveObject**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-ioleclientsite-saveobject)<br/> | <span data-ttu-id="b0f75-112">成功支援持續性所需。</span><span class="sxs-lookup"><span data-stu-id="b0f75-112">Necessary for persistence to be successfully supported.</span></span><br/>                                       |
| [<span data-ttu-id="b0f75-113">**GetMoniker**</span><span class="sxs-lookup"><span data-stu-id="b0f75-113">**GetMoniker**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-ioleclientsite-getmoniker)<br/> | <span data-ttu-id="b0f75-114">只有在容器支援連結至自己的表單或檔內的控制項時才需要。</span><span class="sxs-lookup"><span data-stu-id="b0f75-114">Necessary only if the container supports linking to controls within its own form or document.</span></span><br/> |



 

## <a name="ioleinplacesite"></a><span data-ttu-id="b0f75-115">IOleInPlaceSite</span><span class="sxs-lookup"><span data-stu-id="b0f75-115">IOleInPlaceSite</span></span>



| <span data-ttu-id="b0f75-116">方法</span><span class="sxs-lookup"><span data-stu-id="b0f75-116">Method</span></span>                                                                     | <span data-ttu-id="b0f75-117">註解</span><span class="sxs-lookup"><span data-stu-id="b0f75-117">Comments</span></span>                                                 |
|----------------------------------------------------------------------------|----------------------------------------------------------|
| [<span data-ttu-id="b0f75-118">**CoNtextSensitiveHelp**</span><span class="sxs-lookup"><span data-stu-id="b0f75-118">**ContextSensitiveHelp**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-iolewindow-contextsensitivehelp)<br/> | <span data-ttu-id="b0f75-119">選擇性</span><span class="sxs-lookup"><span data-stu-id="b0f75-119">Optional</span></span><br/>                                      |
| [<span data-ttu-id="b0f75-120">**捲動**</span><span class="sxs-lookup"><span data-stu-id="b0f75-120">**Scroll**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplacesite-scroll)<br/>                        | <span data-ttu-id="b0f75-121">可能會傳回 \_ FALSE，而不採取任何動作。</span><span class="sxs-lookup"><span data-stu-id="b0f75-121">May return S\_FALSE with no action.</span></span><br/>           |
| [<span data-ttu-id="b0f75-122">**DiscardUndoState**</span><span class="sxs-lookup"><span data-stu-id="b0f75-122">**DiscardUndoState**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplacesite-discardundostate)<br/>    | <span data-ttu-id="b0f75-123">可以傳回 \_ [確定]，但不採取任何動作。</span><span class="sxs-lookup"><span data-stu-id="b0f75-123">Can return S\_OK with no action.</span></span><br/>              |
| [<span data-ttu-id="b0f75-124">**DeactivateAndUndo**</span><span class="sxs-lookup"><span data-stu-id="b0f75-124">**DeactivateAndUndo**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplacesite-deactivateandundo)<br/>  | <span data-ttu-id="b0f75-125">停用是強制性的;復原是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="b0f75-125">Deactivation is mandatory; Undo is optional.</span></span> <br/> |



 

## <a name="iolecontrolsite"></a><span data-ttu-id="b0f75-126">>iolecontrolsite</span><span class="sxs-lookup"><span data-stu-id="b0f75-126">IOleControlSite</span></span>



| <span data-ttu-id="b0f75-127">方法</span><span class="sxs-lookup"><span data-stu-id="b0f75-127">Method</span></span>                                                                          | <span data-ttu-id="b0f75-128">註解</span><span class="sxs-lookup"><span data-stu-id="b0f75-128">Comments</span></span>                                                                                                                                                            |
|---------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b0f75-129">**GetExtendedControl**</span><span class="sxs-lookup"><span data-stu-id="b0f75-129">**GetExtendedControl**</span></span>](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-getextendedcontrol)<br/>     | <span data-ttu-id="b0f75-130">支援擴充控制項的容器所需。</span><span class="sxs-lookup"><span data-stu-id="b0f75-130">Necessary for containers that support extended controls.</span></span><br/>                                                                                                 |
| [<span data-ttu-id="b0f75-131">**ShowPropertyFrame**</span><span class="sxs-lookup"><span data-stu-id="b0f75-131">**ShowPropertyFrame**</span></span>](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-showpropertyframe)<br/>       | <span data-ttu-id="b0f75-132">如果容器想要包含自己的屬性頁來處理擴充控制項屬性（除了控制項所提供的屬性），則為必要項。</span><span class="sxs-lookup"><span data-stu-id="b0f75-132">Necessary for containers that wish to include their own property pages to handle extended control properties in addition to those provided by a control.</span></span><br/> |
| [<span data-ttu-id="b0f75-133">**TranslateAccelerator**</span><span class="sxs-lookup"><span data-stu-id="b0f75-133">**TranslateAccelerator**</span></span>](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-translateaccelerator)<br/> | <span data-ttu-id="b0f75-134">可能會傳回 \_ FALSE，而不採取任何動作。</span><span class="sxs-lookup"><span data-stu-id="b0f75-134">May return S\_FALSE with no action.</span></span><br/>                                                                                                                      |
| [<span data-ttu-id="b0f75-135">**LockInPlaceActive**</span><span class="sxs-lookup"><span data-stu-id="b0f75-135">**LockInPlaceActive**</span></span>](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-lockinplaceactive)<br/>       | <span data-ttu-id="b0f75-136">選擇性</span><span class="sxs-lookup"><span data-stu-id="b0f75-136">Optional</span></span><br/>                                                                                                                                                 |



 

## <a name="idispatch-ambient-properties"></a><span data-ttu-id="b0f75-137">IDispatch (環境屬性) </span><span class="sxs-lookup"><span data-stu-id="b0f75-137">IDispatch (Ambient properties)</span></span>



| <span data-ttu-id="b0f75-138">方法</span><span class="sxs-lookup"><span data-stu-id="b0f75-138">Method</span></span>                      | <span data-ttu-id="b0f75-139">註解</span><span class="sxs-lookup"><span data-stu-id="b0f75-139">Comments</span></span>                                                                          |
|-----------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="b0f75-140">GetTypeInfoCount</span><span class="sxs-lookup"><span data-stu-id="b0f75-140">GetTypeInfoCount</span></span><br/> | <span data-ttu-id="b0f75-141">支援非標準環境屬性之容器的必要元件。</span><span class="sxs-lookup"><span data-stu-id="b0f75-141">Necessary for containers that support non-standard ambient properties.</span></span><br/> |
| <span data-ttu-id="b0f75-142">GetTypeInfo</span><span class="sxs-lookup"><span data-stu-id="b0f75-142">GetTypeInfo</span></span><br/>      | <span data-ttu-id="b0f75-143">支援非標準環境屬性之容器的必要元件。</span><span class="sxs-lookup"><span data-stu-id="b0f75-143">Necessary for containers that support non-standard ambient properties.</span></span><br/> |
| <span data-ttu-id="b0f75-144">GetIDsOfNames</span><span class="sxs-lookup"><span data-stu-id="b0f75-144">GetIDsOfNames</span></span><br/>    | <span data-ttu-id="b0f75-145">支援非標準環境屬性之容器的必要元件。</span><span class="sxs-lookup"><span data-stu-id="b0f75-145">Necessary for containers that support non-standard ambient properties.</span></span><br/> |



 

## <a name="idispatch-event-sink"></a><span data-ttu-id="b0f75-146">IDispatch (事件接收) </span><span class="sxs-lookup"><span data-stu-id="b0f75-146">IDispatch (Event sink)</span></span>



| <span data-ttu-id="b0f75-147">方法</span><span class="sxs-lookup"><span data-stu-id="b0f75-147">Method</span></span>                      | <span data-ttu-id="b0f75-148">註解</span><span class="sxs-lookup"><span data-stu-id="b0f75-148">Comments</span></span>                                                                               |
|-----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b0f75-149">GetTypeInfoCount</span><span class="sxs-lookup"><span data-stu-id="b0f75-149">GetTypeInfoCount</span></span><br/> | <span data-ttu-id="b0f75-150">控制項知道自己的型別資訊，因此不需要呼叫這個。</span><span class="sxs-lookup"><span data-stu-id="b0f75-150">The control knows its own type information, so it has no need to call this.</span></span><br/> |
| <span data-ttu-id="b0f75-151">GetTypeInfo</span><span class="sxs-lookup"><span data-stu-id="b0f75-151">GetTypeInfo</span></span><br/>      | <span data-ttu-id="b0f75-152">控制項知道自己的型別資訊，因此不需要呼叫這個。</span><span class="sxs-lookup"><span data-stu-id="b0f75-152">The control knows its own type information, so it has no need to call this.</span></span><br/> |
| <span data-ttu-id="b0f75-153">GetIDsOfNames</span><span class="sxs-lookup"><span data-stu-id="b0f75-153">GetIDsOfNames</span></span><br/>    | <span data-ttu-id="b0f75-154">控制項知道自己的型別資訊，因此不需要呼叫這個。</span><span class="sxs-lookup"><span data-stu-id="b0f75-154">The control knows its own type information, so it has no need to call this.</span></span><br/> |



 

## <a name="ioleinplaceframe"></a><span data-ttu-id="b0f75-155">IOleInPlaceFrame</span><span class="sxs-lookup"><span data-stu-id="b0f75-155">IOleInPlaceFrame</span></span>



| <span data-ttu-id="b0f75-156">方法</span><span class="sxs-lookup"><span data-stu-id="b0f75-156">Method</span></span>                                                                           | <span data-ttu-id="b0f75-157">註解</span><span class="sxs-lookup"><span data-stu-id="b0f75-157">Comments</span></span>                                                                |
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [<span data-ttu-id="b0f75-158">**CoNtextSensitiveHelp**</span><span class="sxs-lookup"><span data-stu-id="b0f75-158">**ContextSensitiveHelp**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-iolewindow-contextsensitivehelp)<br/>       |                                                                         |
| [<span data-ttu-id="b0f75-159">**GetBorder**</span><span class="sxs-lookup"><span data-stu-id="b0f75-159">**GetBorder**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceuiwindow-getborder)<br/>                    | <span data-ttu-id="b0f75-160">具有工具列 UI (的容器的必要選項) </span><span class="sxs-lookup"><span data-stu-id="b0f75-160">Necessary for containers with toolbar UI (which is optional)</span></span><br/> |
| [<span data-ttu-id="b0f75-161">**RequestBorderSpace**</span><span class="sxs-lookup"><span data-stu-id="b0f75-161">**RequestBorderSpace**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceuiwindow-requestborderspace)<br/>  | <span data-ttu-id="b0f75-162">具有工具列 UI (的容器的必要選項) </span><span class="sxs-lookup"><span data-stu-id="b0f75-162">Necessary for containers with toolbar UI (which is optional)</span></span><br/> |
| [<span data-ttu-id="b0f75-163">**SetBorderSpace**</span><span class="sxs-lookup"><span data-stu-id="b0f75-163">**SetBorderSpace**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceuiwindow-setborderspace)<br/>          | <span data-ttu-id="b0f75-164">具有工具列 UI (的容器的必要選項) </span><span class="sxs-lookup"><span data-stu-id="b0f75-164">Necessary for containers with toolbar UI (which is optional)</span></span><br/> |
| [<span data-ttu-id="b0f75-165">**InsertMenus**</span><span class="sxs-lookup"><span data-stu-id="b0f75-165">**InsertMenus**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceframe-insertmenus)<br/>                   | <span data-ttu-id="b0f75-166">具有功能表 UI (的容器的必要選項) </span><span class="sxs-lookup"><span data-stu-id="b0f75-166">Necessary for containers with menu UI (which is optional)</span></span><br/>    |
| [<span data-ttu-id="b0f75-167">**SetMenu**</span><span class="sxs-lookup"><span data-stu-id="b0f75-167">**SetMenu**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceframe-setmenu)<br/>                           | <span data-ttu-id="b0f75-168">具有功能表 UI (的容器的必要選項) </span><span class="sxs-lookup"><span data-stu-id="b0f75-168">Necessary for containers with menu UI (which is optional)</span></span><br/>    |
| [<span data-ttu-id="b0f75-169">**RemoveMenus**</span><span class="sxs-lookup"><span data-stu-id="b0f75-169">**RemoveMenus**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceframe-removemenus)<br/>                   | <span data-ttu-id="b0f75-170">具有功能表 UI (的容器的必要選項) </span><span class="sxs-lookup"><span data-stu-id="b0f75-170">Necessary for containers with menu UI (which is optional)</span></span><br/>    |
| [<span data-ttu-id="b0f75-171">**SetStatusText**</span><span class="sxs-lookup"><span data-stu-id="b0f75-171">**SetStatusText**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceframe-setstatustext)<br/>               | <span data-ttu-id="b0f75-172">只有具有狀態行的容器才需要</span><span class="sxs-lookup"><span data-stu-id="b0f75-172">Necessary only for containers that have a status line</span></span><br/>        |
| [<span data-ttu-id="b0f75-173">**EnableModeless**</span><span class="sxs-lookup"><span data-stu-id="b0f75-173">**EnableModeless**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceframe-enablemodeless)<br/>             | <span data-ttu-id="b0f75-174">選擇性</span><span class="sxs-lookup"><span data-stu-id="b0f75-174">Optional</span></span><br/>                                                     |
| [<span data-ttu-id="b0f75-175">**TranslateAccelerator**</span><span class="sxs-lookup"><span data-stu-id="b0f75-175">**TranslateAccelerator**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceframe-translateaccelerator)<br/> | <span data-ttu-id="b0f75-176">選擇性</span><span class="sxs-lookup"><span data-stu-id="b0f75-176">Optional</span></span><br/>                                                     |



 

## <a name="iolecontainer"></a><span data-ttu-id="b0f75-177">IOleContainer</span><span class="sxs-lookup"><span data-stu-id="b0f75-177">IOleContainer</span></span>



| <span data-ttu-id="b0f75-178">方法</span><span class="sxs-lookup"><span data-stu-id="b0f75-178">Method</span></span>                                                                    | <span data-ttu-id="b0f75-179">註解</span><span class="sxs-lookup"><span data-stu-id="b0f75-179">Comments</span></span>                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b0f75-180">**ParseDisplayName**</span><span class="sxs-lookup"><span data-stu-id="b0f75-180">**ParseDisplayName**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-iparsedisplayname-parsedisplayname)<br/> | <span data-ttu-id="b0f75-181">只有在支援連結至控制項或容器中的其他內嵌時，才支援這項功能，因為這是針對標記系結的必要項。</span><span class="sxs-lookup"><span data-stu-id="b0f75-181">Only if linking to controls or other embeddings in the container is supported, as this is necessary for moniker binding.</span></span><br/>                                                                                                                  |
| [<span data-ttu-id="b0f75-182">**LockContainer**</span><span class="sxs-lookup"><span data-stu-id="b0f75-182">**LockContainer**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-iolecontainer-lockcontainer)<br/>           | <span data-ttu-id="b0f75-183">適用于 ParseDisplayName</span><span class="sxs-lookup"><span data-stu-id="b0f75-183">As for ParseDisplayName</span></span><br/>                                                                                                                                                                                                                   |
| [<span data-ttu-id="b0f75-184">**EnumObjects**</span><span class="sxs-lookup"><span data-stu-id="b0f75-184">**EnumObjects**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-iolecontainer-enumobjects)<br/>               | <span data-ttu-id="b0f75-185">透過 [**IEnumUnknown**](/windows/win32/api/objidlbase/nn-objidlbase-ienumunknown)的列舉值傳回所有 ActiveX 控制項，但不一定都 (的所有物件，因為不保證所有物件都是 ActiveX 控制項;有些可能是一般的 Windows 控制項) 。</span><span class="sxs-lookup"><span data-stu-id="b0f75-185">Returns all ActiveX controls through an enumerator with [**IEnumUnknown**](/windows/win32/api/objidlbase/nn-objidlbase-ienumunknown), but not necessarily all objects (because there's no guarantee that all objects are ActiveX controls; some may be regular Windows controls).</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="b0f75-186">相關主題</span><span class="sxs-lookup"><span data-stu-id="b0f75-186">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b0f75-187">容器</span><span class="sxs-lookup"><span data-stu-id="b0f75-187">Containers</span></span>](containers.md)
</dt> </dl>

 

