---
title: 'INapComponentConfig3 DeleteConfig 方法 (NapCommon .h) '
description: 是由系統健康狀態驗證 (Shv 所執行) ，以提供一種方式來刪除特定設定識別碼的設定資料。
ms.assetid: 9740c122-86c8-4b77-9268-faa90e84d8aa
keywords:
- DeleteConfig 方法 NAP
- DeleteConfig 方法 NAP，INapComponentConfig3 介面
- INapComponentConfig3 介面 NAP，DeleteConfig 方法
topic_type:
- apiref
api_name:
- INapComponentConfig3.DeleteConfig
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5a9b9a6838616f0892b45df34d9a7c5ed63ff16
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685769"
---
# <a name="inapcomponentconfig3deleteconfig-method"></a>INapComponentConfig3：:D eleteConfig 方法

> [!Note]  
> 從 Windows 10 開始，無法使用網路存取保護平臺

 

**DeleteConfig** 方法是由系統健康狀態驗證 (shv) 來提供一種方式，以刪除特定設定識別碼的設定資料。 刪除設定資料之後，可能會重複使用此識別碼。

## <a name="syntax"></a>語法


```C++
HRESULT DeleteConfig(
   UINT32 configID
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*configID* 
</dt> <dd>

值，表示要刪除的設定資料。

</dd> </dl>

## <a name="return-value"></a>傳回值

根據此操作的結果，傳回下列其中一個錯誤碼。



| 傳回碼                                                                                                    | Description                                                                  |
|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> </dl>                          | 作業成功。<br/>                                      |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>                   | *ConfigID* 為 0 (保留給預設設定) 的值。<br/> |
| <dl> <dt>**\_ \_ \_ \_ \_ 找不到 NAP E SHV 設定**</dt> </dl> | 找不到 *ConfigID* 。<br/>                                       |



 

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

 

 





