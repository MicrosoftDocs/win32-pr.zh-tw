---
title: 架構支援層級
description: 本節涵蓋有關架構支援層級的詳細資料。
ms.assetid: ca18306e-6d67-406d-9c42-4be159a0b81f
keywords:
- Windows 的架構支援層級 Web 服務
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d6cae112e074d50b90425c1d8952f3b6c06463378d73767346742193b406d2b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119026278"
---
# <a name="schema-support-level"></a>架構支援層級

本節涵蓋有關架構支援層級的詳細資料。


架構直接支援下列各項：

-   元素的序列。
-   元素類型的衍生。
-   專案的簡單選擇 (對應至加上標籤聯集) 的專案。
-   XSD/.NET 二進位格式所定義的基本類型，包括範圍 (min/max) 。
-   對任何專案的簡單支援 (專案) 的類型沒有任何限制。
-   具有預設值的選擇性元素和屬性。
-   範圍 (min/max) 的重複元素。
-   Nillable 元素。

架構不支援下列直接 (表示「回溯」行為) ：

-   使用者定義的基本類型。
-   更複雜的選項。
-   拒絕未知的屬性。
-   來回往返未知的屬性。
-   對任何專案更複雜的支援。
-   All 結構。
-   Key/keyref。

以下是不同架構元件支援的詳細細目。 它會與 WCF 中的資料合約比較，因為功能中的相似性。 將會說明差異。

通常，針對回溯行為：

-   屬性會被備份到 WS \_ 字串;
-   元素內容會被支援至 WS \_ XML \_ 緩衝區。
-   complexType 的支援是包含 WS XML 緩衝區欄位的結構 \_ \_ 。
-   簡單類型會支援到 WS \_ 字串。

wsutil 會針對目前未完全支援的架構元件產生警告。 應用程式可能需要針對這些元件進行額外的驗證。 您可以改進加班 wsutil 來處理執行時間目前支援的一些功能，例如預設值支援。 wsutil 也可與序列化一起改善，以支援其他功能，例如抽象。 不支援的架構元件數目可在一段時間後減少。

## <a name="the-overall-schema-document"></a>整體架構檔

全域定義，可能會影響架構中的內嵌定義。 這些是全域屬性，適用于架構中的所有定義。

<xs： schema> 屬性

-   已忽略 attributeFromDefault。
-   已忽略 blockDefault。
-   已忽略 elementFormDefault。 這與 dataContract 不同，因為執行時間支援不合格的元素。
-   已忽略 finalDefault。 最終的概念不支援 C 語言。
-   已忽略識別碼。
-   targetNamespace 支援並對應至服務命名空間。
-   已忽略版本。

<xs： schema> 內容

-   包含支援的;wsutil 需要在編譯期間將所有必要的定義當作輸入檔來使用。
-   已忽略重新定義。 wsutil 不支援此功能。
-   支援匯入;wsutil 需要在編譯期間將所有必要的定義當作輸入檔來使用。
-   支援 simpleType-請參閱下方的簡單類型區段。
-   支援 complexType-請參閱 ' complexType ' 區段
-   已忽略群組。
-   已忽略 attributeGroup。
-   支援的元素;對應至全域元素定義。
-   支援的屬性;對應到全域屬性定義。
-   已忽略標記法

## <a name="complex-type"></a>複雜類型

以 <xs： complexType> 表示的複雜類型可能會限制簡單類型或複雜類型、簡單類型、陣列或結構的副檔名。 請注意，在簡單類型的延伸中，沒有任何繼承和 xsi： type 支援。

<xs： complexType> 屬性

-   abstract 會產生有關不支援功能的警告，而不會變更程式碼產生。
-   封鎖會產生有關不支援功能的警告，而不會變更程式碼產生。
-   最後會產生關於不支援功能的警告，而不會變更程式碼產生。
-   已忽略識別碼。
-   mixed 會產生關於不支援功能的警告， \_ 如果為 true，則會使用 WS XML 緩衝區來切換至結構 \_ 。
-   名稱支援且對應至結構類型名稱。

<xs： complexType> 內容

這是結構的型別定義。 不支援 complexContent 限制。

-   complexContent 支援複雜內容延伸模組。 地圖結構繼承。
-   群組目前已與 WS \_ XML 緩衝區欄位回溯至結構 \_ 。 可以根據下一個物件來支援。
-   選擇支援做為聯集。 資料合約中不支援這項功能。
-   支援的序列-對應至結構的欄位
-   支援屬性，但有一個例外狀況「禁止」。 如果「禁止」，則會使用 WS XML 緩衝區來切換至結構 \_ \_ 。
-   attributeGroup 支援-對應至屬性的順序
-   已忽略 anyAttribute
-   AttributeGroupRef 支援-對應至屬性的順序。
-   GroupRef 目前已使用 WS \_ XML 緩衝區欄位回溯至結構 \_ 。 可以根據下一個群組來支援。
-   任何支援的，對應至 XML \_ 緩衝區
-    (空白) 支援的對應至空白結構描述，但未產生任何結構。

複雜型別中的 <xs:sequence>：內容

wsutil 僅支援 minOccurs = 1 和 maxOccurs = 1 的完整支援順序;否則，複雜型別目前會支援到 WS \_ XML \_ 緩衝區。 它可支援為結構的陣列。

-   支援的元素;每個實例都會對應至結構中的欄位。
-   群組退回;complexType 會回到 WS \_ XML \_ 緩衝區。
-   所有回復;complexType 會回到 WS \_ XML \_ 緩衝區。
-   支援的選擇;對應至聯集欄位。
-   順序回復;complexType 會回到 WS \_ XML \_ 緩衝區。
-   任何支援的;對應至 XML \_ 緩衝區。
-    (空白) 支援;如果沒有任何屬性，則 complexType 可以是空的結構。

## <a name="elements"></a>元素

<xs： element>可能發生在三個內容中。

-   它可能會出現在 <xs： sequence> 中，描述一般結構的欄位。 在此情況下，maxOccurs 屬性必須是1。 如果 minOccurs 為0，則此欄位是選擇性的。
-   它可能會出現在 <xs： sequence> 中，描述陣列的欄位。 在此情況下，maxOccurs 屬性必須大於1或「未系結」。
-   它可能會在 <xs： schema> 內，做為全域專案描述。

<xs： element> 在 <xs： sequence> 或 <xs： choice> 作為結構中的欄位

-   支援 ref;解析為全域元素的參考。
-   名稱支援，對應至功能變數名稱。
-   支援的類型，對應至欄位類型。 如需詳細資訊，請參閱「類型對應」。 如果未指定 (且元素未包含匿名型別) ，則會假設為 xs： anyType。
-   封鎖會產生有關不支援功能的警告，而不會變更程式碼產生。
-   預設會產生關於不支援功能的警告，而不會變更程式碼產生。
-   已修正產生不支援功能的警告，而不會變更程式碼產生。
-   忽略的表單。 我們的序列化層同時支援合格和不合格的表單。
-   已忽略識別碼。
-   如果等於1，則 maxOccurs 對應至單一資料欄位。 如果 maxOccurs 大於1，它會對應至陣列欄位， (重複元素) 。
-   如果為0，則欄位選項設定為 [欄位 \_ 選擇性] （如果未設定 nillable）。
-   nillable 欄位是 nillable。 如需詳細資訊，請參閱 [序列化](serialization.md) 。

<xs： element> 為 global element： attributes

minOccurs 和 maxOccurs 屬性是不正確全域元素描述。 應用程式可以直接在序列化層或通道層級中使用產生的元素描述。

-   abstract 會產生有關不支援功能的警告，而不會變更程式碼產生。
-   封鎖會產生有關不支援功能的警告，而不會變更程式碼產生。
-   預設會產生關於不支援功能的警告，而不會變更程式碼產生。
-   最後會產生關於不支援功能的警告，而不會變更程式碼產生。
-   已修正產生不支援功能的警告，而不會變更程式碼產生。
-   已忽略識別碼。
-   支援的名稱-對應至全域元素描述的名稱，而這是指定時匿名型別的基底。
-   nillable 已忽略-應用程式需要以 right 旗標呼叫。
-   如果已設定，substitutionGroup 會使用 WS XML 緩衝區回復為結構 \_ \_ 。 wsutil 不支援 substitutionGroup。
-   輸入支援的類型，並將其對應至元素的類型。

<xs： element> 為 global element：內容

-   支援 simpleType;對應至類型定義。
-   支援 complexType;對應至複雜型別。
-   unique 會產生關於不支援功能的警告，而不會變更程式碼產生。 wsutil 不支援元素條件約束。
-   金鑰會產生關於不支援功能的警告，而不會變更程式碼產生。 wsutil 不支援元素條件約束。
-   keyref 會產生有關不支援功能的警告，而不會變更程式碼產生。 wsutil 不支援元素條件約束。
-    (空白) 支援;沒有類型規格的元素會被視為 xs： anyType。

## <a name="simple-types"></a>簡單型別

<xs： simpleType> 屬性

-   最後會產生關於不支援功能的警告，而不會變更程式碼產生。
-   已忽略識別碼
-   名稱支援，對應至類型名稱。

<xs： simpleType> 內容

-   支援的限制，對應至列舉類型或範圍。 請參閱「xs： simpleType 限制」一節。
-   清單會產生有關不支援功能的警告，並回到 XML \_ 緩衝區。
-   Union 會產生有關不支援之功能的警告，並回到 XML \_ 緩衝區。

## <a name="simple-type-restriction"></a>簡單類型限制

整數類型和字串類型允許某些 facet，以允許範圍和列舉支援。

列舉支援

<xs：列舉> 字串基底類型的簡單類型限制會視為列舉類型。 在此情況下，基底屬性必須是字串類型。 在列舉案例中，會忽略所有其他 facet。

簡單類型支援的範圍

某些 facet 支援簡單類型，可有效地支援類型上允許的範圍。 以下是整數類型和 float/double 類型的限制。 具有其他 facet 的簡單類型會支援至 WS \_ 字串類型

-   支援的 minExclusive
-   支援 minInclusive
-   支援 maxExclusive
-   支援 maxInclusive
-   totalDigits 會產生關於不支援功能的警告，而不會變更程式碼產生。
-   fractionDigits 會產生關於不支援功能的警告，而不會變更程式碼產生。
-   長度會產生有關不支援功能的警告，而不會變更程式碼產生。
-   minLength 會產生有關不支援功能的警告，而不會變更程式碼產生。
-   maxLength 會產生有關不支援功能的警告，而不會變更程式碼產生。
-   列舉會產生有關不支援功能的警告，而不會變更程式碼產生。
-   空白字元會產生關於不支援功能的警告，而不會變更程式碼產生。
-   模式會產生有關不支援功能的警告，而不會變更程式碼產生。
-    (空白) 支援。

目前不支援字串上的 minLength 和 maxLength，但這是要支援的必要功能。

## <a name="inheritance"></a>繼承

Wsutil 支援繼承複雜類型，也就是說，結構可以繼承自另一個結構，類似于 c + + 中的介面繼承。 這是透過 <xs： complexContentExtension> 來完成。 支援 <xs： simpleContentExtension>，但會以基底類型為第一個欄位而非類型繼承的一般結構來產生。

## <a name="typeprimitive-mapping"></a>型別/基本對應

從 XML 中的 Ncname 轉譯時，必須將識別碼正規化。 字串為 nillable;指標類型為 nillable;整數類資料類型和 float/double 是 nillable，而 defaultValue 則設定為0。

![顯示 XSD 類型與 Sapphire 資料類型之間對應的資料表。](images/schematypemap.png)

 

 




