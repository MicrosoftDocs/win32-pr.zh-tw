---
title: MSAD_NamingCoNtext 類別
description: 代表網域控制站上 (NC) 的特定命名內容。
ms.assetid: 67dd6c68-6c67-40b4-a20a-c6c312d23441
ms.tgt_platform: multiple
keywords:
- MSAD_NamingCoNtext 類別 Active Directory
- MSAD_NamingCoNtext 類別 Active Directory，描述
topic_type:
- apiref
api_name:
- MSAD_NamingContext
- MSAD_NamingContext.DistinguishedName
- MSAD_NamingContext.IsFullReplica
api_location:
- replprov.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 571f13642116be0e846fe1350cd932d52087d9f0422b8f40d695e4fef99df5cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025776"
---
# <a name="msad_namingcontext-class"></a>MSAD \_ NamingCoNtext 類別

代表網域控制站上 (NC) 的特定命名內容。

## <a name="syntax"></a>語法

``` syntax
[dynamic, provider("ReplProv1")]
class MSAD_NamingContext
{
  String  DistinguishedName;
  boolean IsFullReplica = FALSE;
};
```

## <a name="members"></a>成員

**MSAD \_ NamingCoNtext** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**MSAD \_ NamingCoNtext** 類別具有這些屬性。

<dl> <dt>

**DistinguishedName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

取得 NC 的 X. 500 路徑。

</dd> <dt>

**IsFullReplica**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

取得值，這個值會指出 NC 是否為讀取/寫入。 如果 NC 為讀取/寫入，則 **為 TRUE** ;如果 NC 是唯讀的，則 **為 FALSE** 。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                               |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 命名空間<br/>                | 根 \\ MicrosoftActiveDirectory<br/>                                               |
| MOF<br/>                      | <dl> <dt>Replprov.dll mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Replprov.dll</dt> </dl> |



 

