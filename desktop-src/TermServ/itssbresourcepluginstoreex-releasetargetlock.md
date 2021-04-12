---
title: ITsSbResourcePluginStoreEx ReleaseTargetLock 方法
description: 釋放目標的鎖定。
ms.assetid: ab2ae9f3-2d38-4b31-9889-58297c574bd4
ms.tgt_platform: multiple
keywords:
- ReleaseTargetLock 方法遠端桌面服務
- ReleaseTargetLock 方法遠端桌面服務，ITsSbResourcePluginStoreEx 介面
- ITsSbResourcePluginStoreEx 介面遠端桌面服務，ReleaseTargetLock 方法
topic_type:
- apiref
api_name:
- ITsSbResourcePluginStoreEx.ReleaseTargetLock
api_location:
- SbTsV.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8fbc34bdb27e40316ea1271bf0faa5d8c6b0abfb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104298"
---
# <a name="itssbresourcepluginstoreexreleasetargetlock-method"></a>ITsSbResourcePluginStoreEx：： ReleaseTargetLock 方法

釋放目標的鎖定。

## <a name="syntax"></a>語法


```C++
HRESULT ReleaseTargetLock(
  [in] IUnknown *pContext
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pCoNtext* \[在\]
</dt> <dd>

[**AcquireTargetLock**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-acquiretargetlock)方法所傳回之內容的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

只有在已安裝 [KB3091411](https://support.microsoft.com/kb/3091411) 的 Windows Server 2012 R2 上，才可在 [**ITsSbResourcePluginStoreEx**](itssbresourcepluginstoreex.md) 介面中使用此方法。 從 Windows Server 2016 開始， [**ITsSbResourcePluginStore**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore) 介面上可以使用這個方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                                     |
| 最低支援的伺服器<br/> | Windows Server 2012 R2<br/>                                                             |
| 伺服器支援結束<br/>    | Windows Server 2012 R2<br/>                                                             |
| Idl<br/>                      | <dl> <dt>SbTsV .idl</dt> </dl>          |
| IID<br/>                      | IID \_ ITsSbResourcePluginStoreEx 定義為80b83ffd-625d-11e5-bea1-a0481c7e9064<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ITsSbResourcePluginStoreEx**](itssbresourcepluginstoreex.md)
</dt> </dl>

 

 





