---
description: BindImage 資料表包含每個可執行檔或 DLL 的相關資訊，這些可執行檔或 DLL 必須系結至它所匯入的 Dll。
ms.assetid: 68bf064c-dd85-4796-8e08-6af307f94ad8
title: BindImage 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f47b97efc8886d7748d0426a49ed76567810939c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943998"
---
# <a name="bindimage-table"></a>BindImage 資料表

BindImage 資料表包含每個可執行檔或 DLL 的相關資訊，這些可執行檔或 DLL 必須系結至它所匯入的 Dll。

BindImage 資料表具有下列資料行。



| Column | 類型                         | 答案 | Nullable |
|--------|------------------------------|-----|----------|
| 檔案\_ | [識別碼](identifier.md) | Y   | N        |
| 路徑   | [路徑](paths.md)           | N   | Y        |



 

## <a name="columns"></a>資料行

<dl> <dt>

<span id="File_"></span><span id="file_"></span><span id="FILE_"></span>檔\_
</dt> <dd>

檔案 [資料表](file-table.md)中第一個資料行的外部索引鍵。 這必須是可執行檔或 DLL 檔案。

</dd> <dt>

<span id="Path"></span><span id="path"></span><span id="PATH"></span>路徑
</dt> <dd>

以分號分隔的路徑清單，表示要搜尋以尋找匯入之 Dll 的路徑。 清單通常是屬性清單，其中每個屬性都以方括弧括住 (\[ \]) 中。

</dd> </dl>

## <a name="remarks"></a>備註

安裝程式會計算從所有 Dll 匯入之每個函式的虛擬位址，然後計算的虛擬位址會儲存在匯入映射的匯入位址表中 (IAT) 。

當 [BindImage 動作](bindimage-action.md) 執行時，就會參考此資料表。

## <a name="validation"></a>驗證

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE46](ice46.md)  
[ICE76](ice76.md)  
</dl>

 

 



