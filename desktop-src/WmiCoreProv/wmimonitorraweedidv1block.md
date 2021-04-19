---
description: 表示來自視頻電子郵件標準關聯的原始資料 (VESA) 增強的擴充顯示器識別資料 (E-EDID) 結構。
ms.assetid: a51b73bb-a5f7-4e01-9c88-780105e9952b
title: WmiMonitorRawEEdidV1Block 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorRawEEdidV1Block
- WmiMonitorRawEEdidV1Block.Active
- WmiMonitorRawEEdidV1Block.InstanceName
- WmiMonitorRawEEdidV1Block.Id
- WmiMonitorRawEEdidV1Block.Type
- WmiMonitorRawEEdidV1Block.Content
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 79566dccceb36281c9b3a94b19fed2ed5679dc8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106982488"
---
# <a name="wmimonitorraweedidv1block-class"></a>WmiMonitorRawEEdidV1Block 類別

**WmiMonitorRawEEdidV1Block** WMI 類別代表來自視頻電子郵件標準關聯的原始資料 (VESA) 增強的擴充顯示器識別資料 (E-EDID) 結構。 這個128位元組資料結構包含的資訊會描述顯示的最佳設定。

## <a name="syntax"></a>語法

``` syntax
class WmiMonitorRawEEdidV1Block : MSMonitorClass
{
  boolean Active;
  string  InstanceName;
  uint8   Id;
  uint8   Type;
  uint8   Content[];
};
```

## <a name="members"></a>成員

**WmiMonitorRawEEdidV1Block** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**WmiMonitorRawEEdidV1Block** 類別具有這些屬性。

<dl> <dt>

**使用中**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

表示使用中的監視器。

</dd> <dt>

**內容**
</dt> <dd> <dl> <dt>

資料類型： **uint8** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

128位元組陣列，其中包含原始區塊內容。

</dd> <dt>

**識別碼**
</dt> <dd> <dl> <dt>

資料類型： **uint8**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

資料區塊的識別。

</dd> <dt>

**InstanceName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 **鍵**
</dt> </dl>

特定監視實例的名稱。

</dd> <dt>

**型別**
</dt> <dd> <dl> <dt>

資料類型： **uint8**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

資料區塊的類型。 下表列出可以傳回的可能值。



| 值                                                                                 | 意義                    |
|---------------------------------------------------------------------------------------|----------------------------|
| <dl> <dt>0 (0x0) </dt> </dl>    | 未初始化：<br/>   |
| <dl> <dt>1 (0x1) </dt> </dl>    | EDID 基底區塊<br/> |
| <dl> <dt>2 (0x2) </dt> </dl>    | EDID 區塊對應<br/>  |
| <dl> <dt>255 (0xFF) </dt> </dl> | 其他<br/>           |



 

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                               |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                         |
| 命名空間<br/>                | 根 \\ wmi<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>WmiCore mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WmiProv.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MSMonitorClass**](msmonitorclass.md)
</dt> <dt>

[**WmiGetMonitorRawEEdidV1Block**](wmigetmonitorraweedidv1block-wmimonitordescriptormethods.md)
</dt> </dl>

 

 




