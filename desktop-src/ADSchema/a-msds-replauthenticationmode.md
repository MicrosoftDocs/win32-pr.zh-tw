---
title: ms DS-複寫-驗證模式屬性
description: Ms DS-複寫驗證模式屬性是用來指定用來驗證複寫夥伴的驗證方法。
ms.assetid: b7e77b40-7aa7-4990-93fd-c8068e35fcf9
ms.tgt_platform: multiple
keywords:
- ms DS-複寫-驗證模式屬性 AD 架構
- Msds-replauthenticationmode 屬性 AD 架構
topic_type:
- apiref
api_name:
- ms-DS-Repl-Authentication-Mode
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3b88c7e3223b946b56962b710b036ee6e0c36dc
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104467350"
---
# <a name="ms-ds-repl-authentication-mode-attribute"></a>ms DS-複寫-驗證模式屬性

**MS DS-複寫驗證模式** 屬性是用來指定用來驗證複寫夥伴的驗證方法。 這個屬性會套用至 ADAM 實例的設定磁碟分割。

下列值是這個屬性的可能值。

| 值        | 驗證方法                          | 描述                                                                                                                                                                    |
|--------------|------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0<br/> | 交涉傳遞<br/>             | 設定集中的所有 ADAM 實例都使用與 ADAM 服務帳戶相同的帳戶名稱和密碼。<br/>                                                 |
| 1<br/> | 已交涉<br/>                          | 會先嘗試 Kerberos 驗證 (使用 SPN)； 如果 Kerberos 失敗，則會嘗試 NTLM 驗證。 如果 NTLM 失敗，ADAM 實例將不會複寫。<br/> |
| 2<br/> | 以 Kerberos 相互驗證<br/> | 需要 Kerberos 驗證 (使用服務主要名稱 (SPN))。 如果 Kerberos 驗證失敗，ADAM 實例將不會複寫。<br/>                |



 

下表包含此屬性值的程式設計識別碼。

| 值        | 從 Ntdsapi 的識別碼 ()                                                |
|--------------|---------------------------------------------------------------------------|
| 0<br/> | **ADAM \_ 複寫 \_ 驗證 \_ 模式 \_ 協商 \_ 傳遞 \_**<br/> |
| 1<br/> | **ADAM \_ 複寫 \_ 驗證 \_ 模式的 \_ 協商**<br/>                |
| 2<br/> | **需要 ADAM 複寫 \_ \_ 驗證 \_ 模式 \_ 相互 \_ 驗證 \_**<br/>   |



 



| 進入 | 值 |
|-------------------|--------------------------------------|
| CN                | ms-DS-複寫-驗證模式       |
| Ldap-顯示名稱 | Msds-replauthenticationmode          |
| 大小              | \-                                   |
| 更新許可權  | \-                                   |
| 更新頻率  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.1861              |
| 系統識別碼-Guid    | 6e124d4f-1a3f-4cc6-8e09-4a54c81b1d50 |
| Syntax            | [**列舉型別**](s-enumeration.md) |



## <a name="implementations"></a>實作

-   [**亞當**](#adam)

## <a name="adam"></a>亞當



| 進入 | 值 |
|------------------------|-----------------------------------------------------|
| 連結識別碼                | \-                                                  |
| MAPI-Id                | \-                                                  |
| System-Only            | 否                                               |
| 是-單一值       | 對                                                |
| 已編制索引             | 否                                               |
| 在通用類別目錄中      | 否                                               |
| NT-Security-描述元 | O:BAG：不正確： S：                                        |
| Range-Lower            | \-                                                  |
| Range-Upper            | \-                                                  |
| Search-Flags           | 0x00000000                                          |
| System-Flags           | 0x00000010                                          |
| 中使用的類別        | [**配置**](c-configuration.md)<br/> |



 

 





