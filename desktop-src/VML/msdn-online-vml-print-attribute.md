---
title: VML 列印屬性
description: VML 列印屬性
ms.assetid: ef9f9f11-782a-40db-986c-946d9ee03071
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55925621ab56f011c998f3feac21a892a4d7ea66
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106983299"
---
# <a name="vml-print-attribute"></a>VML 列印屬性

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

決定是否要列印圖形。 讀取/寫入 [VgTriState](msdn-online-vml-vgtristate.md)。

**適用於**

[形狀](shape-element--vml.md)

**標記語法**

<v： *element* print = " *expression* " >

**指令碼語法**

*element* = "*expression*"

*運算式* =*元素*。列印

**備註**

提供以指定是否列印圖形的方式。 請注意，即使在這個屬性為 **False** 的情況下，圖形仍可以顯示在螢幕上。 預設值是 **True**。

Microsoft Office 會使用這個屬性，但 Microsoft Internet Explorer 不會使用此屬性。

*Microsoft Office Extensions 屬性*

 

 