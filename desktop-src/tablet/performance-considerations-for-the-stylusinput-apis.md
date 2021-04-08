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
# <a name="performance-considerations-for-the-stylusinput-api"></a>StylusInput API 的效能考慮

下列清單說明使用 StylusInput Api 來改善應用程式效能的一些方法。

-   使用 [StylusInput. IStylusSyncPlugin. DataInterest](/previous-versions/ms824752(v=msdn.10)) 或 [StylusInput.](/previous-versions/ms824769(v=msdn.10)) IStylusAsyncPlugin 屬性，只訂閱與您外掛程式相關的資料即可。 這樣可減少 [**RealTimeStylus**](realtimestylus-class.md) 物件所做的總方法呼叫數目，也可降低外掛程式的複雜度。 當附加外掛程式時， **RealTimeStylus** 物件只會檢查 DataInterest 屬性。
-   將同步外掛程式的複雜性降至最低。同步外掛程式通常是由 [**RealTimeStylus**](realtimestylus-class.md) 物件的執行緒所呼叫，而且可能會導致筆墨收集延遲。
-   請考慮讓外掛程式成為非同步。 如果您的外掛程式很複雜，而且需要將自訂資料新增至 [**RealTimeStylus**](realtimestylus-class.md) 物件的佇列，請考慮使用串聯的 **realtimestylus** 模型，並將外掛程式加入至次要 **RealTimeStylus** 物件的同步外掛程式集合。 如需有關串聯的 **realtimestylus** 模型的詳細資訊，請參閱 [串聯的 realtimestylus 模型](the-cascaded-realtimestylus-model.md)。

 

 
