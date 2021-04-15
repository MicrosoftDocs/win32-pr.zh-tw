---
title: MSAD_ReplCursor 類別
description: 提供有關指定命名內容的所有複本 (NC) 的輸入複寫狀態資訊。
ms.assetid: 5746cfe9-b113-4be3-b609-15cb937c271b
ms.tgt_platform: multiple
keywords:
- MSAD_ReplCursor 類別 Active Directory
- MSAD_ReplCursor 類別 Active Directory，描述
topic_type:
- apiref
api_name:
- MSAD_ReplCursor
- MSAD_ReplCursor.NamingContextDN
- MSAD_ReplCursor.SourceDsaInvocationID
- MSAD_ReplCursor.USNAttributeFilter
- MSAD_ReplCursor.SourceDsaDN
- MSAD_ReplCursor.TimeOfLastSuccessfulSync
api_location:
- replprov.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f725ac8e9eee9f921ce4109e0b0e42ed85e75ab8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465393"
---
# <a name="msad_replcursor-class"></a>MSAD \_ ReplCursor 類別

提供有關指定命名內容的所有複本 (NC) 的輸入複寫狀態資訊。

## <a name="syntax"></a>語法

``` syntax
[dynamic, provider("ReplProv1")]
class MSAD_ReplCursor
{
  String   NamingContextDN;
  String   SourceDsaInvocationID;
  uint64   USNAttributeFilter;
  String   SourceDsaDN;
  datetime TimeOfLastSuccessfulSync;
};
```

## <a name="members"></a>成員

**MSAD \_ ReplCursor** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**MSAD \_ ReplCursor** 類別具有這些屬性。

<dl> <dt>

**NamingCoNtextDN**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

取得保存此資料指標的命名內容 (NC) 的 X. 500 路徑。

</dd> <dt>

**SourceDsaDN**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

取得目錄服務代理程式 (DSA) 的 X. 500 路徑，該路徑代表 (DC) 的來源網域控制站。

</dd> <dt>

**SourceDsaInvocationID**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

取得 **USNAttributeFilter** 所對應之源伺服器的調用識別碼。

</dd> <dt>

**TimeOfLastSuccessfulSync**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

取得上次與來源 DSA 成功複寫同步處理的時間戳記。 指出此 DC 上次看到此 NC 來源 DSA 上所做變更的時間。

</dd> <dt>

**USNAttributeFilter**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

取得目的地伺服器在更新序號小於或等於此更新序號時，所產生之所有變更所產生的更新序號（最大值）。 這個屬性是用來篩選目的地伺服器已套用於複寫來源伺服器的變更。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                               |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 命名空間<br/>                | 根 \\ MicrosoftActiveDirectory<br/>                                               |
| MOF<br/>                      | <dl> <dt>Replprov.dll mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Replprov.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**DS 複寫資料 \_ \_ 指標**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_cursor)
</dt> </dl>

 

