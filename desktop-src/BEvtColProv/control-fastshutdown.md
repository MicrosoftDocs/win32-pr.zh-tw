---
description: 快速停止收集器，並捨棄所有已排入佇列的資料。
ms.assetid: 9d96a94b-21ae-40bd-9c7f-b466ca38dce3
ms.tgt_platform: multiple
title: Control 類別的 FastShutdown 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.FastShutdown
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: 444fe9c94e9fd247e5976fd67a43b0a5eee8b591
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973369"
---
# <a name="fastshutdown-method-of-the-control-class"></a>Control 類別的 FastShutdown 方法

快速停止收集器，並捨棄所有已排入佇列的資料。

## <a name="syntax"></a>語法


```mof
void FastShutdown();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 10 桌面應用程式\]<br/>                                                          |
| 最低支援的伺服器<br/> | Windows Server 2016<br/>                                                                       |
| 命名空間<br/>                | 根 \\ Microsoft \\ Windows \\ BootEventCollector<br/>                                              |
| MOF<br/>                      | <dl> <dt>BootEventCollectorWMI Mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>BEvtCol.exe</dt> </dl>               |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**控制**](control.md)
</dt> </dl>

 

 




