---
description: 條件式存取控制專案 (ACE) 可讓您在執行存取檢查時評估存取條件。 安全描述項定義語言 (SDDL) 提供以字串格式定義條件式 Ace 的語法。
ms.assetid: cdc3629d-c4d8-4910-8838-3bdb601f7064
title: 條件式 Ace 的安全描述項定義語言
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee0a746460c7582d95e0c95e2a2c179aac2eb29456418234cb52e842c8c56738
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117780523"
---
# <a name="security-descriptor-definition-language-for-conditional-aces"></a>條件式 Ace 的安全描述項定義語言

條件式 [*存取控制專案*](/windows/desktop/SecGloss/a-gly) (ACE) 可讓您在執行存取檢查時評估存取條件。 安全描述項定義語言 (SDDL) 提供以字串格式定義條件式 Ace 的語法。

條件式 ACE 的 SDDL 與任何 ACE 的 SDDL 相同，並將條件陳述式的語法附加到 ACE 字串的結尾。 如需 SDDL 的詳細資訊，請參閱 [安全描述項定義語言](security-descriptor-definition-language.md)。

\#在資源屬性中，"" 符號與 "0" 同義。 例如，D:AI (XA; OICI; FA;;;WD; (OctetStringType = = \# 1 \# 2 \# 3 \# \#) ) 相當於並解釋為 D:AI (XA; OICI; FA;;;WD; (OctetStringType = = \# 01020300) ) 。

-   [條件式 ACE 字串格式](#conditional-ace-string-format)
-   [條件運算式](#conditional-expressions)
-   [屬性](#attributes)
-   [運算子](#operators)
-   [運算子優先順序](#operator-precedence)
-   [未知的值](#unknown-values)
-   [條件式 ACE 評估](#conditional-ace-evaluation)
-   [範例](#examples)
-   [相關主題](#related-topics)

## <a name="conditional-ace-string-format"></a>條件式 ACE 字串格式

[*安全描述項*](/windows/desktop/SecGloss/s-gly)字串中的每個 ACE 都會以括弧括住。 ACE 的欄位會以下列順序排列，並以分號分隔 (; ) 。

*AceType ***;**_AceFlags_*_;_*_許可權_*_;_*_ObjectGuid_*_;_*_InheritObjectGuid_*_;_*_AccountSid_*_; (_ *_ConditionalExpression_* _)_*

這些欄位如 [ACE 字串](ace-strings.md)所述，但有下列例外狀況。

-   *AceType* 欄位可以是下列其中一個字串。

    | ACE 類型字串 | Sddl 中的常數                         | AceType 值                                   |
    |-----------------|--------------------------------------------|-------------------------------------------------|
    | XA<br/> | \_允許 SDDL 回呼 \_ 存取 \_<br/> | 存取 \_ 允許的 \_ 回呼 \_ ACE \_ 類型<br/> |
    | XD<br/> | SDDL \_ 回呼 \_ \_ 拒絕存取<br/>  | \_拒絕存取 \_ 回呼 \_ ACE \_ 類型<br/>  |

    

     

-   ACE 字串包含一或多個條件運算式，並在字串結尾以括弧括住。

## <a name="conditional-expressions"></a>條件運算式

條件運算式可以包含下列任何元素。



| 運算式元素                                                | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *AttributeName*<br/>                                        | 測試指定的屬性是否有非零值。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| **存在** *AttributeName*<br/>                             | 測試指定的屬性是否存在於用戶端內容中。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| *AttributeName* *運算子**值*<br/>                     | 傳回指定之作業的結果。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| * ConditionalExpression * **\|\|** _ConditionalExpression_<br/> | 測試其中一個指定的條件運算式是否為 true。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| *ConditionalExpression* **&&***ConditionalExpression*<br/> | 測試兩個指定的條件運算式是否為 true。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| **！ (** _ConditionalExpression_ *_)_*<br/>                     | 條件運算式的反向。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| {_SidArray_*_}_* **\_ 的成員**<br/>                         | 測試用戶端內容的 [**SID \_ 和 \_ 屬性**](/windows/desktop/api/Winnt/ns-winnt-sid_and_attributes)陣列是否包含 (sid) 在 *SidArray* 所指定的逗點分隔清單中的所有 [安全識別碼](security-identifiers.md)。<br/> 若為允許 ace，用戶端內容 SID 必須將 **\_ \_ 已啟用 SE 群組** 的屬性設定為視為相符。<br/> 若為 deny ace，用戶端內容 SID 必須 **\_ \_ 啟用 SE 群組**，否則 SE 群組會將 [僅限拒絕屬性] 設定為 [ **\_ \_ \_ \_ \_ 僅限拒絕**] 屬性設定為 [符合]。<br/> *SidArray* 陣列可以包含 sid 字串 (例如 "S-1-5-6" ) 或 sid 別名 (例如 "BA"<br/> |



 

## <a name="attributes"></a>屬性

屬性代表用戶端內容中 [**AUTHZ \_ 安全性 \_ 屬性 \_ 資訊**](/windows/desktop/api/Authz/ns-authz-authz_security_attributes_information) 陣列內的元素。 屬性名稱可包含任何英數位元和任何字元 "："、"/"、"." 和 " \_ "。

屬性值可以是下列任何一種類型。



| 值類型         | 描述                                                                                                                                                                                         |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 整數<br/> | 十進位或十六進位標記法中的64位整數。<br/>                                                                                                                              |
| String<br/>  | 以引號分隔的字串值。<br/>                                                                                                                                                      |
| SID<br/>     | SID (S-1-1-0) 或 SID (BA) 。 必須位於的成員 \_ 或裝置成員的 RHS 上 \_ \_ 。<br/>                                                                                                           |
| BLOB<br/>    | \# 後面接著十六進位數位。 如果數位的長度為奇數，則 \# 會轉譯為0以使其成為偶數。 此外 \# ，出現在值的其他位置時，會轉譯為0。<br/> |



 

## <a name="operators"></a>運算子

下列運算子已定義為在條件運算式中用來測試屬性的值。 這些都是二元運算子，並以 *AttributeName* *運算子**值* 形式使用。



| 運算子            | 描述                                                                                                              |
|---------------------|--------------------------------------------------------------------------------------------------------------------------|
| ==<br/>       | 傳統定義。<br/>                                                                                      |
| !=<br/>       | 傳統定義。<br/>                                                                                      |
| <<br/>     | 傳統定義。<br/>                                                                                      |
| <=<br/>    | 傳統定義。<br/>                                                                                      |
| ><br/>     | 傳統定義。<br/>                                                                                      |
| >=<br/>    | 傳統定義。<br/>                                                                                      |
| 包含<br/> | 如果指定屬性的值是指定值的超集合，則為 **TRUE** ;否則 **為 FALSE**。<br/>  |
| 任何 \_<br/>  | 如果指定的值為指定屬性值的超集合，則為 **TRUE** ;否則 **為 FALSE**。 <br/> |



 

此外，一元運算子存在、成員 \_ 和否定 (！ ) 的定義方式如條件運算式資料表中所述。

"Contains" 運算子前面必須加上空白字元，且 "Any of \_ " 運算子之前必須加上空白字元。

## <a name="operator-precedence"></a>運算子優先順序

系統會依照下列優先順序來評估運算子，而且會從左至右評估相等優先順序的作業。

1.  存在 \_ ，成員隸屬于
2.  Contains \_ 、任何
3.  = =、！ =、<、<=、>、>=
4.  !
5.  &&
6.  \|\|

此外，條件運算式的任何部分都可以用括弧括住。 括弧內的運算式會先評估。

## <a name="unknown-values"></a>未知的值

條件運算式的結果有時會傳回 **未知** 的值。 例如，當指定的屬性不存在時，任何關聯式作業都會傳回 **Unknown** 。

下表描述兩個條件運算式（ *ConditionalExpression1* 和 *ConditionalExpression2*）之間邏輯 **AND** 運算的結果。



| *ConditionalExpression1* | *ConditionalExpression2* | *ConditionalExpression1* **&&***ConditionalExpression2* |
|--------------------------|--------------------------|----------------------------------------------------------|
| **TRUE**<br/>      | **TRUE**<br/>      | **TRUE**<br/>                                      |
| **TRUE**<br/>      | **FALSE**<br/>     | **FALSE**<br/>                                     |
| **TRUE**<br/>      | **UNKNOWN**<br/>   | **UNKNOWN**<br/>                                   |
| **FALSE**<br/>     | **TRUE**<br/>      | **FALSE**<br/>                                     |
| **FALSE**<br/>     | **FALSE**<br/>     | **FALSE**<br/>                                     |
| **FALSE**<br/>     | **UNKNOWN**<br/>   | **FALSE**<br/>                                     |
| **UNKNOWN**<br/>   | **TRUE**<br/>      | **UNKNOWN**<br/>                                   |
| **UNKNOWN**<br/>   | **FALSE**<br/>     | **FALSE**<br/>                                     |
| **UNKNOWN**<br/>   | **UNKNOWN**<br/>   | **UNKNOWN**<br/>                                   |



 

下表描述兩個條件運算式（ *ConditionalExpression1* 和 *ConditionalExpression2*）之間的邏輯 **OR** 運算結果。



| *ConditionalExpression1* | *ConditionalExpression2* | *ConditionalExpression1* **\|\|** *ConditionalExpression2* |
|--------------------------|--------------------------|------------------------------------------------------------|
| **TRUE**<br/>      | **TRUE**<br/>      | **TRUE**<br/>                                        |
| **TRUE**<br/>      | **FALSE**<br/>     | **TRUE**<br/>                                        |
| **TRUE**<br/>      | **UNKNOWN**<br/>   | **TRUE**<br/>                                        |
| **FALSE**<br/>     | **TRUE**<br/>      | **TRUE**<br/>                                        |
| **FALSE**<br/>     | **FALSE**<br/>     | **FALSE**<br/>                                       |
| **FALSE**<br/>     | **UNKNOWN**<br/>   | **UNKNOWN**<br/>                                     |
| **UNKNOWN**<br/>   | **TRUE**<br/>      | **TRUE**<br/>                                        |
| **UNKNOWN**<br/>   | **FALSE**<br/>     | **UNKNOWN**<br/>                                     |
| **UNKNOWN**<br/>   | **UNKNOWN**<br/>   | **UNKNOWN**<br/>                                     |



 

具有 **未知** 值的條件運算式的否定也是 **未知** 的。

## <a name="conditional-ace-evaluation"></a>條件式 ACE 評估

下表描述條件式 ACE 的存取檢查結果，取決於條件運算式的最後評估。

| ACE 類型         | true             | FALSE                 | UNKNOWN               |
|------------------|------------------|-----------------------|-----------------------|
| Allow<br/> | Allow<br/> | 忽略 ACE<br/> | 忽略 ACE<br/> |
| 拒絕<br/>  | 拒絕<br/>  | 忽略 ACE<br/> | 拒絕<br/>       |



 

## <a name="examples"></a>範例

下列範例顯示如何使用 SDDL 定義的條件 ACE 來表示指定的存取原則。

<dl> <dt>

<span id="Policy"></span><span id="policy"></span><span id="POLICY"></span>政策
</dt> <dd>

如果符合下列兩個條件，允許執行至所有人：

-   標題 = PM
-   部門 = 財務或部門 = 銷售

</dd> <dt>

<span id="SDDL"></span><span id="sddl"></span>SDDL
</dt> <dd>

D： (XA;;FX;;;S-1-1-0; (@User.Title = = "PM"  &&  (@User.Division = = "財務" \| \| @User.Division = = "Sales" ) ) ) 

</dd> <dt>

 
</dt> <dd>

 

</dd> <dt>

<span id="Policy"></span><span id="policy"></span><span id="POLICY"></span>政策
</dt> <dd>

如果任何使用者專案與檔案的專案相交，則允許執行。

</dd> <dt>

<span id="SDDL"></span><span id="sddl"></span>SDDL
</dt> <dd>

D： (XA;;FX;;;S-1-1-0; (@User.Project 任何 \_ @Resource.Project) ) 

</dd> <dt>

 
</dt> <dd>

 

</dd> <dt>

<span id="Policy"></span><span id="policy"></span><span id="POLICY"></span>政策
</dt> <dd>

如果使用者使用智慧卡登入、是備份操作員，並且從已啟用 Bitlocker 的電腦進行連線，則允許讀取存取。

</dd> <dt>

<span id="SDDL"></span><span id="sddl"></span>SDDL
</dt> <dd>

D： (XA;; FR;;;S-1-1-0; (成員 \_ {SID (智慧卡 \_ SID) ，SID (BO) }  && @Device.Bitlocker) ) 

</dd> <dt>

 
</dt> <dd>

 

</dd> </dl>

## <a name="related-topics"></a>相關主題

<dl> <dt>

[\[DTYP \] ：安全描述項描述語言](/openspecs/windows_protocols/ms-dtyp/4f4251cc-23b6-44b6-93ba-69688422cb06)
</dt> </dl>

