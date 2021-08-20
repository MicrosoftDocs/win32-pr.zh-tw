---
title: 儲存體物件命名慣例
description: 儲存體和資料流程物件是根據一組慣例來命名。
ms.assetid: 72e87c6a-cce5-4456-8336-c657e65c0a34
keywords:
- 結構化儲存體 Strctd Stg.、基本概念、儲存物件命名慣例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acebeabfbd5ba41a66ee102d2939498064fc3d852d29db4ce54cfd18878eda94
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117960197"
---
# <a name="storage-object-naming-conventions"></a>儲存體物件命名慣例

儲存體和資料流程物件是根據一組慣例來命名。

根儲存物件的名稱是基礎檔案系統中的實際檔案名。 它符合檔案系統所強加的慣例和限制。 傳遞至儲存相關方法和函式的檔案名字串，會以不會的方式傳遞至檔案系統。

儲存物件內所包含之嵌套專案的名稱是由特定儲存物件的執行所管理。 所有儲存體物件的執行都必須支援長度為32個字元的嵌套元素名稱 (包括 Null 結束字元) ，不過某些實 **值** 可能會支援較長的名稱。 儲存物件是否執行任何大小寫轉換都是實作為定義。 如此一來，定義專案名稱的應用程式必須選擇是否執行大小寫轉換時可接受的名稱。 複合檔案的 COM 執行支援最大長度為32個字元的名稱，且不會執行任何大小寫轉換。

 

 




