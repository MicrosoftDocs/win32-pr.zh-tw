---
description: 將引數與收集器的使用中設定進行比較。
ms.assetid: 8decb674-c905-4eb6-9f78-7bc7b99db908
ms.tgt_platform: multiple
title: Control 類別的 IsConfigurationEqual 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.IsConfigurationEqual
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: 6facd4f885eb1eb992f95bf4432e32704f7472d8125cb1022f7a6baf5cf591d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119579668"
---
# <a name="isconfigurationequal-method-of-the-control-class"></a>Control 類別的 IsConfigurationEqual 方法

將引數與收集器的使用中設定進行比較。

## <a name="syntax"></a>語法


```mof
Uint32 IsConfigurationEqual(
  [in] string Config
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*Config* \[在\]
</dt> <dd>

要與現用設定比較的設定。

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

 

 




