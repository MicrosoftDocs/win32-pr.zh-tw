---
description: RealTimeStylus 類別的串聯模型總覽。
ms.assetid: f4c377a7-979d-4a06-a8de-31b8e67d74f8
title: 串聯的 RealTimeStylus 模型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd2f61ea3cd44753d1d91fb2662226a716ee5590
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104553530"
---
# <a name="the-cascaded-realtimestylus-model"></a><span data-ttu-id="323f4-103">串聯的 RealTimeStylus 模型</span><span class="sxs-lookup"><span data-stu-id="323f4-103">The Cascaded RealTimeStylus Model</span></span>

<span data-ttu-id="323f4-104">串聯的 [**realtimestylus**](realtimestylus-class.md) 模型可讓您使用兩個 **RealTimeStylus** 物件，每個物件都在不同的執行緒上執行。</span><span class="sxs-lookup"><span data-stu-id="323f4-104">The cascaded [**RealTimeStylus**](realtimestylus-class.md) model enables you to use two **RealTimeStylus** objects, each running on a different thread.</span></span> <span data-ttu-id="323f4-105">使用此模型，您可以將次要 **realtimestylus** 物件附加至主要的 **realtimestylus** 物件。</span><span class="sxs-lookup"><span data-stu-id="323f4-105">With this model, you attach a secondary **RealTimeStylus** object to a primary **RealTimeStylus** object.</span></span> <span data-ttu-id="323f4-106">次要 **realtimestylus** 物件會附加為主要 **realtimestylus** 物件之非同步外掛程式集合中的唯一非同步外掛程式。</span><span class="sxs-lookup"><span data-stu-id="323f4-106">The secondary **RealTimeStylus** object is attached as the only asynchronous plug-in in the primary **RealTimeStylus** object's asynchronous plug-in collection.</span></span>

<span data-ttu-id="323f4-107">在下列案例中，串聯的 [**RealTimeStylus**](realtimestylus-class.md) 模型可能會很有用。</span><span class="sxs-lookup"><span data-stu-id="323f4-107">The cascaded [**RealTimeStylus**](realtimestylus-class.md) model may be useful in the following scenarios.</span></span>

-   <span data-ttu-id="323f4-108">您可以新增一些可能需要計算的工作，但仍需要對 tablet 畫筆的資料流程進行即時存取，例如 multistroke 手勢辨識，以存取次要 [**RealTimeStylus**](realtimestylus-class.md) 物件的同步外掛程式集合。</span><span class="sxs-lookup"><span data-stu-id="323f4-108">You can add certain tasks that may be computationally demanding yet still require real-time access to the tablet pen's data stream, such as multistroke gesture recognition, to the secondary [**RealTimeStylus**](realtimestylus-class.md) object's synchronous plug-in collection.</span></span>
-   <span data-ttu-id="323f4-109">您可以將同步外掛程式的計算負載分散在兩個執行緒上，減少某些 Tablet Pc 上筆跡集合的延遲。</span><span class="sxs-lookup"><span data-stu-id="323f4-109">You can spread the computational load of your synchronous plug-ins over two threads, reducing delays in ink collection on some Tablet PCs.</span></span>

<span data-ttu-id="323f4-110">下圖說明 tablet 畫筆資料透過兩個串聯的 [**RealTimeStylus**](realtimestylus-class.md) 物件和其外掛程式集合的流程。</span><span class="sxs-lookup"><span data-stu-id="323f4-110">The following diagram illustrates the flow of tablet pen data through two cascaded [**RealTimeStylus**](realtimestylus-class.md) objects and their plug-in collections.</span></span>

![顯示串聯的 realtimestylus 資料流程的圖例](images/72ca1999-e078-49f8-a336-3b4d0157a472.gif)

<span data-ttu-id="323f4-112">在此圖中，「A」圓圈表示主要和次要 [**realtimestylus**](realtimestylus-class.md) 物件已經處理過的 tablet 畫筆資料，並且已置於次要 **RealTimeStylus** 物件的輸出佇列。</span><span class="sxs-lookup"><span data-stu-id="323f4-112">In this diagram the circle lettered "A" represents tablet pen data that has already been processed by both the primary and secondary [**RealTimeStylus**](realtimestylus-class.md) objects and has been placed on the secondary **RealTimeStylus** object's output queue.</span></span> <span data-ttu-id="323f4-113">以字母 "B" 表示的 tablet 畫筆資料，已由主要 **realtimestylus** 物件處理並新增至主要 **realtimestylus** 物件的輸出佇列，但尚未傳送至次要 **realtimestylus** 物件。</span><span class="sxs-lookup"><span data-stu-id="323f4-113">The circle lettered "B" represents tablet pen data that has already been processed by the primary **RealTimeStylus** object and added to the primary **RealTimeStylus** object's output queue and has not yet been sent to the secondary **RealTimeStylus** object.</span></span> <span data-ttu-id="323f4-114">以字母 "C" 表示主要 **RealTimeStylus** 物件目前正在處理的 tablet 畫筆資料。</span><span class="sxs-lookup"><span data-stu-id="323f4-114">The circle lettered "C" represents the tablet pen data that the primary **RealTimeStylus** object is currently processing.</span></span> <span data-ttu-id="323f4-115">它會傳送至同步的外掛程式集合，並放在輸出佇列中。</span><span class="sxs-lookup"><span data-stu-id="323f4-115">It is sent to the synchronous plug-in collection and placed on the output queue.</span></span> <span data-ttu-id="323f4-116">空的圓形代表在輸出佇列中加入未來 tablet 畫筆資料的位置。</span><span class="sxs-lookup"><span data-stu-id="323f4-116">The empty circle represents the position in the output queue where future tablet pen data is added.</span></span>

## <a name="constraints"></a><span data-ttu-id="323f4-117">條件約束</span><span class="sxs-lookup"><span data-stu-id="323f4-117">Constraints</span></span>

<span data-ttu-id="323f4-118">如果您使用預設的 [**realtimestylus**](realtimestylus-class.md)函式，您可以建立只能接受來自另一個 **realtimestylus** 物件之輸入的 **realtimestylus** 物件。</span><span class="sxs-lookup"><span data-stu-id="323f4-118">If you use the default [**RealTimeStylus**](realtimestylus-class.md) constructor, you create a **RealTimeStylus** object that can only accept input from another **RealTimeStylus** object.</span></span>

<span data-ttu-id="323f4-119">下列清單描述與使用串聯式 [**RealTimeStylus**](realtimestylus-class.md) 模型相關聯的條件約束。</span><span class="sxs-lookup"><span data-stu-id="323f4-119">The following list describes the constraints associated with using the cascaded [**RealTimeStylus**](realtimestylus-class.md) model.</span></span>

-   <span data-ttu-id="323f4-120">只有兩個 [**realtimestylus**](realtimestylus-class.md) 物件可以使用，主要的 **realtimestylus** 物件和次要 **realtimestylus** 物件。</span><span class="sxs-lookup"><span data-stu-id="323f4-120">Only two [**RealTimeStylus**](realtimestylus-class.md) objects may be used, a primary **RealTimeStylus** object and a secondary **RealTimeStylus** object.</span></span>
-   <span data-ttu-id="323f4-121">主要 [**RealTimeStylus**](realtimestylus-class.md) 物件必須使用使用 **attachedControl** 或 *handle* 參數的函式來建立。</span><span class="sxs-lookup"><span data-stu-id="323f4-121">The primary [**RealTimeStylus**](realtimestylus-class.md) object must be created with a constructor that uses the **attachedControl** or *handle* parameter.</span></span> <span data-ttu-id="323f4-122">次要 **RealTimeStylus** 物件必須使用無引數的函式來建立。</span><span class="sxs-lookup"><span data-stu-id="323f4-122">The secondary **RealTimeStylus** object must be created with the no-argument constructor.</span></span>
-   <span data-ttu-id="323f4-123">次要 [**realtimestylus**](realtimestylus-class.md) 物件必須是主要 **realtimestylus** 物件之非同步外掛程式集合中的唯一非同步外掛程式。</span><span class="sxs-lookup"><span data-stu-id="323f4-123">The secondary [**RealTimeStylus**](realtimestylus-class.md) object must be the only asynchronous plug-in in the primary **RealTimeStylus** object's asynchronous plug-in collection.</span></span>
-   <span data-ttu-id="323f4-124">次要 [**realtimestylus**](realtimestylus-class.md) 物件一次只能附加至一個主要的 **realtimestylus** 物件。</span><span class="sxs-lookup"><span data-stu-id="323f4-124">A secondary [**RealTimeStylus**](realtimestylus-class.md) object can only be attached to one primary **RealTimeStylus** object at a time.</span></span> <span data-ttu-id="323f4-125">如果新增至第二個主要 **realtimestylus** 物件，則 [Add](/previous-versions/ms824814(v=msdn.10)) 方法會擲回例外狀況，而次要 **realtimestylus** 物件不會附加至第二個主要 **realtimestylus** 物件。</span><span class="sxs-lookup"><span data-stu-id="323f4-125">If it is added to a second primary **RealTimeStylus** object, the [Add](/previous-versions/ms824814(v=msdn.10)) method throws an exception, and the secondary **RealTimeStylus** object is not attached to the second primary **RealTimeStylus** object.</span></span>
-   <span data-ttu-id="323f4-126">修改部分次要 [**RealTimeStylus**](realtimestylus-class.md) 物件成員的行為。</span><span class="sxs-lookup"><span data-stu-id="323f4-126">The behavior of some of the secondary [**RealTimeStylus**](realtimestylus-class.md) object's members is modified.</span></span> <span data-ttu-id="323f4-127">下表描述這些成員的修改後行為。</span><span class="sxs-lookup"><span data-stu-id="323f4-127">The following table describes the modified behavior of these members.</span></span>

    

    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="323f4-128">成員</span><span class="sxs-lookup"><span data-stu-id="323f4-128">Member</span></span></th>
    <th><span data-ttu-id="323f4-129">行為</span><span class="sxs-lookup"><span data-stu-id="323f4-129">Behavior</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="323f4-130"><a href="/previous-versions/ms825905(v=msdn.10)">GetDesiredPacketDescription</a></span><span class="sxs-lookup"><span data-stu-id="323f4-130"><a href="/previous-versions/ms825905(v=msdn.10)">GetDesiredPacketDescription</a></span></span></td>
    <td><span data-ttu-id="323f4-131">這個方法會從主要 <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> 物件傳回信息。</span><span class="sxs-lookup"><span data-stu-id="323f4-131">This method returns the information from the primary <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> object.</span></span><br/> <span data-ttu-id="323f4-132">如果次要 <a href="realtimestylus-class.md"><strong>realtimestylus</strong></a> 未附加至主要 <strong>realtimestylus</strong> 物件，這個方法會傳回預設值。</span><span class="sxs-lookup"><span data-stu-id="323f4-132">If the secondary <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> is not attached to a primary <strong>RealTimeStylus</strong> object, this method returns the default value.</span></span><br/></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="323f4-133"><a href="/previous-versions/ms826041(v=msdn.10)">SetDesiredPacketDescription</a></span><span class="sxs-lookup"><span data-stu-id="323f4-133"><a href="/previous-versions/ms826041(v=msdn.10)">SetDesiredPacketDescription</a></span></span></td>
    <td><span data-ttu-id="323f4-134">這個方法會引發 <a href="/dotnet/api/system.invalidoperationexception">InvalidOperationException</a> 例外狀況。</span><span class="sxs-lookup"><span data-stu-id="323f4-134">This method raises an <a href="/dotnet/api/system.invalidoperationexception">InvalidOperationException</a> exception.</span></span><br/></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="323f4-135"><a href="/previous-versions/ms825913(v=msdn.10)">GetStyluses</a></span><span class="sxs-lookup"><span data-stu-id="323f4-135"><a href="/previous-versions/ms825913(v=msdn.10)">GetStyluses</a></span></span></td>
    <td><span data-ttu-id="323f4-136">這個方法會從主要 <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> 物件傳回信息。</span><span class="sxs-lookup"><span data-stu-id="323f4-136">This method returns the information from the primary <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> object.</span></span><br/> <span data-ttu-id="323f4-137">如果次要 <a href="realtimestylus-class.md"><strong>realtimestylus</strong></a> 未附加至主要 <strong>realtimestylus</strong> 物件，這個方法會傳回空陣列。</span><span class="sxs-lookup"><span data-stu-id="323f4-137">If the secondary <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> is not attached to a primary <strong>RealTimeStylus</strong> object, this method returns an empty array.</span></span><br/></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="323f4-138"><a href="/previous-versions/ms824832(v=msdn.10)">Enabled</a></span><span class="sxs-lookup"><span data-stu-id="323f4-138"><a href="/previous-versions/ms824832(v=msdn.10)">Enabled</a></span></span></td>
    <td><span data-ttu-id="323f4-139">取得此屬性會從主要 <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> 物件傳回信息。</span><span class="sxs-lookup"><span data-stu-id="323f4-139">Getting this property returns the information from the primary <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> object.</span></span><br/> <span data-ttu-id="323f4-140">如果次要 <a href="realtimestylus-class.md"><strong>realtimestylus</strong></a> 未附加至主要 <strong>realtimestylus</strong> 物件，則取得此屬性會傳回預設值。</span><span class="sxs-lookup"><span data-stu-id="323f4-140">If the secondary <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> is not attached to a primary <strong>RealTimeStylus</strong> object, getting this property returns the default value.</span></span><br/>
    <blockquote>
    [!Note]<br />
<span data-ttu-id="323f4-141">設定這個屬性會引發 <a href="/dotnet/api/system.invalidoperationexception">InvalidOperationException</a> 例外狀況。</span><span class="sxs-lookup"><span data-stu-id="323f4-141">Setting this property raises an <a href="/dotnet/api/system.invalidoperationexception">InvalidOperationException</a> exception.</span></span>
    </blockquote>
    <br/></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="323f4-142"><a href="/previous-versions/ms824834(v=msdn.10)">WindowInputRectangle</a></span><span class="sxs-lookup"><span data-stu-id="323f4-142"><a href="/previous-versions/ms824834(v=msdn.10)">WindowInputRectangle</a></span></span></td>
    <td><span data-ttu-id="323f4-143">取得此屬性會從主要 <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> 物件傳回信息。</span><span class="sxs-lookup"><span data-stu-id="323f4-143">Getting this property returns the information from the primary <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> object.</span></span><br/> <span data-ttu-id="323f4-144">如果次要 <a href="realtimestylus-class.md"><strong>realtimestylus</strong></a> 未附加至主要 <strong>realtimestylus</strong> 物件，則取得此屬性會傳回預設值。</span><span class="sxs-lookup"><span data-stu-id="323f4-144">If the secondary <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> is not attached to a primary <strong>RealTimeStylus</strong> object, getting this property returns the default value.</span></span><br/>
    <blockquote>
    [!Note]<br />
<span data-ttu-id="323f4-145">設定這個屬性會引發 <a href="/dotnet/api/system.invalidoperationexception">InvalidOperationException</a> 例外狀況。</span><span class="sxs-lookup"><span data-stu-id="323f4-145">Setting this property raises an <a href="/dotnet/api/system.invalidoperationexception">InvalidOperationException</a> exception.</span></span>
    </blockquote>
    <br/></td>
    </tr>
    </tbody>
    </table>

    

     

-   <span data-ttu-id="323f4-146">當處置子 **realtimestylus** 時，父 [**realtimestylus**](realtimestylus-class.md)物件應該會停止運作。</span><span class="sxs-lookup"><span data-stu-id="323f4-146">The parent [**RealTimeStylus**](realtimestylus-class.md) object is expected to stop functioning when the child **RealTimeStylus** is Disposed.</span></span>

 

 
