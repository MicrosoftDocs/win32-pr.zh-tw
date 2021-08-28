---
description: SNMP 集合會對應到 CIM 類別，而集合的元素會對應至 CIM 類別的屬性。 所有產生的 CIM 類別定義都必須衍生自 SnmpObjectType 類別。
ms.assetid: e6f82fd6-e3d8-48c5-8c7b-a30a2d502f41
ms.tgt_platform: multiple
title: SNMP 集合
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: df4926ab89a6bb9a936fe5bdb27f921699bbe90a528842d81de96d8049412940
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118315302"
---
# <a name="snmp-collections"></a>SNMP 集合

SNMP 集合會對應到 CIM 類別，而集合的元素會對應至 CIM 類別的屬性。 所有產生的 CIM 類別定義都必須衍生自 **SnmpObjectType** 類別。

> [!Note]  
> 如需安裝提供者的詳細資訊，請參閱 [設定 WMI SNMP 環境](setting-up-the-wmi-snmp-environment.md)。

 

下列類別定義父代所有產生的類別定義：

``` syntax
[abstract]
class SnmpMacro
{
};

[abstract]
class SnmpObjectType:SnmpMacro
{
};
```

## <a name="remarks"></a>備註

將 SNMP 集合對應至 CIM 類別時，適用下列規則。 除非另有指定，否則這些規則適用于純量和資料表集合：

-   對應程式會串連 "SNMP \_ "、MIB 模組識別名稱、" \_ " 和集合的物件描述元，以產生 CIM 類別名稱。

    例如： **系統** 會轉譯為 **snmp \_ RFC1213 \_ MIB \_ 系統**，而 **ifTable** 則會轉譯為 **snmp \_ RFC1213 \_ mib \_ ifTable**。

-   在所有情況下，SNMP MIB 識別碼中的連字號 ( ) 會對應到 \_ CIM 類別名稱中的底線 () 。
-   由於 CIM 名稱不區分大小寫，因此可能會發生命名衝突。 如果發生命名衝突，提供者會選擇其中一個衝突的群組定義，並忽略其餘的定義。
-   包含集合的 MIB 模組的身分識別名稱會對應到 CIM 類別限定詞 **模組 \_ 名稱**。
-   製造集合的物件識別碼會對應至 CIM 類別限定詞 **群組 \_ Objectid**。
-   從 **模組身分識別** 巨集定義取得的 MIB 模組匯入清單 (，) 對應至 CIM 類別限定詞 **模組匯 \_ 入**。 此限定詞包含以逗號分隔的模組名稱清單。

 

 



