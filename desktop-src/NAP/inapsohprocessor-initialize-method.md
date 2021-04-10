---
title: 'INapSoHProcessor Initialize 方法 (NapProtocol .h) '
description: 初始化通訊協定封包和 SoH 處理器系統。 這個方法必須剛好呼叫一次。
ms.assetid: 4fccc847-3c4d-4fc5-935d-28fb2964a9be
keywords:
- Initialize 方法 NAP
- Initialize 方法 NAP，INapSoHProcessor 介面
- INapSoHProcessor 介面 NAP，Initialize 方法
topic_type:
- apiref
api_name:
- INapSoHProcessor.Initialize
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01ff3a32bb213caf19964ccea8175a43e5016f08
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934376"
---
# <a name="inapsohprocessorinitialize-method"></a>INapSoHProcessor：： Initialize 方法

> [!Note]  
> 從 Windows 10 開始，無法使用網路存取保護平臺

 

**INapSoHProcessor：： Initialize** 方法會初始化通訊協定封包和 SoH 處理器系統。 這個方法必須剛好呼叫一次。

## <a name="syntax"></a>語法


```C++
HRESULT Initialize(
  [in]  const SoH                  *soh,
  [in]        BOOL                 isRequest,
  [out]       SystemHealthEntityId *id
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*soh* \[在\]
</dt> <dd>

要處理的 [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) 封包指標。

</dd> <dt>

*isRequest* \[在\]
</dt> <dd>

如果封包是 [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) ，則 **布林****值為 TRUE** ，如果是 **SoHResponse**，則為 **FALSE** 。

</dd> <dt>

*識別碼* \[ 輸出\]
</dt> <dd>

唯一的 [SystemHealthEntityId](nap-datatypes.md) ，其中包含用來建立封包之 SHA 或 SHV 的識別碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

也可能傳回其他 COM 特定的錯誤碼。



| 傳回碼                                                                                            | Description                                                        |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> </dl>                  | 作業成功。<br/>                                    |
| <dl> <dt>**E \_ACCESSDENIED**</dt> </dl>        | 許可權錯誤，拒絕存取。<br/>                       |
| <dl> <dt>**E \_OUTOFMEMORY**</dt> </dl>         | 系統資源限制，無法執行操作。<br/> |
| <dl> <dt>**NAP \_ E \_ 不正確封 \_ 包**</dt> </dl> | SoH 封包無效。<br/>                              |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                             |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                       |
| 標頭<br/>                   | <dl> <dt>NapProtocol。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapProtocol .idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qutil.dll</dt> </dl>       |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**INapSoHProcessor**](inapsohprocessor.md)
</dt> </dl>

 

 





