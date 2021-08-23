---
description: 停止收集器。 如果收集器是以服務方式執行，則停止服務是較佳的方法。
ms.assetid: fab3e060-156f-46f5-98a2-d47a23d64552
ms.tgt_platform: multiple
title: Control 類別的 Shutdown 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.Shutdown
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: 6a83b798ff89116ad0e7cadad1a4dac74b3722bdbb2410c1cad09a3ac8c9c710
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119529658"
---
# <a name="shutdown-method-of-the-control-class"></a>Control 類別的 Shutdown 方法

停止收集器。 如果收集器是以服務方式執行，則停止服務是較佳的方法。

## <a name="syntax"></a>語法


```mof
void Shutdown();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

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

 

 




