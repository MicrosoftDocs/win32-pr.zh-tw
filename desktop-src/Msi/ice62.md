---
description: ICE62 會對 IsolatedComponent 資料表執行大量檢查，以取得可能會造成非預期行為的資料。
ms.assetid: 649d3989-8121-4303-aa3e-63bc6649f445
title: ICE62
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb5c2fd3f3305c791851fb3bd7480edc5e17f361c40719e8091930188dfa991c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119528238"
---
# <a name="ice62"></a>ICE62

ICE62 會對 [IsolatedComponent 資料表](isolatedcomponent-table.md) 執行大量檢查，以取得可能會造成非預期行為的資料。

若無法修正 ICE62 回報的錯誤，可能會以各種不同的方式導致隔離元件系統失敗。 例如，如果未設定共用元件的 SharedDllRefCount 位，當另一個應用程式使用該配置器且已卸載時，就可以移除元件的註冊。

## <a name="result"></a>結果

當 ICE62 在 IsolatedComponent 資料表中找到可能會產生非預期行為的資料時，會張貼警告或錯誤。

## <a name="example"></a>範例

ICE62 會針對所顯示的範例報告下列錯誤和警告。

``` syntax
The component 'Component2' is listed as an isolated application 
component in the IsolatedComponent table, but the key path is not a file.
```

Component2 會列為隔離 component1 的應用程式元件。 不過，Component2 有一個登錄機碼路徑，而且不提供可用於隔離元件的有效可執行檔路徑。

若要修正這個錯誤，請使用不同的元件作為隔離元件 Component1 的應用程式。

``` syntax
The component 'Component1' is listed as an isolated shared component in the 
IsolatedComponent table, but is not marked with the SharedDllRefCount component attribute.
```

Component1 列為隔離的共用元件，但未設定 SharedDllRefCount 位。 這可能會導致元件的存留期不正確。 如果另一個應用程式使用此元件 (隔離或未) 並已卸載，則會移除該元件的註冊，但會保留此應用程式的獨立複本。 這會導致修復和卸載問題。

若要修正這個錯誤，請設定元件的 SharedDllRefCount 位。

``` syntax
The isolated shared component 'Component1' is not installed by the same feature as 
(or a parent feature of) its isolated application component 'Component2' (which is installed by feature 'Feature2').
```

Component1 和 Component2 是由不同的功能所安裝。 Component1 是由 Feature1 所安裝，而 Component2 則是由 Feature2 安裝。 Feature1 不是 Feature2 的父系，因此可能會安裝應用程式，而不是隔離的元件，進而中斷隔離。

若要修正這個錯誤，請將專案加入至 FeatureComponents 資料表，以將 Component1 連結至 (的相同功能，或) 安裝 Component2 之功能的父功能。

``` syntax
WARNING: The isolated shared component 'Component1' (referenced in the IsolatedComponent table) 
is conditionalized. Isolated shared component conditions should never change from TRUE to FALSE after the first install of the product.
```

Component1 在元件資料表中有條件。 如果在電腦上安裝的存留期內，此情況的變更為 FALSE，則隔離的元件可能會在沒有註冊資訊的情況下孤立。

若要修正這個警告，請移除條件，或撰寫條件，讓它永遠不會從 TRUE 變更為 FALSE。

``` syntax
WARNING: The isolated shared component 'Component1' is shared by multiple applications 
(including 'Component2') that are installed to the directory 'TARGETDIR'.
WARNING: The isolated shared component 'Component1' is shared by multiple applications 
(including 'Component3') that are installed to the directory 'TARGETDIR'.
```

Component1 會針對 Component2 和 Component3 隔離，而這兩個元件也會安裝在相同的目錄中。 應用程式會共用隔離的元件，但如果移除一個應用程式，則會移除共用的元件，也會導致其他應用程式遺失隔離的元件。

若要修正此警告，請將應用程式安裝到不同的目錄，或檢查是否有一些應用程式確實需要隔離的元件。

[IsolatedComponent 資料表](isolatedcomponent-table.md)



| 元件 \_ 共用 | 元件 \_ 應用程式 |
|-------------------|------------------------|
| Component1        | Component2             |
| Component1        | Component3             |



 

[元件資料表](component-table.md)



| 元件  | ComponentId | 目錄\_ | 屬性 | 條件   | KeyPath   |
|------------|-------------|-------------|------------|-------------|-----------|
| Component1 |             | Dir1        | 0          | MYCONDITION | File1     |
| Component2 |             | TARGETDIR   | 4          |             | Registry2 |
| Component3 |             | TARGETDIR   | 0          |             | File3     |



 

[FeatureComponentsTable](featurecomponents-table.md)



| 特徵\_ | 元件\_ |
|-----------|-------------|
| Feature1  | Component1  |
| Feature2  | Component2  |
| Feature1  | Component3  |



 

[功能表](feature-table.md) (部分) 



| 功能  | 功能 \_ 父系 |
|----------|-----------------|
| Feature1 |                 |
| Feature2 |                 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ICE 參考](ice-reference.md)
</dt> </dl>

 

 



