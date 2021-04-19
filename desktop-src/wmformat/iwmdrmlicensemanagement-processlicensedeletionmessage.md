---
title: 'IWMDRMLicenseManagement ProcessLicenseDeletionMessage 方法 (Wmdrmsdk .h) '
description: ProcessLicenseDeletion 方法會刪除針對原始以其他內容保護系統保護的內容所匯入的授權。
ms.assetid: 478dd156-feb8-4eda-9d3a-35db3e65c227
keywords:
- ProcessLicenseDeletionMessage 方法 windows Media 格式
- ProcessLicenseDeletionMessage 方法 windows Media Format，IWMDRMLicenseManagement 介面
- IWMDRMLicenseManagement 介面 windows Media Format，ProcessLicenseDeletionMessage 方法
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.ProcessLicenseDeletionMessage
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9338c1bc4ef78e658cc25ab95f5c50556af3ed09
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978690"
---
# <a name="iwmdrmlicensemanagementprocesslicensedeletionmessage-method"></a>IWMDRMLicenseManagement：:P rocessLicenseDeletionMessage 方法

**ProcessLicenseDeletion** 方法會刪除針對原始以其他內容保護系統保護的內容所匯入的授權。

## <a name="syntax"></a>語法


```C++
HRESULT ProcessLicenseDeletionMessage(
  [in] BSTR bstrDeletionMessage
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*bstrDeletionMessage* \[在\]
</dt> <dd>

識別要刪除之授權的訊息。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回 **HRESULT**。 可能的值包括 (但不限於) 下表中的這些值。



| 傳回碼                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl> | 此方法已成功。<br/> |



 

## <a name="remarks"></a>備註

無。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Wmdrmsdk。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IWMDRMLicenseManagement 介面**](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





