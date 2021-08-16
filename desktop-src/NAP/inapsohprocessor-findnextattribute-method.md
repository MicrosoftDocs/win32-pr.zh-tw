---
title: 'INapSoHProcessor FindNextAttribute 方法 (NapProtocol .h) '
description: 尋找 SoHAttributeType 所指定類型之下一個屬性的位置 (索引) 。
ms.assetid: 0ff94a32-ece8-4a89-9ee9-93c5e14dfb6c
keywords:
- FindNextAttribute 方法 NAP
- FindNextAttribute 方法 NAP，INapSoHProcessor 介面
- INapSoHProcessor 介面 NAP，FindNextAttribute 方法
topic_type:
- apiref
api_name:
- INapSoHProcessor.FindNextAttribute
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4425707487994904d1bd2a622cd1ab66f286469c93e80a8eb01e71c0319426ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118939575"
---
# <a name="inapsohprocessorfindnextattribute-method"></a>INapSoHProcessor：： FindNextAttribute 方法

> [!Note]  
> 從 Windows 10 開始，無法使用網路存取保護平臺

 

**INapSoHProcessor：： FindNextAttribute** 方法會尋找 *SoHAttributeType* 所指定類型之下一個屬性的位置 (索引) 。

## <a name="syntax"></a>語法


```C++
HRESULT FindNextAttribute(
  [in]  UINT16           fromLocation,
  [in]  SoHAttributeType type,
  [out] UINT16           *attributeLocation
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*fromLocation* \[在\]
</dt> <dd>

在健全狀況聲明中 (索引) 的起始位置 (SoH) 封包，以開始進行屬性搜尋。 這個值必須介於0到 (**numAttrib** -1) ，其中 **NumAttrib** 是使用 [**INapSoHProcessor：： GetNumberOfAttributes**](inapsohprocessor-getnumberofattributes-method.md)抓取。

> [!Note]  
> SoH 封包使用以0為基底的屬性索引。

 

</dd> <dt>

*類型* \[在\]
</dt> <dd>

[**SoHAttributeType**](sohattributetype-enum.md)結構，其中包含要尋找的屬性型別。

</dd> <dt>

*attributeLocation* \[擴展\]
</dt> <dd>

指標，其中包含從索引 *FromLocation* *SoHAttributeType* 類型之第一個屬性之 SoH 封包中的位置 (索引) 。

</dd> </dl>

## <a name="return-value"></a>傳回值

也可能傳回其他 COM 特定的錯誤碼。



| 傳回碼                                                                                            | Description                                                        |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> </dl>                  | 作業成功。<br/>                                    |
| <dl> <dt>**E \_ACCESSDENIED**</dt> </dl>        | 許可權錯誤，拒絕存取。<br/>                       |
| <dl> <dt>**E \_OUTOFMEMORY**</dt> </dl>         | 系統資源限制，無法執行操作。<br/> |
| <dl> <dt>**\_ \_ \_ 找不到錯誤檔案**</dt> </dl> | 找不到屬性。<br/>                                    |



 

## <a name="remarks"></a>備註

**FindNextAttribute** 方法會從 *fromLocation* 和更新版本所指定的索引中搜尋 *SoHAttributeType* 類型的屬性，直到找到相符的屬性為止。 如果找不到相符項，則會傳回 **錯誤 \_ \_ \_** 檔案。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                             |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                       |
| 標頭<br/>                   | <dl> <dt>NapProtocol。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapProtocol .idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qutil.dll</dt> </dl>       |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**INapSoHProcessor**](inapsohprocessor.md)
</dt> </dl>

 

 





