---
title: 'CB_RESOURCE_TYPE 列舉 (Cbclient .h) '
description: 指定連入連接所連線的資源類型。
ms.assetid: 80D921BF-2D84-4A18-9544-50087B81F177
ms.tgt_platform: multiple
keywords:
- CB_RESOURCE_TYPE 列舉遠端桌面服務
topic_type:
- apiref
api_name:
- CB_RESOURCE_TYPE
api_location:
- Cbclient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63dfce0f575147233735dd943645eb51c26141cacaaa61c044698b29b8d118e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139111"
---
# <a name="cb_resource_type-enumeration"></a>CB \_ 資源 \_ 類型列舉

指定連入連接所連線的資源類型。 此列舉會搭配 [**CB \_ 連接 \_ 資訊**](cb-connection-info.md) 結構使用。

## <a name="syntax"></a>Syntax


```C++
typedef enum _CB_RESOURCE_TYPE { 
  CB_RESOURCE_UNDEFINED  = 0,
  CB_RESOURCE_SESSION    = 1,
  CB_RESOURCE_VM
} CB_RESOURCE_TYPE;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="CB_RESOURCE_UNDEFINED"></span><span id="cb_resource_undefined"></span>**CB \_ 資源 \_ 未定義**
</dt> <dd>

資源類型未定義。

</dd> <dt>

<span id="CB_RESOURCE_SESSION"></span><span id="cb_resource_session"></span>**CB \_ 資源 \_ 會話**
</dt> <dd>

資源是遠端會話。

</dd> <dt>

<span id="CB_RESOURCE_VM"></span><span id="cb_resource_vm"></span>**CB \_ 資源 \_ VM**
</dt> <dd>

資源是一種虛擬機器。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8<br/>                                                                  |
| 最低支援的伺服器<br/> | Windows Server 2012<br/>                                                        |
| 標頭<br/>                   | <dl> <dt>Cbclient。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CB \_ 連接 \_ 資訊**](cb-connection-info.md)
</dt> </dl>

 

 





