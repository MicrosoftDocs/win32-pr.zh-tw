---
description: 讀取收集器的主動式設定。
ms.assetid: ea26142d-5dcd-466d-b9df-5349f58a190f
ms.tgt_platform: multiple
title: Control 類別的 GetConfiguration 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.GetConfiguration
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: a877b4ae061b6568b877d9b8ee65b8d9b0380a012d7fdba28408ad4bfcae7030
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119579718"
---
# <a name="getconfiguration-method-of-the-control-class"></a>Control 類別的 GetConfiguration 方法

讀取收集器的主動式設定。

## <a name="syntax"></a>語法


```mof
Uint32 GetConfiguration(
  [out] Uint32 TimestampLow,
  [out] Uint32 TimestampHigh
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*TimestampLow* \[擴展\]
</dt> <dd>

當此方法傳回時，此參數會包含時間戳記的低序位位，指出設定的設定時間。

</dd> <dt>

*TimestampHigh* \[擴展\]
</dt> <dd>

當此方法傳回時，此參數會包含時間戳記的高序位位，指出設定的設定時間。

</dd> </dl>

## <a name="return-value"></a>傳回值

<dl> <dt>


</dt> <dd>

0

失敗

</dd> <dt>


</dt> <dd>

1

Success

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10 \[僅限桌面應用程式\]<br/>                                                          |
| 最低支援的伺服器<br/> | Windows Server 2016<br/>                                                                       |
| 命名空間<br/>                | 根 \\ Microsoft \\ Windows \\ BootEventCollector<br/>                                              |
| MOF<br/>                      | <dl> <dt>BootEventCollectorWMI mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>BEvtCol.exe</dt> </dl>               |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**控制**](control.md)
</dt> </dl>

 

 




