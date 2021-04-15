---
title: VML IVgAdjustments 資料類型
description: VML IVgAdjustments 資料類型
ms.assetid: d605632b-3ee2-44fd-8122-f38b1f91e965
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a29f85f93218db098ca247fa66b1f493e9c622a5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463304"
---
# <a name="vml-ivgadjustments-data-type"></a>VML IVgAdjustments 資料類型

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

可在公式中使用之圖形的調整集合。 調整可用來作為暫時預留位置，或因任何原因而使用變數。 集合中只有8項調整。



| 屬性 | Description                                                                                                                                                                                                                                                                                                                            |
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 長度     | **Integer** (整數)。 調整的數目。 不能大於8。                                                                                                                                                                                                                                                                          |
| 項目       | **Long**。 從0到7的索引調整陣列。 請注意，可能會 sparcely 指定調整;也就是說，中繼陣列值可能不一定會填滿。 例如，專案1、3和5的值可能是3，而專案 (0) 、專案 (2) 和專案 (4) 指定。 若要查看專案是否存在，請使用 Exists 屬性。 |
| Exists     | **IVgTriState**。 判斷指定的調整是否存在。 請注意，必須使用索引;也就是說， (專案) 必須用來取出專案的存在。                                                                                                                                                           |
| 值      | **字串**。 數值的文字標記法，每個數位之間都有逗號。                                                                                                                                                                                                                                                    |



 

 

 