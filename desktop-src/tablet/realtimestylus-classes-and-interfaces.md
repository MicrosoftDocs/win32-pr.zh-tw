---
description: 本章節包含有關即時手寫筆中所使用之介面和類別的資訊。
ms.assetid: fc0900b4-f08b-4a93-bbc0-d3db067d7917
title: RealTimeStylus 類別和介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34769b2c268bcdfe2becf9e759344d972092fe28
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850016"
---
# <a name="realtimestylus-classes-and-interfaces"></a><span data-ttu-id="908c9-103">RealTimeStylus 類別和介面</span><span class="sxs-lookup"><span data-stu-id="908c9-103">RealTimeStylus Classes and Interfaces</span></span>

<span data-ttu-id="908c9-104">本章節包含有關即時手寫筆中所使用之介面和類別的資訊。</span><span class="sxs-lookup"><span data-stu-id="908c9-104">This section contains information about the interfaces and classes used in the real time stylus.</span></span>

> [!Note]  
> <span data-ttu-id="908c9-105">即時手寫筆類別和介面不符合自動化規範。</span><span class="sxs-lookup"><span data-stu-id="908c9-105">The real time stylus classes and interfaces are not Automation compliant.</span></span>

 

## <a name="in-this-section"></a><span data-ttu-id="908c9-106">本節內容</span><span class="sxs-lookup"><span data-stu-id="908c9-106">In This Section</span></span>



| <span data-ttu-id="908c9-107">類別</span><span class="sxs-lookup"><span data-stu-id="908c9-107">Class</span></span>                                                      | <span data-ttu-id="908c9-108">描述</span><span class="sxs-lookup"><span data-stu-id="908c9-108">Description</span></span>                                                                                     |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="908c9-109">**RealTimeStylus 類別**</span><span class="sxs-lookup"><span data-stu-id="908c9-109">**RealTimeStylus Class**</span></span>](realtimestylus-class.md)       | <span data-ttu-id="908c9-110">實行 [**IRealTimeStylus**](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylus) 介面。</span><span class="sxs-lookup"><span data-stu-id="908c9-110">Implements the [**IRealTimeStylus**](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylus) interface.</span></span><br/>                 |
| <span data-ttu-id="908c9-111">[**DynamicRenderer 類別**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="908c9-111">[**DynamicRenderer Class**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85))</span></span>     | <span data-ttu-id="908c9-112">實行 [**IDynamicRenderer 介面**](/windows/desktop/api/RTSCom/nn-rtscom-idynamicrenderer) 介面。</span><span class="sxs-lookup"><span data-stu-id="908c9-112">Implements the [**IDynamicRenderer Interface**](/windows/desktop/api/RTSCom/nn-rtscom-idynamicrenderer) interface.</span></span><br/>     |
| [<span data-ttu-id="908c9-113">**GestureRecognizer 類別**</span><span class="sxs-lookup"><span data-stu-id="908c9-113">**GestureRecognizer Class**</span></span>](gesturerecognizer-class.md) | <span data-ttu-id="908c9-114">實行 [**IGestureRecognizer 介面**](/windows/desktop/api/RTSCom/nn-rtscom-igesturerecognizer) 介面。</span><span class="sxs-lookup"><span data-stu-id="908c9-114">Implements the [**IGestureRecognizer Interface**](/windows/desktop/api/RTSCom/nn-rtscom-igesturerecognizer) interface.</span></span><br/> |
| [<span data-ttu-id="908c9-115">**StrokeBuilder 類別**</span><span class="sxs-lookup"><span data-stu-id="908c9-115">**StrokeBuilder Class**</span></span>](strokebuilder-class.md)         | <span data-ttu-id="908c9-116">實行 [**IStrokeBuilder 介面**](/windows/desktop/api/RTSCom/nn-rtscom-istrokebuilder) 介面。</span><span class="sxs-lookup"><span data-stu-id="908c9-116">Implements the [**IStrokeBuilder Interface**](/windows/desktop/api/RTSCom/nn-rtscom-istrokebuilder) interface.</span></span><br/>         |



 

## <a name="interfaces"></a><span data-ttu-id="908c9-117">介面</span><span class="sxs-lookup"><span data-stu-id="908c9-117">Interfaces</span></span>



| <span data-ttu-id="908c9-118">介面</span><span class="sxs-lookup"><span data-stu-id="908c9-118">Interface</span></span>                                                                          | <span data-ttu-id="908c9-119">描述</span><span class="sxs-lookup"><span data-stu-id="908c9-119">Description</span></span>                                                                                                                                                                                 |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="908c9-120">**IDynamicRenderer 介面**</span><span class="sxs-lookup"><span data-stu-id="908c9-120">**IDynamicRenderer Interface**</span></span>](/windows/desktop/api/RTSCom/nn-rtscom-idynamicrenderer)                             | <span data-ttu-id="908c9-121">公開方法，可讓您在資料由 [**RealTimeStylus 類別**](realtimestylus-class.md) 物件處理時，即時控制手寫筆資料的顯示。</span><span class="sxs-lookup"><span data-stu-id="908c9-121">Exposes methods enabling you to control the display of stylus data in real time as the data is being handled by the [**RealTimeStylus Class**](realtimestylus-class.md) object.</span></span><br/> |
| [<span data-ttu-id="908c9-122">**IGestureRecognizer 介面**</span><span class="sxs-lookup"><span data-stu-id="908c9-122">**IGestureRecognizer Interface**</span></span>](/windows/desktop/api/RTSCom/nn-rtscom-igesturerecognizer)                         | <span data-ttu-id="908c9-123">公開方法，讓您能夠辨識手寫筆手勢，並讓您將資料新增至輸入佇列，以回應事件。</span><span class="sxs-lookup"><span data-stu-id="908c9-123">Exposes methods enabling you to react to events by recognizing stylus gestures and enabling you to add data to the input queue.</span></span><br/>                                                  |
| [<span data-ttu-id="908c9-124">**IRealTimeStylus**</span><span class="sxs-lookup"><span data-stu-id="908c9-124">**IRealTimeStylus**</span></span>](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylus)                                         | <span data-ttu-id="908c9-125">即時處理來自數位板的手寫筆封包資料。</span><span class="sxs-lookup"><span data-stu-id="908c9-125">Handles the stylus packet data from a digitizer in real time.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="908c9-126">**IRealTimeStylus2**</span><span class="sxs-lookup"><span data-stu-id="908c9-126">**IRealTimeStylus2**</span></span>](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylus2)                                       | <span data-ttu-id="908c9-127">擴充 IRealTimeStylus 介面。</span><span class="sxs-lookup"><span data-stu-id="908c9-127">Extends the IRealTimeStylus interface.</span></span><br/>                                                                                                                                           |
| [<span data-ttu-id="908c9-128">**IRealTimeStylus3**</span><span class="sxs-lookup"><span data-stu-id="908c9-128">**IRealTimeStylus3**</span></span>](/windows/desktop/api/rtscom/nn-rtscom-irealtimestylus3)                                       | <span data-ttu-id="908c9-129">擴充 IRealTimeStylus 介面。</span><span class="sxs-lookup"><span data-stu-id="908c9-129">Extends the IRealTimeStylus interface.</span></span><br/>                                                                                                                                           |
| [<span data-ttu-id="908c9-130">**IRealTimeStylusSynchronization 介面**</span><span class="sxs-lookup"><span data-stu-id="908c9-130">**IRealTimeStylusSynchronization Interface**</span></span>](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylussynchronization) | <span data-ttu-id="908c9-131">同步處理對 [**RealTimeStylus 類別**](realtimestylus-class.md) 物件的存取。</span><span class="sxs-lookup"><span data-stu-id="908c9-131">Synchronizes access to the [**RealTimeStylus Class**](realtimestylus-class.md) object.</span></span><br/>                                                                                          |
| [<span data-ttu-id="908c9-132">**IStrokeBuilder 介面**</span><span class="sxs-lookup"><span data-stu-id="908c9-132">**IStrokeBuilder Interface**</span></span>](/windows/desktop/api/RTSCom/nn-rtscom-istrokebuilder)                                 | <span data-ttu-id="908c9-133">公開可讓您以程式設計方式建立筆劃的方法。</span><span class="sxs-lookup"><span data-stu-id="908c9-133">Exposes methods that enable you to programmatically create strokes.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="908c9-134">**IStylusPlugin 介面**</span><span class="sxs-lookup"><span data-stu-id="908c9-134">**IStylusPlugin Interface**</span></span>](/windows/desktop/api/RTSCom/nn-rtscom-istylusplugin)                                   | <span data-ttu-id="908c9-135">公開方法，讓您可以接收事件的通知，並根據這些事件執行自訂處理。</span><span class="sxs-lookup"><span data-stu-id="908c9-135">Exposes methods enabling you to receive notifications of events and to perform custom processing based on those events.</span></span><br/>                                                          |
| [<span data-ttu-id="908c9-136">**IStylusAsyncPlugin**</span><span class="sxs-lookup"><span data-stu-id="908c9-136">**IStylusAsyncPlugin**</span></span>](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin)                                   | <span data-ttu-id="908c9-137">表示可以加入至 [**RealTimeStylus 類別**](realtimestylus-class.md) 非同步外掛程式集合的非同步外掛程式。</span><span class="sxs-lookup"><span data-stu-id="908c9-137">Represents an asynchronous plug-in that can be added to the [**RealTimeStylus Class**](realtimestylus-class.md) asynchronous plug-in collection.</span></span><br/>                                |
| [<span data-ttu-id="908c9-138">**IStylusSyncPlugin**</span><span class="sxs-lookup"><span data-stu-id="908c9-138">**IStylusSyncPlugin**</span></span>](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin)                                     | <span data-ttu-id="908c9-139">表示可以加入至 [**RealTimeStylus 類別**](realtimestylus-class.md) 同步外掛程式集合的同步外掛程式。</span><span class="sxs-lookup"><span data-stu-id="908c9-139">Represents a synchronous plug-in that can be added to the [**RealTimeStylus Class**](realtimestylus-class.md) synchronous plug-in collection.</span></span><br/>                                   |



 

## <a name="return-values"></a><span data-ttu-id="908c9-140">傳回值</span><span class="sxs-lookup"><span data-stu-id="908c9-140">Return Values</span></span>

<span data-ttu-id="908c9-141">COM 程式庫中的方法會傳回 **HRESULT** 的值。</span><span class="sxs-lookup"><span data-stu-id="908c9-141">Methods in the COM Library return values of **HRESULT**.</span></span> <span data-ttu-id="908c9-142">除非另有說明，否則 **HRESULT** 值的意義如下表所述。</span><span class="sxs-lookup"><span data-stu-id="908c9-142">Unless otherwise noted, the meanings of the **HRESULT** values are described in the following table.</span></span>



| <span data-ttu-id="908c9-143">HRESULT 值</span><span class="sxs-lookup"><span data-stu-id="908c9-143">HRESULT value</span></span>                                   | <span data-ttu-id="908c9-144">Description</span><span class="sxs-lookup"><span data-stu-id="908c9-144">Description</span></span>                                                                              |
|-------------------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="908c9-145">S \_ 確定</span><span class="sxs-lookup"><span data-stu-id="908c9-145">S\_OK</span></span><br/>                                | <span data-ttu-id="908c9-146">成功。</span><span class="sxs-lookup"><span data-stu-id="908c9-146">Success.</span></span><br/>                                                                      |
| <span data-ttu-id="908c9-147">E \_ 指標</span><span class="sxs-lookup"><span data-stu-id="908c9-147">E\_POINTER</span></span><br/>                           | <span data-ttu-id="908c9-148">輸入或輸出參數的至少一個指標 () 無效。</span><span class="sxs-lookup"><span data-stu-id="908c9-148">At least one pointer (for either an input or an output parameter) is invalid.</span></span><br/> |
| <span data-ttu-id="908c9-149">E \_ INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="908c9-149">E\_INVALIDARG</span></span><br/>                        | <span data-ttu-id="908c9-150">成員嘗試傳入不正確引數。</span><span class="sxs-lookup"><span data-stu-id="908c9-150">Member attempted to pass in an invalid argument.</span></span><br/>                              |
| <span data-ttu-id="908c9-151">E \_ 筆墨 \_ 例外狀況</span><span class="sxs-lookup"><span data-stu-id="908c9-151">E\_INK\_EXCEPTION</span></span><br/>                    | <span data-ttu-id="908c9-152">發生例外狀況。</span><span class="sxs-lookup"><span data-stu-id="908c9-152">Exception occurred.</span></span><br/>                                                           |
| <span data-ttu-id="908c9-153">E \_ OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="908c9-153">E\_OUTOFMEMORY</span></span><br/>                       | <span data-ttu-id="908c9-154">系統無法配置記憶體來完成操作。</span><span class="sxs-lookup"><span data-stu-id="908c9-154">System cannot allocate memory to complete the operation.</span></span><br/>                      |
| <span data-ttu-id="908c9-155">E \_ 失敗</span><span class="sxs-lookup"><span data-stu-id="908c9-155">E\_FAIL</span></span><br/>                              | <span data-ttu-id="908c9-156">發生未指定的失敗。</span><span class="sxs-lookup"><span data-stu-id="908c9-156">Unspecified failure occurred.</span></span><br/>                                                 |
| <span data-ttu-id="908c9-157">E \_ INVALIDOPERATION</span><span class="sxs-lookup"><span data-stu-id="908c9-157">E\_INVALIDOPERATION</span></span><br/>                  | <span data-ttu-id="908c9-158">成員嘗試使用不正確作業。</span><span class="sxs-lookup"><span data-stu-id="908c9-158">Member attempted to use an invalid operation.</span></span><br/>                                 |
| <span data-ttu-id="908c9-159">TPC \_ E \_ 無效 \_ 模式</span><span class="sxs-lookup"><span data-stu-id="908c9-159">TPC\_E\_INVALID\_MODE</span></span><br/>                | <span data-ttu-id="908c9-160">成員嘗試使用不正確模式。</span><span class="sxs-lookup"><span data-stu-id="908c9-160">Member attempted to use an invalid mode.</span></span><br/>                                      |
| <span data-ttu-id="908c9-161">TPC \_ E \_ 不正確設定 \_</span><span class="sxs-lookup"><span data-stu-id="908c9-161">TPC\_E\_INVALID\_CONFIGURATION</span></span><br/>       | <span data-ttu-id="908c9-162">成員嘗試使用不正確設定。</span><span class="sxs-lookup"><span data-stu-id="908c9-162">Member attempted to use an invalid configuration.</span></span><br/>                             |
| <span data-ttu-id="908c9-163">TPC \_ E \_ 不正確封 \_ 包 \_ 描述</span><span class="sxs-lookup"><span data-stu-id="908c9-163">TPC\_E\_INVALID\_PACKET\_DESCRIPTION</span></span><br/> | <span data-ttu-id="908c9-164">成員嘗試使用不正確封包描述。</span><span class="sxs-lookup"><span data-stu-id="908c9-164">Member attempted to use an invalid packet description.</span></span><br/>                        |



 

## <a name="related-topics"></a><span data-ttu-id="908c9-165">相關主題</span><span class="sxs-lookup"><span data-stu-id="908c9-165">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="908c9-166">RealTimeStylus 參考</span><span class="sxs-lookup"><span data-stu-id="908c9-166">RealTimeStylus Reference</span></span>](realtimestylus-reference.md)
</dt> </dl>

 

 
