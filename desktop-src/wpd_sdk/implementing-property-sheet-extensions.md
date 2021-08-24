---
description: 執行屬性工作表延伸模組
ms.assetid: 5d1f9d91-e8a1-4cbb-b1de-4262a61e3cb7
title: 執行屬性工作表延伸模組
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23b4f74559176ecc0c411f75e7ca630db152a51109f09ecdca47a62d0113e70c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119590278"
---
# <a name="implementing-property-sheet-extensions"></a>執行屬性工作表延伸模組

WPD 命名空間延伸模組支援可擴充的屬性工作表。 當使用者以滑鼠右鍵按一下某個物件（例如檔案或資料夾）並選取 [ **屬性**] 時，就會出現這些屬性對話方塊。 某些 WPD 應用程式會利用這些可延伸的屬性工作表來顯示裝置端內容 (的屬性，或是位於裝置) 的物件。

下表所述的介面支援可延伸的屬性工作表。 如需這些介面的詳細資訊，請參閱 Windows SDK。



| 介面           | 描述                                                                  |
|---------------------|------------------------------------------------------------------------------|
| IDataObject         | 用來將內容功能表的 PIDL 陣列傳遞至內容功能表處理常式。      |
| IPropertySetStorage | 這個介面是用來取得指定物件的 WPD 屬性。      |
| IPropertyStorage    | 這個介面也用來取出指定物件的 WPD 屬性。 |
| IShellExtInit       | 初始化內容功能表的 Windows Vista Shell 擴充功能。         |
| IShellPropSheetExt  | 支援加入屬性工作表延伸模組。                              |



 

WPD 的屬性工作表會像 Windows Vista 中的任何其他屬性工作表一樣執行。 如果您已經執行屬性工作表處理常式，您可以修改現有的程式碼，使其支援裝置端的內容。 如果您從未建立內容功能表處理常式，請參閱 Windows SDK 中的建立屬性工作表處理常式主題。

WPD 屬性工作表處理常式與任何其他處理常式不同的點是在處理常式註冊和裝置端內容支援。

 

 



