---
description: ICE57 會驗證個別的元件不會混用每部電腦和每個使用者的資料。 這個 ICE 自訂動作會檢查登錄專案、檔案、目錄金鑰路徑，以及非公告的快捷方式。
ms.assetid: 3c82efa7-9cf3-4bcd-8ec4-b81d1d7aa0a6
title: ICE57
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d875264ed1fbc0f7dedac863c21801e5180ae879c9c255af7cf4b36e5d402970
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118635159"
---
# <a name="ice57"></a>ICE57

ICE57 會驗證個別的元件不會混用每部電腦和每個使用者的資料。 這個 ICE 自訂動作會檢查登錄專案、檔案、目錄金鑰路徑，以及非公告的快捷方式。

混用相同元件中的每位使用者和每部電腦資料，可能會導致多使用者環境中的部分使用者只部分安裝元件。

請參閱 [**ALLUSERS**](allusers.md) 屬性。

## <a name="result"></a>結果

如果 ICE57 找到任何包含每一電腦和每個使用者登錄專案、檔案、目錄金鑰路徑或非公告快速鍵的元件，則會張貼錯誤。

## <a name="example"></a>範例

針對顯示的範例 ICE57reports 下列錯誤。

``` syntax
Component 'Component1' has both per-user and per-machine 
    data with a per-machine KeyPath. 
 
WARNING: Component 'Component2' has both per-user and 
    per-machine data with an HKCU Registry KeyPath. 
 
Component 'Component3' has a registry entry that 
    can be either per-user or per-machine and a per-machine KeyPath. 
 
Component 'Component4' has both per-user data and 
    a keypath that can be either per-user or per-machine.
```

[元件資料表](component-table.md) (部分) 



| 元件  | 目錄  | 屬性 | KeyPath |
|------------|------------|------------|---------|
| Component1 | DirectoryA | 0          | >filea.docx   |
| Component2 | DirectoryA | 4          | RegKeyB |
| Component3 | DirectoryA | 0          | FileC   |
| Component4 | DirectoryA | 4          | RegKeyD |



 

登錄[表](registry-table.md) (部分) 



| 登錄 | Root | 元件\_ |
|----------|------|-------------|
| RegKeyA  | 1    | Component1  |
| RegKeyB  | 1    | Component2  |
| RegKeyC  | -1   | Component3  |
| RegKeyD  | -1   | Component4  |



 

[檔資料表](file-table.md) (部分) 



| 檔案  | 元件\_ |
|-------|-------------|
| >filea.docx | Component1  |
| >fileb.docx | Component2  |
| FileC | Component3  |
| 提交 | Component4  |



 

[目錄資料表](directory-table.md)



| 目錄  | 目錄 \_ 父系 | DefaultDir |
|------------|-------------------|------------|
| TARGETDIR  |                   | SourceDir  |
| DirectoryA | TARGETDIR         | DirectoryA |



 

若要修正錯誤，請重新組織應用程式，讓每個元件只包含每個使用者或每一電腦的資源，而不是兩者都包含。

第一個錯誤訊息是張貼的，因為 Component1 包含每一電腦的 >filea.docx () ，而 HKCU 登錄機碼 RegKeyA (每個使用者) 。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ICE 參考](ice-reference.md)
</dt> </dl>

 

 



