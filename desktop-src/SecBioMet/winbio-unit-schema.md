---
title: 'WINBIO_UNIT_SCHEMA 結構 (Winbio \_ 類型 .h) '
description: 描述生物特徵辨識設備的功能。
ms.assetid: b20adf18-2948-481f-9d12-8da17aa152f7
keywords:
- WINBIO_UNIT_SCHEMA 結構 Windows 生物特徵辨識架構 API
- PWINBIO_UNIT_SCHEMA 結構指標 Windows 生物特徵辨識架構 API
topic_type:
- apiref
api_name:
- WINBIO_UNIT_SCHEMA
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae91ae5353aa0e9c02414e90a8364d86bdc56c0cdcc4f4586656f28f92f100ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118909167"
---
# <a name="winbio_unit_schema-structure"></a>WINBIO \_ 單元 \_ 架構結構

**WINBIO \_ 單元 \_ 架構** 結構描述生物特徵辨識設備的功能。 [**WinBioEnumBiometricUnits**](/windows/desktop/api/Winbio/nf-winbio-winbioenumbiometricunits)函式會使用它。

## <a name="syntax"></a>語法


```C++
typedef struct _WINBIO_UNIT_SCHEMA {
  WINBIO_UNIT_ID                  UnitId;
  WINBIO_POOL_TYPE                PoolType;
  WINBIO_BIOMETRIC_TYPE           BiometricFactor;
  WINBIO_BIOMETRIC_SENSOR_SUBTYPE SensorSubType;
  WINBIO_CAPABILITIES             Capabilities;
  WINBIO_STRING                   DeviceInstanceId;
  WINBIO_STRING                   Description;
  WINBIO_STRING                   Manufacturer;
  WINBIO_STRING                   Model;
  WINBIO_STRING                   SerialNumber;
  WINBIO_VERSION                  FirmwareVersion;
} WINBIO_UNIT_SCHEMA, *PWINBIO_UNIT_SCHEMA;
```



## <a name="members"></a>成員

<dl> <dt>

**UnitId**
</dt> <dd>

識別生物特徵辨識單位的值。

</dd> <dt>

**PoolType**
</dt> <dd>

指定生物特徵辨識單位類型的 **ULONG** 值。 這個值可以是下列其中一個值：



| 值                                                                                                                                                                            | 意義                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_POOL_UNKNOWN"></span><span id="winbio_pool_unknown"></span><dl> <dt>**WINBIO \_ 集區 \_ 不明**</dt> </dl> | 未知的類型。<br/>                                                                            |
| <span id="WINBIO_POOL_SYSTEM"></span><span id="winbio_pool_system"></span><dl> <dt>**WINBIO \_ 集區 \_ 系統**</dt> </dl>    | 會話會連接到服務提供者所管理的生物識別單位共用集合。<br/> |
| <span id="WINBIO_POOL_PRIVATE"></span><span id="winbio_pool_private"></span><dl> <dt>**WINBIO \_ 集區 \_ 私用**</dt> </dl> | 會話會連接到由呼叫端管理的生物特徵辨識單位集合。<br/>         |



 

</dd> <dt>

**BiometricFactor**
</dt> <dd>

指定生物特徵辨識單位類型的值。 目前只支援 **WINBIO \_ 類型 \_ 指紋** 。

</dd> <dt>

**SensorSubType**
</dt> <dd>

針對 **BiometricFactor** 成員所指定的生物特徵辨識類型定義的感應器子類型。 目前只支援 (**WINBIO \_ 類型 \_ 指紋**) 的指紋類型。 下列子類型目前為指紋定義：

-   WINBIO \_ 感應器 \_ 子類型 \_ 不明
-   WINBIO \_ FP \_ 感應器 \_ 子類型 \_ 滑動
-   WINBIO \_ FP \_ 感應器 \_ 子類型 \_ 觸控

</dd> <dt>

**Capabilities**
</dt> <dd>

生物識別感應器功能的位元遮罩。 這可以是下列值的位 **or** ：

-   WINBIO \_ 功能 \_ 感應器
-   WINBIO \_ 功能比對 \_
-   WINBIO \_ 功能 \_ 資料庫
-   WINBIO \_ 功能 \_ 處理
-   WINBIO \_ 功能 \_ 加密
-   WINBIO \_ 功能 \_ 導覽
-   WINBIO \_ 功能 \_ 指標
-   WINBIO \_ 功能 \_ 虛擬 \_ 感應器
    > [!Note]  
    > **WINBIO \_ 功能 \_ 虛擬 \_ 感應器** 常數只適用于 Windows 10 和更新版本。

     

</dd> <dt>

**DeviceInstanceId**
</dt> <dd>

包含裝置識別碼的字串值。 字串最多可以包含256個 Unicode 字元，包括結束的 **Null** 字元。

</dd> <dt>

**說明**
</dt> <dd>

包含生物特徵辨識單位描述的字串值。 字串最多可以包含256個 Unicode 字元，包括結束的 **Null** 字元。

</dd> <dt>

**製造商**
</dt> <dd>

包含製造商名稱的字串值。 字串最多可以包含256個 Unicode 字元，包括結束的 **Null** 字元。

</dd> <dt>

**型號**
</dt> <dd>

字串值，包含生物特徵辨識單位的模型編號。 字串最多可以包含256個 Unicode 字元，包括結束的 **Null** 字元。

</dd> <dt>

**SerialNumber**
</dt> <dd>

以 **Null** 終止的 Unicode 字串，其中包含生物特徵辨識單位的序號。 字串最多可以包含256個 Unicode 字元，包括結束的 **Null** 字元。

</dd> <dt>

**FirmwareVersion**
</dt> <dd>

[**WINBIO \_ 版本**](winbio-version.md)結構，其中包含生物識別單位的主要和次要版本號碼。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>                                                                    |
| 最低支援的伺服器<br/> | Windows僅限 Server 2008 R2 \[ desktop 應用程式\]<br/>                                                       |
| 標頭<br/>                   | <dl> <dt>Winbio \_ 類型 .h (包含 Winbio .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[用戶端應用程式結構](client-application-structures.md)
</dt> <dt>

[**WinBioEnumBiometricUnits**](/windows/desktop/api/Winbio/nf-winbio-winbioenumbiometricunits)
</dt> </dl>

 

 





