---
title: ITsSbResourcePluginStoreEx AcquireTargetLock 方法
description: 鎖定目標。
ms.assetid: 76707f1d-1f13-4d81-8954-2acf05cda2cd
ms.tgt_platform: multiple
keywords:
- AcquireTargetLock 方法遠端桌面服務
- AcquireTargetLock 方法遠端桌面服務，ITsSbResourcePluginStoreEx 介面
- ITsSbResourcePluginStoreEx 介面遠端桌面服務，AcquireTargetLock 方法
topic_type:
- apiref
api_name:
- ITsSbResourcePluginStoreEx.AcquireTargetLock
api_location:
- SbTsV.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c18be0a544ebcea2d2cecb40dcea3a08e4bd35b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094104"
---
# <a name="itssbresourcepluginstoreexacquiretargetlock-method"></a>ITsSbResourcePluginStoreEx：： AcquireTargetLock 方法

鎖定目標。

## <a name="syntax"></a>語法


```C++
HRESULT AcquireTargetLock(
  [in]  BSTR     targetName,
  [in]  DWORD    dwTimeout,
  [out] IUnknown **ppContext
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*targetName* \[在\]
</dt> <dd>

要鎖定之目標的名稱。

</dd> <dt>

*dwTimeout* \[在\]
</dt> <dd>

作業的執行時間（以毫秒為單位）。

</dd> <dt>

*ppCoNtext* \[擴展\]
</dt> <dd>

傳回鎖定內容的指標。 若要釋放鎖定，請提供此指標給 [**ReleaseTargetLock**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-releasetargetlock) 方法。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

取得鎖定之後，會假設呼叫的執行緒具有目標物件的獨佔存取權，因此不會在同一部機器內 (其他執行緒) 可以更新它。 因此，呼叫的執行緒必須在對目標物件進行必要的更新時，立即呼叫 [**ReleaseTargetLock**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-releasetargetlock) 方法。

> [!IMPORTANT]
> 如果部署中有一個以上的連接代理程式，此鎖定並不會完全防止外部修改目標物件。 呼叫執行緒必須做好準備，才能正常地處理失敗，然後重試目標更新。

 

此方法可在已安裝 [KB3091411](https://support.microsoft.com/kb/3091411) 的 Windows Server 2012 R2 上使用，並安裝在 [**ITsSbResourcePluginStoreEx**](itssbresourcepluginstoreex.md) 介面中。

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

 

 





