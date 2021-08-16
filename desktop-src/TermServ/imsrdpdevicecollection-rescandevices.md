---
title: IMsRdpDeviceCollection RescanDevices 方法
description: 重新整理集合中的物件清單。 |IMsRdpDeviceCollection RescanDevices 方法
ms.assetid: 2e2a959d-0a1d-4aca-9daf-3c24fb9b3b08
ms.tgt_platform: multiple
keywords:
- RescanDevices 方法遠端桌面服務
- RescanDevices 方法遠端桌面服務，IMsRdpDeviceCollection 介面
- IMsRdpDeviceCollection 介面遠端桌面服務，RescanDevices 方法
topic_type:
- apiref
api_name:
- IMsRdpDeviceCollection.RescanDevices
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d62011697b21171f8de326689ca35195ad4057e2e6edd01a5159fcf89c32d0f8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959238"
---
# <a name="imsrdpdevicecollectionrescandevices-method"></a>IMsRdpDeviceCollection：： RescanDevices 方法

重新整理集合中的物件清單。

## <a name="syntax"></a>語法


```C++
HRESULT RescanDevices(
  [in] VARIANT_BOOL vboolDynRedir
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*vboolDynRedir* \[在\]
</dt> <dd>

預設會套用至任何新探索到的裝置或磁片磁碟機的重新導向狀態。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果方法成功，則會傳回 **S \_ OK** 。 任何其他 **HRESULT** 值都表示呼叫失敗。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                  |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                            |
| 類型程式庫<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>    |
| IID<br/>                      | IID \_ IMsRdpDeviceCollection 定義為 56540617-d281-488c-8738-6a8fdf64a118<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMsRdpDeviceCollection**](imsrdpdevicecollection.md)
</dt> </dl>

 

 





