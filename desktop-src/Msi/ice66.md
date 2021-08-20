---
description: ICE66 會使用資料庫中的資料表，來判斷您的資料庫應該使用哪一個架構。
ms.assetid: 7cf929a0-2c4c-40ca-a902-dfd9dcd203b8
title: ICE66
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 023450a451a412c47c21904ab96a13e4513c71f8327966dffa5b657b1b65bb65
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119787398"
---
# <a name="ice66"></a>ICE66

ICE66 會使用資料庫中的資料表，來判斷您的資料庫應該使用哪一個架構。

只有當封裝安裝在具有目前 Windows Installer 版本的系統上時，才能使用某些功能。

## <a name="result"></a>結果

如果您的資料庫使用錯誤的架構，ICE66 會張貼警告。

## <a name="example"></a>範例

ICE66 會針對所顯示的範例報告下列警告。

``` syntax
WARNING: Complete functionality of the IsolatedComponents table is only available with Windows Installer versions 1.1 or greater. Your schema is 100.
```

如果您想要使用目前的 Windows Installer 版本安裝封裝，可以忽略這個警告。 例如，如果您只想要在2.0 版或更新版本上安裝套件，請將您的封裝架構 (PID \_ PAGECOUNT) 變更為200。

[IsolatedComponent 資料表](isolatedcomponent-table.md)



| 元件 \_ 共用 | 元件 \_ 應用程式 |
|-------------------|------------------------|
| Component1        | Component2             |



 

[摘要資訊串流](summary-information-stream.md)



| PIDt           | 值 |
|----------------|-------|
| PID \_ PAGECOUNT | 100   |



 

## <a name="table-used-during-execution"></a>執行期間所使用的資料表：

[\_Columns 資料表](-columns-table.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ICE 參考](ice-reference.md)
</dt> </dl>

 

 



