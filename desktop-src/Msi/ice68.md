---
description: ICE68 會檢查安裝所需的所有自訂動作類型是否有效。
ms.assetid: a37d6d6c-3005-425b-883a-6fe074b9d708
title: ICE68
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1392db6ec05085c672ed70c8f035ea8eed3015e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987393"
---
# <a name="ice68"></a>ICE68

ICE68 會檢查安裝所需的所有自訂動作類型是否有效。 若無法修正 ICE68 所回報的錯誤，會導致嘗試執行動作失敗的安裝。 如果設定 **msidbCustomActionTypeNoImpersonate** 屬性時未同時設定 **MSIDBCUSTOMACTIONTYPEINSCRIPT** 屬性，ICE68 會發出警告。

## <a name="result"></a>結果

如果安裝所需的動作類型無效，ICE68 會傳回錯誤。

## <a name="example"></a>範例

如果自訂動作在 CustomAction 資料表的類型欄位中設定 **msidbCustomActionTypeNoImpersonate** 位，但未設定 **msidbCustomActionTypeInScript** ，ICE68 會張貼下列警告。

``` syntax
Even though custom action '[2]' is marked to be elevated (with 
attribute msidbCustomActionTypeNoImpersonate), it will not be run with elevated 
privileges because it's not deferred (with attribute msidbCustomActionTypeInScript).
```

若要修正此警告，請在自訂動作包含 **msidbCustomActionTypeNoImpersonate** (0x800) 時，包括 **msidbCustomActionTypeInScript** (0x400) 。 否則，安裝程式會忽略 **msidbCustomActionTypeNoImpersonate** 屬性。 如需詳細資訊，請參閱 [自訂動作 In-Script 執行選項](custom-action-in-script-execution-options.md)。

ICE68 會針對所顯示的範例報告下列錯誤：

``` syntax
Invalid custom action type for action 'Action1'.
```

1027不是有效的動作類型。

若要修正這個錯誤，請選擇有效的自訂動作類型。

[CustomAction 資料表](customaction-table.md) (部分) 



| 動作  | 類型 | 來源   | 目標     |
|---------|------|----------|------------|
| Action1 | 1027 | 引數 | Component1 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ICE 參考](ice-reference.md)
</dt> </dl>

 

 



