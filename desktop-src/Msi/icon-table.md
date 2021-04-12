---
description: 此表格包含圖示檔。 資料表中的每個圖示都會複製到檔案做為產品公告的一部分，以用於公告的快捷方式和 OLE 伺服器。 請參閱 OLE 對資料流程的限制。
ms.assetid: a59c552a-21c0-4dd4-9146-88a5f9a22962
title: 圖示表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e8e8e38575dc6f6e6bda10b2c1047f3940f7559
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192445"
---
# <a name="icon-table"></a>圖示表

此表格包含圖示檔。 資料表中的每個圖示都會複製到檔案做為產品公告的一部分，以用於公告的快捷方式和 OLE 伺服器。 請參閱 [OLE 對資料流程的限制](ole-limitations-on-streams.md)。

圖示表具有下列資料行。



| Column | 類型                         | 答案 | Nullable |
|--------|------------------------------|-----|----------|
| Name   | [識別碼](identifier.md) | Y   | N        |
| 資料   | [二進位](binary.md)         | N   | N        |



 

## <a name="columns"></a>資料行

<dl> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>名字
</dt> <dd>

圖示檔的名稱。

</dd> <dt>

<span id="Data"></span><span id="data"></span><span id="DATA"></span>資料
</dt> <dd>

PE 中的二進位圖示資料 ( .dll 或 .exe) 或圖示 ( .ico) 格式。

</dd> </dl>

## <a name="remarks"></a>備註

當 [PublishProduct 動作](publishproduct-action.md) 執行時，就會參考此資料表。

快速鍵、副檔名和 Clsid 的圖示必須儲存在與目標檔案本身不同的檔案中。 這是必要的，因為安裝程式應該只在廣告資源時將小型圖示檔複製到使用者的電腦上。 因此，安裝套件的開發人員必須撰寫只包含圖示的個別檔案。 這些圖示檔接著會以二進位資料的形式儲存在圖示資料表中。

嚴格與副檔名或 Clsid 相關聯的圖示檔可以有任何副檔名，例如 .ico。 不過，與快捷方式相關聯的圖示檔必須是 EXE 二進位格式，而且必須命名，使其擴充功能符合目標的副檔名。 如果未遵循此規則，快捷方式將無法運作。 例如，如果快捷方式是指向具有金鑰檔 Red.bar 的資源，則圖示檔也必須有副檔名 bar。 只要所有目標檔案都具有相同的副檔名，就可以將多個圖示芝到相同的圖示檔。

## <a name="validation"></a>驗證

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE29](ice29.md)  
[ICE32](ice32.md)  
[ICE36](ice36.md)  
[ICE50](ice50.md)  
</dl>

 

 



