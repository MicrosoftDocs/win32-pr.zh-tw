---
description: ICE42 會驗證 InProc 伺服器是否未連結至類別表中的 EXE 檔案。 它也會驗證只有 LocalServer 和 LocalServer32 類別具有引數和 DefInProc 值。
ms.assetid: 14976772-c873-46d8-8687-dcdad2420d83
title: ICE42
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebe2ea09431870ac7b52ccd69d0ae16c646286ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106983713"
---
# <a name="ice42"></a>ICE42

ICE42 會驗證 InProc 伺服器是否未連結至 [類別表](class-table.md)中的 EXE 檔案。 它也會驗證只有 LocalServer 和 LocalServer32 類別具有引數和 DefInProc 值。

## <a name="result"></a>結果

如果有 InProc 伺服器連結至類別資料表中的 EXE 檔案，ICE42 會張貼錯誤。

## <a name="example"></a>範例

ICE42 會針對所顯示的範例報告下列錯誤。



| ICE42 錯誤                                                                                                                             | Description                                                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CLSID ' {GUID1} ' 是 InProc 伺服器，但正在執行的元件 ' Component1 ' 有 EXE ( ' test.exe ' ) 作為 KeyFile。                | 有一個可執行檔指定為 InProc 伺服器。 EXE 檔案不能是 InProc 伺服器。                                                                                                                            |
| 內容 ' InProcServer32 ' 中的 CLSID ' {GUID1} ' 有引數。 只有 LocalServer 內容可以有引數。                              | 若要修正這個錯誤，請移除引數。                                                                                                                                                                                   |
| 內容 ' InProcServer32 ' 中的 CLSID ' {GUID1} ' 指定了預設 InProc 值。 只有 LocalServer 內容可以有預設 InProc 值。 | 具有預設 InProc 值的物件不是在 LocalServer 或 LocalServer32 內容中運作的物件。 若要修正這個錯誤，請移除 DeflnProc 值或變更類別的內容。<br/> |



 

[類別表](class-table.md) (部分) 



| CLSID   | Context        | 元件\_ | DefInProcHandler | 引數 |
|---------|----------------|-------------|------------------|----------|
| GUID1 | InProcServer32 | Component1  | InProcServer     | 精 氨 酸      |



 

[元件資料表](component-table.md) (部分) 



| 元件  | KeyPath |
|------------|---------|
| Component1 | File1   |



 

[檔資料表](file-table.md) (部分) 



| 檔案  | 檔案名稱 |
|-------|----------|
| File1 | test.exe |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ICE 參考](ice-reference.md)
</dt> </dl>

 

 




