---
title: RESOURCEHEADER 結構
description: 包含資源標頭本身的相關資訊，以及此資源特定的資料。
ms.assetid: e0eba7b3-a275-4ffe-9347-46361213cf48
keywords:
- RESOURCEHEADER 結構功能表和其他資源
topic_type:
- apiref
api_name:
- RESOURCEHEADER
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 41b436ebd6aeb5dc31f8ed773fbe7b12a1586185
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965887"
---
# <a name="resourceheader-structure"></a>RESOURCEHEADER 結構

包含資源標頭本身的相關資訊，以及此資源特定的資料。 此結構不是真正的 C 語言結構，因為它包含可變長度的成員。 此處提供的結構定義僅供說明之用;它不會出現在任何標準標頭檔中。

## <a name="syntax"></a>語法


```C++
typedef struct {
  DWORD DataSize;
  DWORD HeaderSize;
  DWORD TYPE;
  DWORD NAME;
  DWORD DataVersion;
  WORD  MemoryFlags;
  WORD  LanguageId;
  DWORD Version;
  DWORD Characteristics;
} RESOURCEHEADER;
```



## <a name="members"></a>成員

<dl> <dt>

**DataSize**
</dt> <dd>

類型： **DWORD**

</dd> <dd>

在此特定資源的資源標頭之後，資料的大小（以位元組為單位）。 它不會在資源檔中包含此資源和其後任何資源之間的任何檔案填補。

</dd> <dt>

**HeaderSize**
</dt> <dd>

類型： **DWORD**

</dd> <dd>

接下來資源標頭資料的大小（以位元組為單位）。

</dd> <dt>

**TYPE**
</dt> <dd>

類型： **DWORD**

</dd> <dd>

資源類型。 **型** 別成員可以是數值，也可以是以 null 結束的 Unicode 字串來指定類型的名稱。 如需 **名稱** 或 **序數** 類型成員的描述，請參閱下列備註一節。

如果 **類型** 成員是數值，則可以指定標準或使用者定義的資源類型。 如果成員是字串，則它是使用者定義的資源類型。 如需預先定義的資源類型清單，請參閱 [資源類型](/windows/desktop/menurc/resource-types)。

小於256的值會保留供系統使用。

</dd> <dt>

**名稱**
</dt> <dd>

類型： **DWORD**

</dd> <dd>

識別特定資源的名稱。 **名稱** 成員就像 **類型** 成員一樣，可以是數值或以 null 終止的 Unicode 字串。 如需 **名稱** 或 **序數** 類型成員的描述，請參閱下列備註一節。

您不需要在 **類型** 和 **名稱** 成員之間新增 **DWORD** 對齊的填補，因為它們包含 **文字** 資料。 不過，您可能需要在 **名稱** 成員後面加上邊框間距，以對齊 **DWORD** 界限上的其餘標頭。

</dd> <dt>

**DataVersion**
</dt> <dd>

類型： **DWORD**

</dd> <dd>

預先定義的資源資料版本。 這會決定應用程式應使用哪個版本的資源資料。

</dd> <dt>

**MemoryFlags**
</dt> <dd>

類型： **WORD**

</dd> <dd>

一組可描述資源狀態的屬性旗標。 中的修飾詞。RC 腳本檔會將這些屬性指派給資源。 腳本識別碼可以指派下列旗標值。

應用程式不會使用這些屬性。 腳本中允許使用屬性來與現有腳本回溯相容，但是會忽略這些屬性。 載入對應模組時，會載入資源，並在卸載模組時釋放資源。

<dt>

<span id="MOVEABLE"></span><span id="moveable"></span>

**可移動** 的 (0x0010) 


</dt> <dd></dd> <dt>

<span id="FIXED"></span><span id="fixed"></span>

已 **修正** (~ 可移動) 


</dt> <dd></dd> <dt>

<span id="PURE"></span><span id="pure"></span>

**純** (0x0020) 


</dt> <dd></dd> <dt>

<span id="IMPURE"></span><span id="impure"></span>

**IMPURE** (~ 純) 


</dt> <dd></dd> <dt>

<span id="PRELOAD"></span><span id="preload"></span>

**預先載入** (0x0040) 


</dt> <dd></dd> <dt>

<span id="LOADONCALL"></span><span id="loadoncall"></span>

**LOADONCALL** (~ 預先載入) 


</dt> <dd></dd> <dt>

<span id="DISCARDABLE"></span><span id="discardable"></span>

**DISCARDABLE** (0x1000) 


</dt> <dd></dd> </dl> </dd> <dt>

**LanguageId**
</dt> <dd>

類型： **WORD**

</dd> <dd>

資源或資源集的語言。 使用選擇性 [語言](./language-statement.md) 資源定義語句來設定這個成員的值。 這些參數是來自 Winnt .h 檔案的常數。

每個資源都包含一個語言識別項，讓系統或應用程式可以選取適用于系統目前地區設定的語言。 如果有多個相同類型和名稱的資源與資源內的字串語言不同，您就必須為每個資源指定 **LanguageId** 。

</dd> <dt>

**版本**
</dt> <dd>

類型： **DWORD**

</dd> <dd>

工具可用來讀取和寫入資源檔的資源資料的使用者定義版本號碼。 使用選擇性的 [版本](./version-statement.md) 資源定義語句來設定此值。

</dd> <dt>

**特性**
</dt> <dd>

類型： **DWORD**

</dd> <dd>

指定有關工具可用來讀取和寫入資源檔之資源的使用者定義資訊。 使用選擇性的 [ [特性](./characteristics-statement.md) ] 資源定義語句來設定此值。

</dd> </dl>

## <a name="remarks"></a>備註

變數型別成員稱為「 **名稱** 」或「 **序數** 」成員，它會在資源檔中出現識別碼的大部分位置使用。 **Name** 或 **序數** 類型成員的第一個 **單字** 指出成員是數值或字串。 如果成員中的第一個 **單字** 等於值0xffff （這是不正確 Unicode 字元），則下列 **單字** 是類型號碼。 否則，成員會包含 Unicode 字串，而成員中的第一個 **單字** 是名稱字串中的第一個字元。 如需資源定義語句的詳細資訊，請參閱 [資源定義語句](./resource-definition-statements.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/> |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>       |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**概念**
</dt> <dt>

[資源](resources.md)
</dt> <dt>

**其他資源**
</dt> <dt>

[特性語句](./characteristics-statement.md)
</dt> <dt>

[LANGUAGE 語句](./language-statement.md)
</dt> <dt>

[VERSION 語句](./version-statement.md)
</dt> </dl>

 

