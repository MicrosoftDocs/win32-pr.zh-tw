---
description: 設定在虛擬機器中執行之應用程式的健全狀況狀態。
ms.assetid: 012190CA-9CBF-47B6-9C5D-F75D73B0499B
title: IVmApplicationHealthMonitor：： SetApplicationState 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IVmApplicationHealthMonitor.SetApplicationState
api_type:
- COM
api_location:
- VmApplicationHealthMonitor.idl
ms.openlocfilehash: 785b5e6254bde84497f4fcf72d15b20ff16ccd7319ecc3631c0864b3e4992655
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118392353"
---
# <a name="ivmapplicationhealthmonitorsetapplicationstate-method"></a>IVmApplicationHealthMonitor：： SetApplicationState 方法

設定在虛擬機器中執行之應用程式的健全狀況狀態。

## <a name="syntax"></a>語法


```C++
HRESULT SetApplicationState(
  [in] BSTR              Id,
  [in] BSTR              Name,
  [in] APPLICATION_STATE State
);
```



## <a name="parameters"></a>參數

<dl> <dt>

 \[ 中的識別碼\]
</dt> <dd>

識別應用程式之 **GUID** 的 **BSTR** 標記法。 呼叫應用程式必須負責建立和維護其用於受監視應用程式的識別碼。

</dd> <dt>

*名稱* \[在\]
</dt> <dd>

應用程式的顯示名稱。 此名稱會用於狀態變更的參考事件記錄專案中。

</dd> <dt>

*狀態* \[在\]
</dt> <dd>

[**應用程式 \_ 狀態**](application-state.md)列舉值，這個值會指定應用程式的新健全狀況狀態。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

在虛擬機器中執行之應用程式的狀態會反映在 \[ \] [**Msvm \_ HeartbeatComponent**](msvm-heartbeatcomponent.md)類別的 OperationalStatus 1 屬性值中。

若要使用這個程式設計項目，Windows 8 的整合元件必須安裝在執行應用程式的虛擬機器上。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[僅限桌面應用程式\]<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2012 \[僅限桌面應用程式\]<br/>                                                      |
| 版本<br/>                  | Windows 8 的整合元件<br/>                                                           |
| Idl<br/>                      | <dl> <dt>VmApplicationHealthMonitor .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IVmApplicationHealthMonitor**](ivmapplicationhealthmonitor.md)
</dt> </dl>

 

 




