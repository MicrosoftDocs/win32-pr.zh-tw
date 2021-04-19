---
description: 執行內容功能表延伸模組
ms.assetid: b8bea667-b9ea-476d-942f-281cb2e9636c
title: 執行內容功能表延伸模組
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c65918f385984355490456cccb626ba297bd3368
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997530"
---
# <a name="implementing-context-menu-extensions"></a>執行內容功能表延伸模組

WPD 命名空間延伸模組支援可擴充的內容 (或快捷方式) 功能表。 這些是使用者以滑鼠右鍵按一下某個物件（例如檔案或資料夾）時所顯示的功能表。 某些 WPD 應用程式會利用這些可延伸的功能表，來支援裝置端內容 (或位於裝置) 上的物件的作業。

下表所述的介面支援可擴充的內容功能表。 如需這些介面的詳細資訊，請參閱 Windows SDK。



| 介面           | 描述                                                                                                                |
|---------------------|----------------------------------------------------------------------------------------------------------------------------|
| ICoNtextMenu        | Windows Vista Shell 會呼叫此介面中的方法，以建立新的內容功能表，或將其與指定的物件合併。 |
| IDataObject         | 用來將內容功能表的 PIDL 陣列傳遞至內容功能表處理常式。                                                    |
| IPropertySetStorage | 這個介面是用來取得指定物件的 WPD 屬性。                                                    |
| IPropertyStorage    | 這個介面也用來取出指定物件的 WPD 屬性。                                               |
| IShellExtInit       | 初始化內容功能表的 Windows Vista Shell 擴充功能。                                                       |
| IStream             | 提供。                                                                                                            |



 

WPD 的內容功能表會像 Windows Vista 中的任何其他內容功能表一樣執行。 如果您已經執行內容功能表處理常式，您可以修改現有的程式碼，使其支援裝置端的內容。 如果您從未建立內容功能表處理常式，請參閱 Windows SDK 中的建立內容功能表處理常式主題。

WPD 內容功能表處理常式與任何其他處理常式不同的點是在處理常式註冊和裝置端內容支援。

 

 



