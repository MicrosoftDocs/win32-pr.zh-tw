---
title: 'IWMDRMLicenseManagement StoreLicense 方法 (Wmdrmsdk .h) '
description: StoreLicense 方法包含在本機授權存放區的本機 DRM 子系統以外產生的授權。
ms.assetid: 2190ff8c-8969-4f03-9f90-331bff8f4da2
keywords:
- StoreLicense 方法 windows Media 格式
- StoreLicense 方法 windows Media Format，IWMDRMLicenseManagement 介面
- IWMDRMLicenseManagement 介面 windows Media Format，StoreLicense 方法
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.StoreLicense
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcfde6347e099ceb9fc168e1183cbd62c90f9b9c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990120"
---
# <a name="iwmdrmlicensemanagementstorelicense-method"></a>IWMDRMLicenseManagement：： StoreLicense 方法

**StoreLicense** 方法包含在本機授權存放區的本機 DRM 子系統以外產生的授權。

## <a name="syntax"></a>語法


```C++
HRESULT StoreLicense(
  [in] BSTR bstrLicenseResponse
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*bstrLicenseResponse* \[在\]
</dt> <dd>

要解碼並新增至本機授權存放區的授權回應字串。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回 **HRESULT**。 可能的值包括 (但不限於) 下表中的這些值。



| 傳回碼                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl> | 此方法已成功。<br/> |



 

## <a name="remarks"></a>備註

您可以使用此方法，將您建立的 XMR 授權新增至本機授權存放區。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Wmdrmsdk。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>Wmdrmsdk .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IWMDRMLicenseManagement 介面**](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





