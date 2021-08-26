---
description: ProgId 資料表包含程式識別碼和版本獨立程式識別碼的相關資訊，這些程式識別碼必須在產品公告中產生。
ms.assetid: 66a7e170-6f70-4db7-98f4-8a074471b9f2
title: ProgId 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbed8baea9bd8421757cf2e31f0ba06679db3394c95f732537a7e230c02b5ee8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120042058"
---
# <a name="progid-table"></a>ProgId 資料表

ProgId 資料表包含程式識別碼和版本獨立程式識別碼的相關資訊，這些程式識別碼必須在產品公告中產生。

ProgId 資料表具有下列資料行。



| Column         | 類型                         | 答案 | Nullable |
|----------------|------------------------------|-----|----------|
| ProgId         | [Text](text.md)             | Y   | N        |
| ProgId \_ 父系 | [Text](text.md)             | N   | Y        |
| 類別\_        | [GUID](guid.md)             | N   | Y        |
| 描述    | [Text](text.md)             | N   | Y        |
| 圖示\_         | [識別碼](identifier.md) | N   | Y        |
| >iconindex      | [整數](integer.md)       | N   | Y        |



 

## <a name="columns"></a>資料行

<dl> <dt>

<span id="ProgId"></span><span id="progid"></span><span id="PROGID"></span>ProgId
</dt> <dd>

程式識別碼或版本獨立的程式識別碼。 如果此資料表的類別資料行中所列的 CLSID \_ 已排程要進行公告或安裝，則會註冊 ProgId 資料表中所列的 progid。 選取 ProgId 以進行註冊時，也會選取透過 ProgId 父資料行參考此資料 \_ 列的所有 progid 進行註冊。

</dd> <dt>

<span id="ProgId_Parent"></span><span id="progid_parent"></span><span id="PROGID_PARENT"></span>ProgId \_ 父系
</dt> <dd>

只定義為版本獨立的程式識別碼。 此欄位是 ProgId 資料行中的外鍵。 若要定義版本獨立程式識別碼，請在 ProgId 父資料行中輸入對應的 ProgId \_ 。 選取 ProgId 以進行安裝時，也會選取透過 ProgId 父資料行相關聯的對應與版本無關的 Progid \_ 來進行註冊。

</dd> <dt>

<span id="Class_"></span><span id="class_"></span><span id="CLASS_"></span>類\_
</dt> <dd>

[類別資料表](class-table.md)中的選擇性外鍵。 針對版本獨立的 ProgId，此資料行必須是 Null。 如果 ProgId 的類別值為 null，則會在延伸模組資料表中的資料 \_ 列的 progid 資料行中出現 progid 時[](extension-table.md)註冊，而且此延伸模組在[動詞資料表](verb-table.md)中至少有一個與其相關聯的動詞。 以這種方式選取以進行註冊的 Progid，不會安裝透過 ProgId 預設值參考目前 ProgId 的其他 Progid \_ 。

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>描述
</dt> <dd>

相關聯程式識別碼的選擇性當地語系化描述。

</dd> <dt>

<span id="Icon_"></span><span id="icon_"></span><span id="ICON_"></span>圖示\_
</dt> <dd>

[圖示表格](icon-table.md)中的選擇性外鍵，可指定與這個 ProgId 相關聯的圖示檔。 這會寫入與此 ProgId 相關聯的 DefaultIcon 索引鍵下。 針對版本獨立的 ProgId，此資料行必須是 Null。

</dd> <dt>

<span id="IconIndex"></span><span id="iconindex"></span><span id="ICONINDEX"></span>>iconindex
</dt> <dd>

圖示檔中的圖示索引。 針對版本獨立的 ProgId，此資料行必須是 Null。

</dd> </dl>

## <a name="remarks"></a>備註

[*順序資料表*](s-gly.md)中的 [RegisterProgIdInfo](registerprogidinfo-action.md)和 [UnregisterProgIdInfo](unregisterprogidinfo-action.md)動作會處理此資料表中的資訊。 如需使用 *順序資料表* 的詳細資訊，請參閱 [使用順序資料表](using-a-sequence-table.md)。

## <a name="validation"></a>驗證

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE36](ice36.md)  
[ICE89](ice89.md)  
</dl>

 

 



