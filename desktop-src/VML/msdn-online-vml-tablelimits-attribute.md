---
title: VML TableLimits 屬性
description: VML TableLimits 屬性
ms.assetid: eef855de-23c5-4894-b7cf-2ea39e372e08
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af52ba570b04e56f1dede169045f7ee1addf374fae5ca4f1cd5de4d9390f1235
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959248"
---
# <a name="vml-tablelimits-attribute"></a>VML TableLimits 屬性

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需有關 Windows Internet Explorer 目前版本的資訊、建議和指引，請參閱[Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

資料表中每個資料列的最小高度值清單。 讀取/寫入 **VgLengthArray**。

**適用於**

[圖形](shape-element--vml.md)

**標記語法**

<v： *element* o:tablelimits = " *expression* " >

**備註**

由 Microsoft PowerPoint 用於原生資料表。 預設值為 **Null**。

雖然此值是儲存在圖形中，但此屬性只有在資料表是由群組的圖形組成時才有用。 將文字加入至資料表資料格時，資料列高度可能會增加。 **TableLimits** 屬性會儲存原始資料列的高度，因此，如果刪除文字，資料列高度將不會低於原始值。

*Microsoft OfficeExtensions 屬性*

 

 