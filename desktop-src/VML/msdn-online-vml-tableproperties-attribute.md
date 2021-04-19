---
title: VML TableProperties 屬性
description: VML TableProperties 屬性
ms.assetid: 10355742-13b9-4c08-bff7-f7f7501762e9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f0f010f673b2663764814150f7a38fc06f23e11
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106967897"
---
# <a name="vml-tableproperties-attribute"></a>VML TableProperties 屬性

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

決定資料表屬性。 讀取/寫入 **Integer** (整數)。

**適用於**

[形狀](shape-element--vml.md)

**標記語法**

<v： *element* o:tableproperties = " *expression* " >

**備註**

由 Microsoft PowerPoint 用於原生資料表。 預設值為 0。 只會使用這個整數的前三個位。

雖然此值是儲存在圖形中，但此屬性只有在資料表是由群組的圖形組成時才有用。可以合併位。

包含下列位值。



| bit | 描述                              |
|-----|------------------------------------------|
| 1   | 設定圖形群組是否為數據表。   |
| 2   | 設定圖形是否為預留位置。       |
| 3   | 設定資料表文字是否為雙向。 |



 

*Microsoft Office Extensions 屬性*

 

 