---
description: 指定端點資料遺失防止 (DLP) 操作的動作類型。
title: 'DlpActionType 列舉 (endpointdlp) '
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpActionType
api_type:
- COM
api_location:
- endpointdlp.h
ms.openlocfilehash: 5b7066eec7832ba0b76dee38e6483e0bfcfcfb05fdb8448ee7b3a91e701069fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976648"
---
# <a name="dlpactiontype-enumeration"></a>DlpActionType 列舉

指定端點資料遺失防止 (DLP) 操作的動作類型。

## <a name="syntax"></a>Syntax


```C++
typedef enum  
{
    DlpActionTypeCopyToRemovableMedia = 0,
    DlpActionTypeCopyToNetworkShare = 1,
    DlpActionTypeCopyToClipboard = 2,
    DlpActionTypePrint = 3,
    DlpActionTypeScreenClip = 4,
    DlpActionTypeAccessByUnallowedApp = 5,
    DlpActionTypeCloudAppEgress = 6,
    DlpActionTypeAccessByBluetoothApp = 7,
    DlpActionTypeAccessByRDPApp = 8,
    DlpActionTypeCount = 9
} DlpActionType;
```


## <a name="constants"></a>常數

<dl> <dt>

*DlpActionTypeCopyToRemovableMedia*
</dt> <dd>

卸載式媒體的複製操作。

</dd> </dl>

<dl> <dt>

*DlpActionTypeCopyToNetworkShare*
</dt> <dd>

共用網路資料夾的複製操作。

</dd> </dl>

<dl> <dt>

*DlpActionTypeCopyToClipboard*
</dt> <dd>

剪貼簿的複製操作。

</dd> </dl>

<dl> <dt>

*DlpActionTypePrint*
</dt> <dd>

列印操作。

</dd> </dl>


<dl> <dt>

*DlpActionTypeScreenClip*
</dt> <dd>

畫面捕捉作業。

</dd> </dl>

<dl> <dt>

*DlpActionTypeAccessByUnallowedApp*
</dt> <dd>

不允許之應用程式所執行的作業。

</dd> </dl>


<dl> <dt>

*DlpActionTypeCloudAppEgress*
</dt> <dd>

以雲端位置為目標的作業。

</dd> </dl>

<dl> <dt>

*DlpActionTypeAccessByBluetoothApp*
</dt> <dd>

包含藍牙應用程式存取權的作業。

</dd> </dl>

<dl> <dt>

*DlpActionTypeAccessByRDPApp*
</dt> <dd>

包含遠端桌面存取權的作業。

</dd> </dl>

<dl> <dt>

*DlpActionTypeCount*
</dt> <dd>

列舉的最大值。

</dd> </dl>
 

## <a name="remarks"></a>備註

[DLP_APP_OP_ENLIGHTENED_LEVEL](endpointdlp-dlp_app_op_enlightened_level.md)結構會使用這個列舉的值。

## <a name="requirements"></a>規格需求



| 需求          |    值                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10 版本 1809 (10.0;組建 17763)            |

