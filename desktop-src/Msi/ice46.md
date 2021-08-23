---
description: ICE46 只會在一或多個字元的情況下，檢查條件中的自訂屬性、格式化的文字，以及與系統定義的屬性不同的其他位置。
ms.assetid: 892d7462-0222-4fa0-b14c-17742a266c0a
title: ICE46
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbe334f973449ffe8bdbba1eb51347576c0b39c6b8eacfb8103970726dbc1ec6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119580988"
---
# <a name="ice46"></a>ICE46

ICE46 只會在一或多個字元的情況下，檢查條件中的自訂屬性、格式化的文字，以及與系統定義的屬性不同的其他位置。

## <a name="result"></a>結果

如果條件中有自訂屬性、格式化的文字，以及在一或多個字元的情況下與系統定義的屬性不同的其他位置，ICE46 會張貼參考用訊息。

## <a name="example"></a>範例

ICE46 會針對所顯示的範例報告下列錯誤。



| ICE46 錯誤                                                                                                                                            | 描述                                                                                                                                                                                                                   |
|--------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 在屬性資料表中定義的屬性 ReinstallMode，與另一個已定義的屬性不同，只有大小寫。                                                   | 系統定義的屬性名稱 **REINSTALLMODE** 與自訂屬性的大小寫不同。 屬性會區分大小寫，因此自訂屬性與系統屬性不同。 這是錯誤的常見原因。 |
| 在資料行 ' InstallExecuteSequence ' 中參考的屬性 ' Myproperty '。資料列 ' InstallFinalize ' 的條件 ' 與已定義的屬性（僅限大小寫）不同。 | 屬性工作表定義了資料表 MyProperty，但是參考的屬性是 Myproperty。 屬性會區分大小寫，因此這兩個屬性不相同。 這是錯誤的常見原因。                          |



 

[屬性工作表](property-table.md)



| 屬性      | 值   |
|---------------|---------|
| ReinstallMode | omus reinstall    |
| MyProperty    | 值 |



 

[InstallExecuteSequence 資料表](installexecutesequence-table.md) (部分) 



| 動作          | 條件  |
|-----------------|------------|
| InstallFinalize | Myproperty |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ICE 參考](ice-reference.md)
</dt> </dl>

 

 



