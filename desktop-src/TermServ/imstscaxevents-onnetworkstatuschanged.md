---
title: IMsTscAxEvents OnNetworkStatusChanged 方法
description: 在網路狀態變更時呼叫。 |IMsTscAxEvents OnNetworkStatusChanged 方法
ms.assetid: 177A410E-2449-4FC7-8DE5-21F83A6DD028
ms.tgt_platform: multiple
keywords:
- OnNetworkStatusChanged 方法遠端桌面服務
- OnNetworkStatusChanged 方法遠端桌面服務，IMsTscAxEvents 介面
- IMsTscAxEvents 介面遠端桌面服務，OnNetworkStatusChanged 方法
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnNetworkStatusChanged
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2b9bdcd7774493fcc54e1390ad199a6a56a7c51
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106979860"
---
# <a name="imstscaxeventsonnetworkstatuschanged-method"></a>IMsTscAxEvents：： OnNetworkStatusChanged 方法

在網路狀態變更時呼叫。

## <a name="syntax"></a>語法


```C++
void OnNetworkStatusChanged(
  [in] ULONG qualityLevel,
  [in] LONG  bandwidth,
  [in] LONG  rtt
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*qualityLevel* \[在\]
</dt> <dd>

指定新的連線速度。 這會是下列其中一個值。

<dt>

1
</dt> <dd>

每秒小於 512 kb (KBps) 。

</dd> <dt>

2
</dt> <dd>

512到 1999 KBps。

</dd> <dt>

3
</dt> <dd>

2000到 9999 KBps。

</dd> <dt>

4
</dt> <dd>

大於或等於 10000 KBps。

</dd> </dl> </dd> <dt>

*頻寬* \[在\]
</dt> <dd>

指定連接頻寬。

</dd> <dt>

*rtt* \[在\]
</dt> <dd>

指定連接延遲。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8<br/>                                                                   |
| 最低支援的伺服器<br/> | Windows Server 2012<br/>                                                         |
| 類型程式庫<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IMsTscAxEvents 定義為336d5562-efa8-482e-8cb3-c5c0fc7a7db6<br/>           |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMsTscAxEvents**](imstscaxevents-interface.md)
</dt> </dl>

 

 





