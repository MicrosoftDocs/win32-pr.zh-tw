---
title: IMsTscAxEvents OnChannelReceivedData 方法
description: 當用戶端在可編寫腳本的虛擬通道上接收資料時呼叫。
ms.assetid: 38e6c33c-6a79-4760-818e-445e33d8e0ec
ms.tgt_platform: multiple
keywords:
- OnChannelReceivedData 方法遠端桌面服務
- OnChannelReceivedData 方法遠端桌面服務，IMsTscAxEvents 介面
- IMsTscAxEvents 介面遠端桌面服務，OnChannelReceivedData 方法
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnChannelReceivedData
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72f411eae7e03f134f4adfd6fdc6108634e4e58c06bb8645e9f97f27e8489a3e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120125188"
---
# <a name="imstscaxeventsonchannelreceiveddata-method"></a>IMsTscAxEvents：： OnChannelReceivedData 方法

當用戶端在可編寫腳本的虛擬通道上接收資料時呼叫。

## <a name="syntax"></a>語法


```C++
void OnChannelReceivedData(
  [in] BSTR chanName,
  [in] BSTR data
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*chanName* \[在\]
</dt> <dd>

收到資料的虛擬通道名稱。 這個名稱符合對 [**IMsTscAx：： CreateVirtualChannels**](imstscax-createvirtualchannels.md)的呼叫所建立的其中一個通道。

</dd> <dt>

*資料* \[在\]
</dt> <dd>

在可編寫腳本的虛擬通道上收到的資料。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

如需此事件的詳細資訊，請參閱 [使用遠端桌面網頁連線執行可編寫腳本的虛擬通道](implementing-scriptable-virtual-channels-using-remote-desktop-web-connection.md) 。

如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                               |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                         |
| 類型程式庫<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IMsTscAxEvents 定義為336d5562-efa8-482e-8cb3-c5c0fc7a7db6<br/>           |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMsTscAxEvents**](imstscaxevents-interface.md)
</dt> </dl>

 

 





