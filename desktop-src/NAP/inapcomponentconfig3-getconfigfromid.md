---
title: 'INapComponentConfig3 GetConfigFromID 方法 (NapCommon .h) '
description: 是由系統健康狀態驗證 (Shv 所執行) ，以提供一種方式來取得特定設定識別碼的設定資料。
ms.assetid: 5c91681d-16d6-42f3-b1e0-c4b6e7561a73
keywords:
- GetConfigFromID 方法 NAP
- GetConfigFromID 方法 NAP，INapComponentConfig3 介面
- INapComponentConfig3 介面 NAP，GetConfigFromID 方法
topic_type:
- apiref
api_name:
- INapComponentConfig3.GetConfigFromID
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ce3a0e20f19c73271cdcba4070972649fe25aea
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685767"
---
# <a name="inapcomponentconfig3getconfigfromid-method"></a>INapComponentConfig3：： GetConfigFromID 方法

> [!Note]  
> 從 Windows 10 開始，無法使用網路存取保護平臺

 

**GetConfigFromID** 方法是由系統健康狀態驗證 (shv) 來提供方法，以取得特定設定識別碼的設定資料。

## <a name="syntax"></a>語法


```C++
HRESULT GetConfigFromID(
  [in]  UINT32 configID,
  [out] UINT16 *count,
  [out] BYTE   **outdata
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*configID* \[在\]
</dt> <dd>

表示設定的值。 如果 *ConfigID* 為 **0**，SHV 應該會傳回 *outdata* 中的預設設定資料。

</dd> <dt>

*計數* \[擴展\]
</dt> <dd>

*Outdata* 中傳回的設定資料大小（以位元組為單位）。

</dd> <dt>

*outdata* \[擴展\]
</dt> <dd>

傳回時，包含 *ConfigID* 所代表之設定資料的位元組陣列。

</dd> </dl>

## <a name="return-value"></a>傳回值

根據此操作的結果，傳回下列其中一個錯誤碼。



| 傳回碼                                                                                                    | Description                             |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <dt>**S \_確定**</dt> </dl>                          | 作業成功。<br/> |
| <dl> <dt>**\_ \_ \_ \_ \_ 找不到 NAP E SHV 設定**</dt> </dl> | 找不到 *ConfigID* 。<br/>  |



 

## <a name="remarks"></a>備註

在呼叫這個方法之前，必須先使用 [**>newconfig.json**](inapcomponentconfig3-newconfig.md) 方法來配置 *ConfigID* 的設定資料。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                                |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 R2 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>NapCommon。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapCommon .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**INapComponentConfig3**](inapcomponentconfig3.md)
</dt> </dl>

 

 





