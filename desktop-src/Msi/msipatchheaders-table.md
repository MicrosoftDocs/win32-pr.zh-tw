---
description: MsiPatchHeaders 資料表會保存用於修補程式驗證的二進位修補標頭資料流程。
ms.assetid: aefdd365-1681-43e4-8470-04a5d6efd993
title: MsiPatchHeaders 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a3fa4e037a31f3e913f13ff9c96735ed6760dc4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193103"
---
# <a name="msipatchheaders-table"></a>MsiPatchHeaders 資料表

MsiPatchHeaders 資料表會保存用於修補程式驗證的二進位修補標頭資料流程。

當長檔案 [資料表](file-table.md) 索引鍵導致無法在 [patch 資料表](patch-table.md)中產生 patch 標頭資料流程時，就會使用 MsiPatchHeaders 資料表。 這可能是因為資料流程的 [OLE 限制](ole-limitations-on-streams.md)中所述的資料流程名稱限制所致。 在此情況下，Patch 資料表可以參考 MsiPatchHeaders 資料表，以建立 Patch 標頭資料流程。

MsiPatchHeaders 資料表具有下列資料行。



| Column    | 類型                         | 答案 | Nullable |
|-----------|------------------------------|-----|----------|
| StreamRef | [識別碼](identifier.md) | Y   | N        |
| 標頭    | [二進位](binary.md)         | N   | N        |



 

## <a name="columns"></a>資料行

<dl> <dt>

<span id="StreamRef"></span><span id="streamref"></span><span id="STREAMREF"></span>StreamRef
</dt> <dd>

可唯一識別特定 patch 標頭之資料表的主要索引鍵。

</dd> <dt>

<span id="Header"></span><span id="header"></span><span id="HEADER"></span>頭
</dt> <dd>

此資料行是用於修補驗證的二進位資料流程修補程式標頭。

</dd> </dl>

## <a name="remarks"></a>備註

此資料表是由 [PatchFiles 動作](patchfiles-action.md)處理。 此資料表通常會透過修補套件的轉換新增至安裝套件。 它通常不會直接撰寫到安裝套件中。

## <a name="validation"></a>驗證

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE29](ice29.md)  
</dl>

 

 



