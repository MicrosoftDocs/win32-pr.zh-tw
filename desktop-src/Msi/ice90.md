---
description: 如果 ICE90 發現快捷方式的目錄已指定為公用屬性，則會張貼警告。
ms.assetid: 47565d9b-c3c2-4a5c-8f91-2b3912a63b47
title: ICE90
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fba38ba074bf939431f497e8aab73ec0640d7bbc66fb0998498ce190d99fd92
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894948"
---
# <a name="ice90"></a>ICE90

如果 ICE90 發現快捷方式的目錄已指定為公用屬性，則會張貼警告。 [公用屬性](public-properties.md)的名稱是以大寫字母撰寫。 如果 [**ALLUSERS**](allusers.md) 屬性的值變更，則公用屬性指定的快捷方式可能無法運作。

此 ICE 自訂動作會驗證快速鍵資料表並使用目錄資料表。 如果目錄資料表不存在，則會在未驗證快速鍵資料表的情況下傳回，而且不會張貼任何錯誤或警告。

## <a name="result"></a>結果

ICE90 會張貼下列警告。



| ICE90 錯誤                                                                                                                                                                                                                    | 描述                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| 快速鍵 ' \[ 1 \] ' 的目錄是公用屬性 (所有 CAPS) ，而且位於使用者設定檔目錄下。 如果 UI 順序中的 [**ALLUSERS**](allusers.md) 屬性值變更，這會導致問題。 | 快速鍵的目錄已指定為公用屬性。 |



 

## <a name="example"></a>範例

ICE90 會報告下列範例警告：

``` syntax
The shortcut 'Shortcut1' has a directory that is a public property (ALL CAPS) 
and is under user profile directory. This results in a problem if the value 
of the ALLUSERS property changes in the UI sequence.
```

在此範例中，MYDIR 是在使用者設定檔下。 ICE90 會張貼警告，因為目標目錄的位置是由公用屬性 MYDIR 所指定。 使用者可變更 MYDIR 或 [**ALLUSERS**](allusers.md) 屬性。 如果針對每部電腦 [安裝內容](installation-context.md)設定 **ALLUSERS** ，而 MYDIR 是在使用者設定檔下，MYDIR 中的快捷方式檔案就會複製到 [所有使用者] 設定檔下，而不是特定使用者的設定檔。 如果針對每個使用者安裝內容設定 **ALLUSERS** ，MYDIR 中的快捷方式檔案就會複製到特定使用者的設定檔中，而不會提供給其他使用者使用。

 (部分) 的[快捷方式資料表](shortcut-table.md)



| 快速鍵  | 目錄\_ |
|-----------|-------------|
| Shortcut1 | MYDIR       |



 

[目錄資料表](directory-table.md) (部分) 



| 目錄 | 目錄 \_ 父系 |
|-----------|-------------------|
| MYDIR     | ProgramMenuFolder |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ICE 參考](ice-reference.md)
</dt> </dl>

 

 



