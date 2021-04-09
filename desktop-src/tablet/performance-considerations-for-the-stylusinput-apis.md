---
description: 說明使用 StylusInput 應用程式開發介面)  (Api 時，增強效能的方法。
ms.assetid: 2a541715-2d9e-4eb2-ab60-ec95368fca5a
title: StylusInput API 的效能考慮
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 721474f1e1097729246e5d497d20dcab868190a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103695179"
---
# <a name="performance-considerations-for-the-stylusinput-api"></a><span data-ttu-id="40cd0-103">StylusInput API 的效能考慮</span><span class="sxs-lookup"><span data-stu-id="40cd0-103">Performance Considerations for the StylusInput API</span></span>

<span data-ttu-id="40cd0-104">下列清單說明使用 StylusInput Api 來改善應用程式效能的一些方法。</span><span class="sxs-lookup"><span data-stu-id="40cd0-104">The following list describes some ways in which to improve the performance of applications that use the StylusInput APIs.</span></span>

-   <span data-ttu-id="40cd0-105">使用 [StylusInput. IStylusSyncPlugin. DataInterest](/previous-versions/ms824752(v=msdn.10)) 或 [StylusInput.](/previous-versions/ms824769(v=msdn.10)) IStylusAsyncPlugin 屬性，只訂閱與您外掛程式相關的資料即可。</span><span class="sxs-lookup"><span data-stu-id="40cd0-105">Use the [Microsoft.StylusInput.IStylusSyncPlugin.DataInterest](/previous-versions/ms824752(v=msdn.10)) or [Microsoft.StylusInput.IStylusAsyncPlugin.DataInterest](/previous-versions/ms824769(v=msdn.10)) property to subscribe only to the data that is relevant to your plug-in.</span></span> <span data-ttu-id="40cd0-106">這樣可減少 [**RealTimeStylus**](realtimestylus-class.md) 物件所做的總方法呼叫數目，也可降低外掛程式的複雜度。</span><span class="sxs-lookup"><span data-stu-id="40cd0-106">This reduces the overall number of method calls the [**RealTimeStylus**](realtimestylus-class.md) object makes and also reduces the complexity of your plug-in.</span></span> <span data-ttu-id="40cd0-107">當附加外掛程式時， **RealTimeStylus** 物件只會檢查 DataInterest 屬性。</span><span class="sxs-lookup"><span data-stu-id="40cd0-107">The **RealTimeStylus** object only checks the DataInterest property when the plug-in is attached.</span></span>
-   <span data-ttu-id="40cd0-108">將同步外掛程式的複雜性降至最低。同步外掛程式通常是由 [**RealTimeStylus**](realtimestylus-class.md) 物件的執行緒所呼叫，而且可能會導致筆墨收集延遲。</span><span class="sxs-lookup"><span data-stu-id="40cd0-108">Minimize the complexity of synchronous plug-ins. Synchronous plug-ins generally called by the [**RealTimeStylus**](realtimestylus-class.md) object's thread and may contribute to delays in ink collection.</span></span>
-   <span data-ttu-id="40cd0-109">請考慮讓外掛程式成為非同步。</span><span class="sxs-lookup"><span data-stu-id="40cd0-109">Consider making your plug-in asynchronous.</span></span> <span data-ttu-id="40cd0-110">如果您的外掛程式很複雜，而且需要將自訂資料新增至 [**RealTimeStylus**](realtimestylus-class.md) 物件的佇列，請考慮使用串聯的 **realtimestylus** 模型，並將外掛程式加入至次要 **RealTimeStylus** 物件的同步外掛程式集合。</span><span class="sxs-lookup"><span data-stu-id="40cd0-110">If your plug-in is complex and needs to add custom data to the [**RealTimeStylus**](realtimestylus-class.md) object's queue, consider using a cascaded **RealTimeStylus** model and adding the plug-in to the secondary **RealTimeStylus** object's synchronous plug-in collection.</span></span> <span data-ttu-id="40cd0-111">如需有關串聯的 **realtimestylus** 模型的詳細資訊，請參閱 [串聯的 realtimestylus 模型](the-cascaded-realtimestylus-model.md)。</span><span class="sxs-lookup"><span data-stu-id="40cd0-111">For more information about the cascaded **RealTimeStylus** model, see [The Cascaded RealTimeStylus Model](the-cascaded-realtimestylus-model.md).</span></span>

 

 
