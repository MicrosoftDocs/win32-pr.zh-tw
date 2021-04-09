---
title: 'INapSoHConstructor Initialize 方法 (NapProtocol .h) '
description: 初始化 NAP 系統中的 SoH 通訊協定封包。
ms.assetid: 1678b677-c8c8-465c-a412-9b929e39bbac
keywords:
- Initialize 方法 NAP
- Initialize 方法 NAP，INapSoHConstructor 介面
- INapSoHConstructor 介面 NAP，Initialize 方法
topic_type:
- apiref
api_name:
- INapSoHConstructor.Initialize
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eab8d6b27547be6e7c7e9abb59f7edb7b49e716e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934303"
---
# <a name="inapsohconstructorinitialize-method"></a>INapSoHConstructor：： Initialize 方法

> [!Note]  
> 從 Windows 10 開始，無法使用網路存取保護平臺

 

**INapSoHConstructor：： Initialize** 方法會初始化 NAP 系統中的 SoH 通訊協定封包。

## <a name="syntax"></a>語法


```C++
HRESULT Initialize(
  [in] SystemHealthEntityId id,
  [in] BOOL                 isRequest
);
```



## <a name="parameters"></a>參數

<dl> <dt>

 \[ 中的識別碼\]
</dt> <dd>

唯一的 [SystemHealthEntityId](nap-datatypes.md) ，其中包含正在建立封包的 SHA 或 SHV 識別碼。

</dd> <dt>

*isRequest* \[在\]
</dt> <dd>

如果封包是 [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) ，則 **布林****值為 TRUE** ，如果是 **SoHResponse**，則為 **FALSE** 。

</dd> </dl>

## <a name="return-value"></a>傳回值

也可能傳回其他 COM 特定的錯誤碼。



| 傳回碼                                                                                     | Description                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> </dl>           | 作業成功。<br/>                                   |
| <dl> <dt>**E \_ACCESSDENIED**</dt> </dl> | 許可權錯誤，拒絕存取。<br/>                       |
| <dl> <dt>**E \_OUTOFMEMORY**</dt> </dl>  | 系統資源限制，無法執行操作。<br/> |



 

## <a name="remarks"></a>備註

每個封包都必須剛好呼叫這個方法一次。

在 *識別碼* 中指定的 [SystemHealthEntityId](nap-datatypes.md)是新建立的 SOH 封包中的第一個 TLV，而且具有屬性類型 [**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md)。

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

[**INapSoHConstructor**](inapsohconstructor.md)
</dt> </dl>

 

 





