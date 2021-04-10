---
description: ICE38 會驗證在目前使用者的設定檔下安裝的每個元件，也會在 \_ \_ 元件資料表的 KeyPath 資料行中的 [HKEY 目前的使用者根目錄] 下指定一個登錄機碼。
ms.assetid: f1548b04-78c2-461a-a729-9a8c4856d0d8
title: ICE38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d001d244160f939a73e697e677bf43a1f5f825f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027023"
---
# <a name="ice38"></a>ICE38

ICE38 會驗證在目前使用者的設定檔下安裝的每個元件，也會在 [元件資料表](component-table.md)的 KeyPath 資料行中的 [ **HKEY \_ 目前的 \_ 使用者** 根目錄] 下指定一個登錄機碼。

## <a name="result"></a>結果

如果安裝在使用者設定檔之下的元件未指定 HKCU 登錄機碼，ICE38 會張貼錯誤。

## <a name="example"></a>範例

ICE38 會針對所顯示的範例報告下列錯誤。



| ICE38 錯誤                                                                                                                         | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 元件 Component1 會安裝到使用者設定檔。 它必須使用 HKCU 下的登錄機碼作為其 KeyPath，而不是檔案。                    | Component1 的 attributes 資料行值為0，表示元件必須使用檔案作為其 KeyPath。 當多位使用者在同一部電腦上安裝元件時，這會造成困難。 若要在 Component1 上修正這個錯誤，請在 [元件資料表](component-table.md) 的 [屬性] 資料行中設定 RegistryKeyPath 位，然後將 [KeyPath] 資料行中的專案變更為登錄 [資料表](registry-table.md)的登錄資料行中所列的值。<br/>                                                                                |
| 元件 Component2 會安裝到使用者設定檔。 它必須使用 HKCU 下的登錄機碼作為其 KeyPath。 KeyPath 目前為 Null。 | Component2 已在 [元件資料表](component-table.md)的 [屬性] 資料行中設定 RegistryKeyPath 位。 因此，KeyPath 欄位必須包含登錄 [資料表](registry-table.md) 登錄資料行的索引鍵，但 KeyPath 資料行則為 Null。 若要修正這個錯誤，請將 KeyPath 值變更為登錄資料表中的有效專案。<br/>                                                                                                                                                                                                     |
| 元件 Component3 會安裝到使用者設定檔。 它的 KeyPath 登錄機碼必須落在 HKCU 下。                                      | Component3 在 [元件資料表](component-table.md) 的 [屬性] 資料行中設定 RegistryKeyPath 位，但登錄表的根資料行中所指定之登錄專案的根目錄指定 **了 \_ HKEY \_ 本機電腦** ，而不是 **HKEY 目前的 \_ \_ 使用者**。 若要修正這個錯誤，請使用 **HKEY \_ 本機 \_ 電腦** 下的有效登錄專案作為此元件的 KeyPath，或將登錄 [資料表](registry-table.md) 之根資料行中的值變更為-1 或1。<br/>                                                                  |
| 元件 Component4 的 KeyPath 登錄專案不存在。                                                                 | Component4 在 [Component 資料表](component-table.md) 的 Attributes 資料行中設定 RegistryKeyPath 位，但 KeyPath 資料行中的專案不存在於登錄 [資料表](registry-table.md)中。 若要修正這個錯誤，請將 Reg4 的專案加入至 **HKEY \_ 目前 \_ 使用者** 底下的登錄資料表。<br/>                                                                                                                                                                                                                                      |
| 登錄專案 Reg5 設定為元件 Component5 的 KeyPath，但該登錄專案不屬於 Component5。      | 在元件的 KeyPath 資料行中所參考的登錄專案是在 HKCU 樹狀目錄下找到，但登錄專案的 [元件] 資料 \_ 行不會回頭參考列為 KeyPath 的相同元件。 這表示只會在安裝其他元件時，才會建立用來作為元件 KeyPath 的登錄專案。 若要修正這個錯誤，請將 KeyPath 值變更為參考屬於元件的登錄專案，或是將登錄專案變更為屬於 KeyPath 的元件。<br/> |



 

[目錄資料表](directory-table.md) (部分) 



| 目錄 | 目錄 \_ 父系 | DefaultDir      |
|-----------|-------------------|-----------------|
| Dir1      |                   | StartMenuFolder |
| Dir2      |                   | DesktopFolder   |
| Dir3      | Dir3              | AppData         |
| Dir4      | Dir3              | SubDir          |



 

[元件資料表](component-table.md) (部分) 



| 元件  | 目錄\_ | 屬性 | KeyPath |
|------------|-------------|------------|---------|
| Component1 | Dir1        | 0          | File1   |
| Component2 | Dir2        | 4          |         |
| Component3 | Dir3        | 4          | Reg3    |
| Component4 | Dir4        | 4          | Reg4    |
| Component5 | Dir5        | 4          | Reg5    |



 

登錄[表](registry-table.md) (部分) 



| 登錄 | Root | 值 | 元件\_ |
|----------|------|-------|-------------|
| Reg3     | 2    |       | Component3  |
| Reg5     | 0    |       | Component4  |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ICE 參考](ice-reference.md)
</dt> </dl>

 

 




