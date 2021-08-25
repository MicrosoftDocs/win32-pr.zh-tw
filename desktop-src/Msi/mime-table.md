---
description: MIME 資料表會建立 MIME 內容類型與副檔名或 CLSID 之間的關聯，以產生廣告 (多用途網際網路郵件延伸) 內容的通告所需的擴充功能或 COM 伺服器資訊。
ms.assetid: 5d452b24-ae04-4c45-8b3b-48e81f13a21e
title: MIME 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9e8a8f83499e286b63bf24dffa8858329231e74eec1f641588230da51578007
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119913368"
---
# <a name="mime-table"></a>MIME 資料表

MIME 資料表會建立 MIME 內容類型與副檔名或 CLSID 之間的關聯，以產生廣告 (多用途網際網路郵件延伸) 內容的通告所需的擴充功能或 COM 伺服器資訊。

MIME 資料表具有下列資料行。



| Column      | 類型             | 答案 | Nullable |
|-------------|------------------|-----|----------|
| ContentType | [Text](text.md) | Y   | N        |
| 延伸模組\_ | [Text](text.md) | N   | N        |
| CLSID       | [GUID](guid.md) | N   | Y        |



 

## <a name="columns"></a>資料行

<dl> <dt>

<span id="ContentType"></span><span id="contenttype"></span><span id="CONTENTTYPE"></span>ContentType
</dt> <dd>

此資料行是 MIME 內容的識別碼。 它通常是以型別/格式來撰寫。

</dd> <dt>

<span id="Extension_"></span><span id="extension_"></span><span id="EXTENSION_"></span>擴展\_
</dt> <dd>

此資料行包含要與 MIME 內容相關聯的伺服器延伸模組（不含點）。 此資料行是 [延伸模組資料表](extension-table.md)中的外鍵。 延伸模組資料表包含用來作為公告一部分的副檔名伺服器資訊。

</dd> <dt>

<span id="CLSID"></span><span id="clsid"></span>CLSID
</dt> <dd>

此資料行包含要與 MIME 內容相關聯的 COM 伺服器 CLSID。 此資料行中的 CLSID 可以是 [類別資料表](class-table.md) 中的外鍵，也可以是已存在於使用者電腦上的 clsid。 類別資料表包含 COM 伺服器的相關資訊，此資訊可作為公告的一部分。

</dd> </dl>

## <a name="remarks"></a>備註

當執行 [RegisterMIMEInfo 動作](registermimeinfo-action.md) 或 [UnregisterMIMEInfo 動作](unregistermimeinfo-action.md) 時，就會參考此資料表。 在 [公告] 模式中，[RegisterMIMEInfo] 動作會從已啟用對應功能的 MIME 資料表中，註冊伺服器的所有 MIME 資訊。 否則，此動作會從 MIME 資料表中，為目前選取要安裝對應功能的伺服器註冊 MIME 資訊。 [UnregisterMIMEInfo 動作](unregistermimeinfo-action.md)會從系統中取消註冊 MIME 相關的登錄資訊。 動作會從 MIME 資料表中取消註冊伺服器的 MIME 資訊，而這項功能目前已選取要卸載的對應功能。

## <a name="validation"></a>驗證

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE15](ice15.md)  
[ICE32](ice32.md)  
</dl>

 

 



