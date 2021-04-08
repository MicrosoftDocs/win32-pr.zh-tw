---
title: 選擇語法
description: 本主題包含定義新屬性時所要使用的建議語法清單。
ms.assetid: ed8a4164-5c82-43c2-8efb-a735c963a884
ms.tgt_platform: multiple
keywords:
- Active Directory，語法，已定義
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3379fa46d4e81cdeb31976abc0e32768b028a846
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "103681689"
---
# <a name="choosing-a-syntax"></a>選擇語法

Active Directory Domain Services 中定義了23個語法。 本主題包含定義新屬性時所要使用的建議語法清單。如需詳細資訊，請參閱 [Active Directory Domain Services 中的屬性語法](syntaxes-for-attributes-in-active-directory-domain-services.md)。

下表提供建議清單。



| 要儲存在屬性中的資料      | 使用的語法                                                      | 註解                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|---------------------------------|--------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 二進位資料                     | [**String(Octet)**](/windows/desktop/ADSchema/s-string-octet)                       | 用來儲存二進位資料。 這是位元組陣列。                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| 具有 DN 參考的二進位資料 | [**Object(DN-Binary)**](/windows/desktop/ADSchema/s-object-dn-binary)               | 包含二進位值，以及 (DN) 的分辨名稱。 Active Directory 伺服器會將 DN 保持在最新狀態。                                                                                                                                                                                                                                                                                                                                                                                                     |
| Boolean                         | [**布林**](/windows/desktop/ADSchema/s-boolean)                                  | 用於布林值。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| DN 參考                    | [**Object(DS-DN)**](/windows/desktop/ADSchema/s-object-ds-dn)                       | 用來儲存您想要由 Active Directory 伺服器保持最新狀態的辨別名稱。 當 DN 語法的屬性是以有效的 DN 建立時，伺服器會將屬性視為已設定之 DN 所代表之物件的參考。 如果參考的物件已重新命名或移動，伺服器就會確保屬性反映變更。 如果使用新的 DN 來重設屬性，則屬性會參考新 DN 所表示的物件。                                |
| 整數                         | [**整數**](/windows/desktop/ADSchema/s-integer)                                  | 用於整數。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| 大型整數 (64 位值)    | [**LargeInteger**](/windows/desktop/ADSchema/s-largeinteger)                        | 用於64位值。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| 連結的 DN                       | [**Object(DS-DN)**](/windows/desktop/ADSchema/s-object-ds-dn)                       | 此字串語法可用於連結的 DNs。 後置連結必須是語法 DN。 轉寄連結可以是語法 DN 以及 [**物件 (dn-字串)**](/windows/desktop/ADSchema/s-object-dn-string)、 [**物件 (dn 二進位)**](/windows/desktop/ADSchema/s-object-dn-binary)、 [**物件 (存取點)**](/windows/desktop/ADSchema/s-object-access-point)或 [**物件 (或-名稱)**](/windows/desktop/ADSchema/s-object-or-name)。 連結的屬性必須定義 **linkID** 。 請參閱 [**屬性架構**](/windows/desktop/ADSchema/c-attributeschema)屬性中的 **linkID** 描述。 |
| 安全性描述元             | [**String(NT-Sec-Desc)**](/windows/desktop/ADSchema/s-string-nt-sec-desc)           | 包含安全描述項的八位字串。                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|  (SID) 的安全識別碼       | [**(Sid) 的字串**](/windows/desktop/ADSchema/s-string-sid)                           | 包含安全識別碼 (SID) 的八位字串。 使用此語法只儲存 SID 值。                                                                                                                                                                                                                                                                                                                                                                                                                  |
| String                          | [**String(Unicode)**](/windows/desktop/ADSchema/s-string-unicode)                   | 用於大部分的字串屬性。 它支援 Unicode 字元集。 當 Active Directory 伺服器針對此語法的屬性執行比較時 (例如評估查詢) ，它會執行不區分大小寫的比較。 您可以使用其他字串語法 ([**字串 (IA5)**](/windows/desktop/ADSchema/s-string-ia5)、 [**字串 (數值)**](/windows/desktop/ADSchema/s-string-numeric)等，) 儲存只應包含語法所支援之特定字元集的字串。<br/>                          |
| 具有 DN 參考的字串資料 | [**Object(DN-String)**](/windows/desktop/ADSchema/s-object-dn-string)               | 包含字串值的字串，以及 (DN) 的分辨名稱。 Active Directory 伺服器會將 DN 保持在最新狀態。                                                                                                                                                                                                                                                                                                                                                                                            |
| Time                            | [**String(Generalized-Time)**](/windows/desktop/ADSchema/s-string-generalized-time) | 使用 [**字串 (通用時間)**](/windows/desktop/ADSchema/s-string-generalized-time) 語法來儲存時間值，而不是 [**字串 (utc 時間)**](/windows/desktop/ADSchema/s-string-utc-time) 語法，因為 **字串 (一般化時間)** 使用四個字元的年份和 **字串 (UTC 時間)** 只使用兩個字元。                                                                                                                                                                                                                 |



 

 

