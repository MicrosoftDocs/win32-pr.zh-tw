---
title: 'INapComponentConfig3 >newconfig.json 方法 (NapCommon .h) '
description: 是由系統健康狀態驗證 (Shv 所執行) ，以提供一種方式來建立特定設定識別碼的設定資料。
ms.assetid: cea762d3-815d-4034-94c1-5fa9a859cce8
keywords:
- '>newconfig.json 方法 NAP'
- '>newconfig.json 方法 NAP，INapComponentConfig3 介面'
- INapComponentConfig3 介面 NAP，>newconfig.json 方法
topic_type:
- apiref
api_name:
- INapComponentConfig3.NewConfig
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 924204068dbb66b22cc06d28966511d8922e0068
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094247"
---
# <a name="inapcomponentconfig3newconfig-method"></a>INapComponentConfig3：： >newconfig.json 方法

> [!Note]  
> 從 Windows 10 開始，無法使用網路存取保護平臺

 

**>newconfig.json** 方法是由系統健康狀態驗證 (shv) 來提供一種方法，以建立特定設定識別碼的設定資料。 呼叫此函式時，SHV 必須配置新的設定資料，並填入預設設定資料的複本。

## <a name="syntax"></a>語法


```C++
HRESULT NewConfig(
   UINT32 configID
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*configID* 
</dt> <dd>

表示設定的值。 網路原則伺服器 (NPS) 服務指派 *ConfigID* ，且在 SHV 內是唯一的。

</dd> </dl>

## <a name="return-value"></a>傳回值

根據此操作的結果，傳回下列其中一個錯誤碼。



| 傳回碼                                                                                                 | Description                                                                                   |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> </dl>                       | 作業成功。<br/>                                                       |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>                | *ConfigID* 為 0 (保留給預設設定) 的值。<br/>                  |
| <dl> <dt>**NAP \_ E \_ SHV 設定已 \_ \_ 存在**</dt> </dl> | *ConfigID* 已經存在。 NPS 已知的識別碼清單與 SHV 不同。<br/> |



 

## <a name="remarks"></a>備註

**>newconfig.json** 建立新的設定之後，應該使用 [**GetConfigFromID**](inapcomponentconfig3-getconfigfromid.md)、 [**InvokeUIFromConfigBlob**](inapcomponentconfig2-invokeuifromconfigblob.md)和 [**SetConfigToID**](inapcomponentconfig3-setconfigtoid.md)方法來視需要變更設定。

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

 

 





