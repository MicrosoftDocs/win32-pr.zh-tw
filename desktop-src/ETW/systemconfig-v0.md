---
description: SystemConfig_V0 類別-此類別是硬體設定事件的父類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: 9da1a7ec-89b5-462b-a336-544e4b7adf96
title: SystemConfig_V0 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_V0
api_type:
- NA
api_location: ''
ms.openlocfilehash: 6986e5ac907784a19c14fb8dc6b9c086031863f322c3c35a58edcf3fd4089ea8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118151218"
---
# <a name="systemconfig_v0-class"></a>SystemConfig \_ V0 類別

此類別是硬體設定事件的父類別。

以下是從 MOF 程式碼簡化的語法。

## <a name="syntax"></a>語法

``` syntax
[Guid("{01853a65-418f-4f36-aefc-dc0f1d2fd235}"), EventVersion(0)]
class SystemConfig_V0 : MSNT_SystemTrace
{
};
```

## <a name="members"></a>成員

**SystemConfig \_ V0** 類別未定義任何成員。

## <a name="remarks"></a>備註

如需 Windows XP 上的硬體設定事件，請參閱 [**HWConfig**](hwconfig.md)類別。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                            |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MSNT \_ SystemTrace**](msnt-systemtrace.md)
</dt> <dt>

[**SystemConfig**](systemconfig.md)
</dt> <dt>

[**SystemConfig \_ V0 \_ CPU**](systemconfig-v0-cpu.md)
</dt> <dt>

[**SystemConfig \_ V0 \_ LogDisk**](systemconfig-v0-logdisk.md)
</dt> <dt>

[**SystemConfig \_ V0 \_ NIC**](systemconfig-v0-nic.md)
</dt> <dt>

[**SystemConfig \_ V0 \_ PhyDisk**](systemconfig-v0-phydisk.md)
</dt> <dt>

[**SystemConfig \_ V0 \_ 電源**](systemconfig-v0-power.md)
</dt> <dt>

[**SystemConfig \_ V0 \_ 服務**](systemconfig-v0-services.md)
</dt> <dt>

[**SystemConfig \_ V0 \_ 影片**](systemconfig-v0-video.md)
</dt> </dl>

 

 




