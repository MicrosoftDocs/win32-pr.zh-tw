---
title: 'INapSoHConstructor AppendAttribute 方法 (NapProtocol .h) '
description: 將 TLV 新增至 SoH 緩衝區的結尾。
ms.assetid: 5706ceaa-757f-49d2-90e0-011415853875
keywords:
- AppendAttribute 方法 NAP
- AppendAttribute 方法 NAP，INapSoHConstructor 介面
- INapSoHConstructor 介面 NAP，AppendAttribute 方法
topic_type:
- apiref
api_name:
- INapSoHConstructor.AppendAttribute
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc10fad9c775d324822700b77afed4e65a798db6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508528"
---
# <a name="inapsohconstructorappendattribute-method"></a>INapSoHConstructor：： AppendAttribute 方法

> [!Note]  
> 從 Windows 10 開始，無法使用網路存取保護平臺

 

**INapSoHConstructor：： AppendAttribute** 方法會將 TLV 新增至 SoH 緩衝區的結尾。

## <a name="syntax"></a>語法


```C++
HRESULT AppendAttribute(
  [in]       SoHAttributeType  type,
  [in] const SoHAttributeValue *value
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*類型* \[在\]
</dt> <dd>

[**SoHAttributeType**](sohattributetype-enum.md)列舉，指出新的 TLV 的屬性類型。

</dd> <dt>

*值* \[在\]
</dt> <dd>

[**SoHAttributeValue**](sohattributevalue-union.md)結構的指標，其中包含新的 TLV 的值。

</dd> </dl>

## <a name="return-value"></a>傳回值

也可能傳回其他 COM 特定的錯誤碼。



| 傳回碼                                                                                     | Description                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> </dl>           | 作業成功。<br/>                                    |
| <dl> <dt>**E \_ACCESSDENIED**</dt> </dl> | 許可權錯誤，拒絕存取。<br/>                       |
| <dl> <dt>**E \_OUTOFMEMORY**</dt> </dl>  | 系統資源限制，無法執行操作。<br/> |



 

## <a name="remarks"></a>備註

不能使用此函式來新增 [**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md) 的 TLV。 它會新增為 [**INapSoHConstructor：： Initialize**](inapsohconstructor-initialize-method.md) 到新建立之 SOH 封包的第一個 TLV。

附加 Nap 系統將使用的屬性時，不應以任何方式加密或修改。 如果 HealthEntity 需要加密/完整性檢查 (Mac) 私用資訊，它只應包含在 [**sohAttributeTypeVendorSpecific**](sohattributetype-enum.md) 屬性中。

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

 

 





