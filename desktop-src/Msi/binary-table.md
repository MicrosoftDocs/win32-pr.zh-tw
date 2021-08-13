---
description: 二進位資料表會保存點陣圖、動畫和圖示等專案的二進位資料。 二進位資料表也用來儲存自訂動作的資料。 請參閱 OLE 對資料流程的限制。
ms.assetid: 44c56407-df2e-4cbe-b7a3-b22e8d97eb03
title: 二進位資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a70750193b1dc147a9b2b4cfa01bbea410f0e44b7c03f16bd1c992f118a4f0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118638802"
---
# <a name="binary-table"></a>二進位資料表

二進位資料表會保存點陣圖、動畫和圖示等專案的二進位資料。 二進位資料表也用來儲存自訂動作的資料。 請參閱 [OLE 對資料流程的限制](ole-limitations-on-streams.md)。

二進位資料表具有下列資料行。



| Column | 類型                         | 答案 | Nullable |
|--------|------------------------------|-----|----------|
| 名稱   | [識別碼](identifier.md) | Y   | N        |
| 資料   | [二進位](binary.md)         | N   | N        |



 

## <a name="columns"></a>資料行

<dl> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>名字
</dt> <dd>

識別特定二進位資料的唯一索引鍵。 如果二進位資料是針對控制項，則索引鍵會出現在 [控制項資料表](control-table.md)中相關聯控制項的文字資料行中。 此索引鍵在所有需要二進位資料的控制項中必須是唯一的。

</dd> <dt>

<span id="Data"></span><span id="data"></span><span id="DATA"></span>資料
</dt> <dd>

未格式化的二進位資料。

</dd> </dl>

## <a name="validation"></a>驗證

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE17](ice17.md)  
[ICE29](ice29.md)  
</dl>

 

 



