---
description: WDM 類別提供者會定義 \\ 根 wmi 命名空間中的 WMIBinaryMofResource 類別 \\ ，以支援追蹤 wmi 儲存機制中資料狀態的工作。
ms.assetid: 57416a36-5b3a-4d04-808c-09adc597c47a
title: WMIBinaryMofResource 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WMIBinaryMofResource
- WMIBinaryMofResource.HighDateTime
- WMIBinaryMofResource.LowDateTime
- WMIBinaryMofResource.MofProcessed
- WMIBinaryMofResource.Name
api_type:
- Schema
api_location:
- Root\WMI
ms.openlocfilehash: 715436ef19308c811e5486926b3cd7e59ee9de0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848397"
---
# <a name="wmibinarymofresource-class"></a>WMIBinaryMofResource 類別

WDM 類別提供者會定義 \\ 根 wmi 命名空間中的 WMIBinaryMofResource 類別 \\ ，以支援追蹤 wmi 儲存機制中資料狀態的工作。

## <a name="syntax"></a>語法

``` syntax
class WMIBinaryMofResource
{
  uint32  HighDateTime;
  uint32  LowDateTime;
  boolean MofProcessed;
  string  Name;
};
```

## <a name="members"></a>成員

**WMIBinaryMofResource** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**WMIBinaryMofResource** 類別具有這些屬性。

<dl> <dt>

**HighDateTime**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

高一半的日期時間戳記。

</dd> <dt>

**LowDateTime**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

日期時間戳記的下半部。

</dd> <dt>

**MofProcessed**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

指出是否已完整處理 mof 檔案的旗標。

</dd> <dt>

**名稱**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

已啟用 WDM 的驅動程式名稱，此驅動程式在 WMI 儲存機制中已成功編譯二進位 MOF 檔案。

</dd> </dl>

## <a name="remarks"></a>備註

WDM 類別提供者會為每個提供二進位 MOF 檔案的 WDM 驅動程式建立 **WMIBinaryMofResource** 的實例。

每當 WMI 初始化提供者時，提供者會將時間戳記與驅動程式影像檔的時間戳記進行比較。 如果時間戳記不同，WMI 會重新編譯 MOF 檔案。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows XP<br/>                                                              |
| 最低支援的伺服器<br/> | Windows Server 2003<br/>                                                     |
| 命名空間<br/>                | 根 \\ WMI<br/>                                                               |
| MOF<br/>                      | <dl> <dt>Wmi. mof</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[WDM 提供者](wdm-provider.md)
</dt> </dl>

 

