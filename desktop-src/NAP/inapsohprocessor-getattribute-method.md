---
title: 'INapSoHProcessor GetAttribute 方法 (NapProtocol .h) '
description: 在指定屬性位置時，抓取屬性型別和值。
ms.assetid: 0d7bc655-428b-4a31-b03f-445e80a6d194
keywords:
- GetAttribute 方法 NAP
- GetAttribute 方法 NAP，INapSoHProcessor 介面
- INapSoHProcessor 介面 NAP，GetAttribute 方法
topic_type:
- apiref
api_name:
- INapSoHProcessor.GetAttribute
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ed2d7d9cbafa5a44e0f6c24f4c42959c456722a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967315"
---
# <a name="inapsohprocessorgetattribute-method"></a>INapSoHProcessor：： GetAttribute 方法

> [!Note]  
> 從 Windows 10 開始，無法使用網路存取保護平臺

 

**INapSoHProcessor：： GetAttribute** 方法會在指定屬性位置時，抓取屬性型別和值。

## <a name="syntax"></a>語法


```C++
HRESULT GetAttribute(
  [in]  UINT16            attributeLocation,
  [out] SoHAttributeType  *type,
  [out] SoHAttributeValue **value
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*attributeLocation* \[在\]
</dt> <dd>

要抓取其類型和值的屬性位置 (索引) 。 *AttributeLocation* 的值會從先前的 [**INapSoHProcessor：： FindNextAttribute**](inapsohprocessor-findnextattribute-method.md)呼叫傳回。

</dd> <dt>

*類型* \[擴展\]
</dt> <dd>

[**SoHAttributeType**](sohattributetype-enum.md)結構的指標，此結構會指定屬性在 *值* 中的型別。

</dd> <dt>

*值* \[擴展\]
</dt> <dd>

[**SoHAttributeValue**](sohattributevalue-union.md)結構指標的指標，該結構包含屬性的值，如 *類型* 所定義。

</dd> </dl>

## <a name="return-value"></a>傳回值

也可能傳回其他 COM 特定的錯誤碼。



| 傳回碼                                                                                     | Description                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> </dl>           | 作業成功。<br/>                                    |
| <dl> <dt>**E \_ACCESSDENIED**</dt> </dl> | 許可權錯誤，拒絕存取。<br/>                       |
| <dl> <dt>**E \_OUTOFMEMORY**</dt> </dl>  | 系統資源限制，無法執行操作。<br/> |



 

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

 

 





