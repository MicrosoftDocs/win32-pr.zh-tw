---
description: 代表數位視訊的輸入參數。
ms.assetid: aa459612-db79-477b-891f-28c9d0b1b497
title: WmiMonitorDigitalVideoInputParams 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorDigitalVideoInputParams
- WmiMonitorDigitalVideoInputParams.Active
- WmiMonitorDigitalVideoInputParams.InstanceName
- WmiMonitorDigitalVideoInputParams.IsDFP1xCompatible
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: fa86add32d77a5b2838fc78eaf097c11b8a15db3f0fde9186f93046691ebc3f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117926564"
---
# <a name="wmimonitordigitalvideoinputparams-class"></a>WmiMonitorDigitalVideoInputParams 類別

**WmiMonitorDigitalVideoInputParams** 代表數位視訊的輸入參數。 此類別中的資料會對應至視頻電子郵件標準關聯的影片輸入定義中的資料 (VESA) 增強的擴充顯示器識別資料 (E-EDID) 標準。 只有當 [**WmiMonitorBasicDisplayParams**](wmimonitorbasicdisplayparams.md)類別的 **VideoInputType** 屬性值為 "數位" 時，才能使用這個類別的實例。

## <a name="syntax"></a>語法

``` syntax
class WmiMonitorDigitalVideoInputParams : MSMonitorClass
{
  boolean Active;
  string  InstanceName;
  boolean IsDFP1xCompatible;
};
```

## <a name="members"></a>成員

**WmiMonitorDigitalVideoInputParams** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**WmiMonitorDigitalVideoInputParams** 類別具有這些屬性。

<dl> <dt>

**使用中**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

表示使用中的監視器。

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

**IsDFP1xCompatible**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

VESA DFP 1.x 或相容。 如果設定，介面與 VESA 數位平面面板的信號相容 (DFP) 1.x 轉換最小化差異信號 (TMDS) CRGB、1圖元/時鐘、最多8個位/色彩最高 (MSB) 對齊、DE 高。

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
</dt> </dl>

 

 




