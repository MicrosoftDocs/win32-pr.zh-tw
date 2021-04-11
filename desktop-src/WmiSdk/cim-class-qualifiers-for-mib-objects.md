---
description: 當將 MIB 物件定義對應至 CIM 類別定義時，SNMP 提供者會使用下列 CIM 類別限定詞。
ms.assetid: 458167dc-562e-47b8-8760-797ae13f9459
ms.tgt_platform: multiple
title: MIB 物件的 CIM 類別限定詞
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d60fe97debc7fd81b48a6daf0f5a955374546458
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194491"
---
# <a name="cim-class-qualifiers-for-mib-objects"></a>MIB 物件的 CIM 類別限定詞

當將 MIB 物件定義對應至 CIM 類別定義時，SNMP 提供者會使用下列 CIM 類別限定詞。 SNMP 提供者必須要有必要的限定詞，才能完全解析群組物件。 無法定義強制辨識符號會傳回錯誤。 指定不合法的辨識符號值也會傳回錯誤。

> [!Note]  
> 如需安裝提供者的詳細資訊，請參閱 [設定 WMI SNMP 環境](setting-up-the-wmi-snmp-environment.md)。

 



| Qualifier           | 描述                                                                                                                             |
|---------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| **說明**     | **字串** 選<br/> 類別的描述。<br/>                                                                      |
| **群組 \_ Objectid** | **字串** 如果是 SNMP 類別提供者的類別，則為必要項。<br/> 製造之集合的物件識別碼。<br/> |
| **模組匯 \_ 入** | **字串** 選<br/> 用來解析匯入之 MIB 模組名稱的逗號分隔清單。<br/>                              |
| **模組 \_ 名稱**    | **字串** 選<br/> MIB 模組的身分識別名稱。<br/>                                                                 |
| **參考**       | **字串** 選<br/> 是指包含類別之詳細資訊的另一份檔。<br/>                     |
| **單身 人士**       | **Bool** 從純量集合對應之類別的必要參數。<br/> 表示只能有一個實例的類別。<br/>  |



 

 

 




