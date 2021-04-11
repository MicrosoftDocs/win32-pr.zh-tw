---
description: PatchPackage 資料表會描述已套用至此產品的所有修補程式套件。 針對每個修補套件，會提供修補程式的唯一識別碼，以及修補程式所在之媒體映射的相關資訊。
ms.assetid: 212d99dd-c80c-42ca-9dfa-819ae1813006
title: PatchPackage 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b13bf9fc03012ca54a0b2144e97c828c968c68da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195266"
---
# <a name="patchpackage-table"></a>PatchPackage 資料表

PatchPackage 資料表會描述已套用至此產品的所有修補程式套件。 針對每個修補套件，會提供修補程式的唯一識別碼，以及修補程式所在之媒體映射的相關資訊。

PatchPackage 資料表具有下列資料行。



| Column  | 類型                   | 答案 | Nullable |
|---------|------------------------|-----|----------|
| PatchId | [GUID](guid.md)       | Y   | N        |
| 媒體\_ | [整數](integer.md) | N   | N        |



 

## <a name="columns"></a>資料行

<dl> <dt>

<span id="PatchId"></span><span id="patchid"></span><span id="PATCHID"></span>PatchId
</dt> <dd>

此資料行包含此特定修補程式的唯一識別碼。

</dd> <dt>

<span id="Media_"></span><span id="media_"></span><span id="MEDIA_"></span>媒體\_
</dt> <dd>

此資料行是 [媒體資料表](media-table.md) 中 DiskId 資料行的外鍵，表示包含修補程式套件的磁片。

</dd> </dl>

## <a name="remarks"></a>備註

每個修補封裝都需要 PatchPackage 資料表。 如果資料表遺失，嘗試安裝修補程式會失敗，並出現「錯誤2768： patch 封裝中的轉換無效」。 此資料表通常會透過修補套件的轉換新增至安裝套件。 它通常不會直接撰寫到安裝套件中。

## <a name="validation"></a>驗證

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
</dl>

 

 



