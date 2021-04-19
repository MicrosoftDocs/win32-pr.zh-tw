---
description: 定義 CAPICOM 屬性識別碼。
ms.assetid: faf10018-3ed8-4de6-9838-c553626f6dd7
title: 'CAPICOM_PROPID 列舉 (Capicom) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_PROPID
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: d817262b869ef694c2cf9ff5b1e577840c3168a4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990176"
---
# <a name="capicom_propid-enumeration"></a>CAPICOM \_ PROPID 列舉

**Capicom \_ PROPID** 列舉會定義 capicom 屬性識別碼。

## <a name="members"></a>成員



| member                                                 | 描述                                                                                                                                                                                                                                                                                | 值      |
|--------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------|
| **CAPICOM \_ PROPID \_ 不明**                           | 未知的屬性類型。<br/>                                                                                                                                                                                                                                          | 0          |
| **CAPICOM \_ PROPID \_ KEY \_ >PROV \_ 控制碼**                 | [*密碼編譯服務提供者*](../secgloss/c-gly.md)中金鑰容器的控制碼 (CSP) 。<br/>                                                                                        | 1          |
| **CAPICOM \_ PROPID \_ 金鑰 \_ >PROV \_ 資訊**                   | CSP 內金鑰容器的相關資訊。<br/>                                                                                                                                                                                                                                 | 2          |
| **CAPICOM \_ PROPID \_ SHA1 \_ 雜湊**                        | SHA1 雜湊物件。<br/>                                                                                                                                                                                                                                                             | 3          |
| **CAPICOM \_ PROPID \_ 雜湊 \_**                        | 雜湊物件的屬性。<br/>                                                                                                                                                                                                                                                | 3          |
| **CAPICOM \_ PROPID \_ MD5 \_ 雜湊**                         | MD5 雜湊物件。<br/>                                                                                                                                                                                                                                                             | 4          |
| **CAPICOM \_ PROPID 索引 \_ 鍵 \_ 內容**                      | 主要 [*內容*](../secgloss/c-gly.md)。<br/>                                                                                                                                                                                                | 5          |
| **CAPICOM \_ PROPID \_ 金鑰 \_ 規格**                         | 索引鍵的規格。<br/>                                                                                                                                                                                                                                                   | 6          |
| **已 \_ 保留的 CAPICOM PROPID \_ IE30 \_**                    | 物件是否保留在 Internet Explorer 3.0 中的相關資訊。<br/>                                                                                                                                                                                                      | 7          |
| **已 \_ 保留的 CAPICOM PROPID \_ PUBKEY \_ 雜湊 \_**            | 是否保留公開金鑰雜湊的相關資訊。<br/>                                                                                                                                                                                                               | 8          |
| **CAPICOM \_ PROPID \_ ENHKEY \_ 使用方式**                     |  (EKU) 的 [*增強金鑰使用*](../secgloss/e-gly.md) 方法。<br/>                                                                                                                                                              | 9          |
| **CAPICOM \_ PROPID \_ CTL \_ 使用方式**                        | [*憑證信任清單*](../secgloss/c-gly.md) (CTL) 使用方式。<br/>                                                                                                                                             | 9          |
| **CAPICOM \_ PROPID \_ 下一個 \_ 更新 \_ 位置**            | [*憑證撤銷清單*](../secgloss/c-gly.md)的下一個更新位置 (CRL) 。<br/>                                                                                               | 10         |
| **CAPICOM \_ PROPID \_ 易記 \_ 名稱**                    | 人們看得懂的名稱。<br/>                                                                                                                                                                                                                                                          | 11         |
| **CAPICOM \_ PROPID \_ PVK \_ 檔**                         | 包含私密金鑰的檔案。<br/>                                                                                                                                                                                                                                             | 12         |
| **CAPICOM \_ PROPID \_ 描述**                       | 人們看得懂的描述。<br/>                                                                                                                                                                                                                                                   | 13         |
| **CAPICOM \_ PROPID \_ 存取 \_ 狀態**                     | 存取的狀態。<br/>                                                                                                                                                                                                                                                        | 14         |
| **CAPICOM \_ PROPID \_ 簽名 \_ 雜湊**                   | 簽章的雜湊。<br/>                                                                                                                                                                                                                                                        | 15         |
| **CAPICOM \_ PROPID \_ 智慧 \_ 卡 \_ 資料**                 | 智慧卡資料。<br/>                                                                                                                                                                                                                                                                | 16         |
| **CAPICOM \_ PROPID \_ EFS**                               | [*加密檔案系統*](../secgloss/e-gly.md) (EFS) 。<br/>                                                                                                                                                  | 17         |
| **CAPICOM \_ PROPID \_ FORTEZZA \_ 資料**                    | 使用「 [*國家/地區」標準和技術*](../secgloss/n-gly.md) 所擁有的密碼編譯通訊協定和演算法所建立的資料 (NIST) 。<br/> | 18         |
| **已封存的 CAPICOM \_ PROPID \_**                          | 物件是否已封存的相關資訊。<br/>                                                                                                                                                                                                                               | 19         |
| **CAPICOM \_ PROPID \_ 金鑰 \_ 識別碼**                   | 金鑰識別碼。<br/>                                                                                                                                                                                                                                                               | 20         |
| **CAPICOM \_ PROPID \_ 自動 \_ 註冊**                      | 憑證的自動註冊資訊。<br/>                                                                                                                                                                                                                                  | 21         |
| **CAPICOM \_ PROPID \_ PUBKEY \_ ALG \_ 段落**                 | 公開金鑰演算法的參數。<br/>                                                                                                                                                                                                                                          | 22         |
| **CAPICOM \_ PROPID \_ 跨 \_ CERT \_ DIST \_ 點**         | 用來更新動態交叉憑證的資訊。<br/>                                                                                                                                                                                                                          | 23         |
| **CAPICOM \_ PROPID \_ 簽發 \_ 者 \_ 公開金鑰 \_ MD5 \_ 雜湊**    | 簽發者之公開金鑰的 MD5 雜湊。<br/>                                                                                                                                                                                                                                        | 24         |
| **CAPICOM \_ PROPID \_ 主體 \_ 公開金鑰 \_ \_ MD5 \_ 雜湊**   | 主體公開金鑰的 MD5 雜湊。<br/>                                                                                                                                                                                                                                       | 25         |
| **CAPICOM \_ PROPID \_ 註冊**                        | 憑證註冊的相關資訊。<br/>                                                                                                                                                                                                                                 | 26         |
| **CAPICOM \_ PROPID \_ 日期 \_ 戳記**                       | 日期戳記。<br/>                                                                                                                                                                                                                                                                   | 27         |
| **CAPICOM \_ PROPID \_ 簽發 \_ 者 \_ 序號 \_ MD5 \_ 雜湊** | 簽發者序號的 MD5 雜湊。<br/>                                                                                                                                                                                                                                     | 28         |
| **CAPICOM \_ PROPID \_ 主體 \_ 名稱 \_ MD5 \_ 雜湊**          | 主體名稱的 MD5 雜湊。<br/>                                                                                                                                                                                                                                             | 29         |
| **CAPICOM \_ PROPID \_ 延伸 \_ 錯誤 \_ 資訊**             | 有關錯誤的延伸資訊。<br/>                                                                                                                                                                                                                                            | 30         |
| **CAPICOM \_ PROPID \_ 續約**                           | [*憑證授權單位*](../secgloss/c-gly.md)單位更新的相關資訊。<br/>                                                                                                                     | 64         |
| **CAPICOM \_ PROPID 封存的 \_ \_ 金鑰 \_ 雜湊**               | 金鑰的封存雜湊。<br/>                                                                                                                                                                                                                                                      | 65         |
| **\_ \_ 先保留 CAPICOM \_ PROPID**                   | 第一個保留的相關資訊。<br/>                                                                                                                                                                                                                                        | 66         |
| **\_ \_ 上次 \_ 保留的 CAPICOM PROPID**                    | 最新保留的相關資訊。<br/>                                                                                                                                                                                                                                  | 0x00007FFF |
| **CAPICOM \_ PROPID \_ 第一位 \_ 使用者**                       | 第一個使用者的相關資訊。<br/>                                                                                                                                                                                                                                               | 0x00008000 |
| **CAPICOM \_ PROPID \_ 上次 \_ 使用者**                        | 最新使用者的相關資訊。<br/>                                                                                                                                                                                                                                         | 0x0000FFFF |



## <a name="remarks"></a>備註

下列的 CAPICOM 屬性會使用這個列舉：

-   [**ExtendedProperty. PropID**](extendedproperty-propid.md)
-   [**ExtendedProperties。移除**](extendedproperties-remove.md)

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|--------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                |
| 標頭<br/>          | <dl> <dt>Capicom</dt> </dl> |



 

 
