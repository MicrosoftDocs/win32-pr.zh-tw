---
title: 'IWMDRMLicenseManagement CreateLicenseEnumeration 方法 (Wmdrmsdk .h) '
description: CreateLicenseEnumeration 方法會建立授權列舉值物件，讓您可以在本機授權存放區中取得授權的相關資訊。
ms.assetid: 48da1ef4-89bc-4cba-b5c9-0e202eb2986f
keywords:
- CreateLicenseEnumeration 方法 windows Media 格式
- CreateLicenseEnumeration 方法 windows Media Format，IWMDRMLicenseManagement 介面
- IWMDRMLicenseManagement 介面 windows Media Format，CreateLicenseEnumeration 方法
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.CreateLicenseEnumeration
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6bb75d21cc640da39c3679ac118ead629b24f719
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106975968"
---
# <a name="iwmdrmlicensemanagementcreatelicenseenumeration-method"></a>IWMDRMLicenseManagement：： CreateLicenseEnumeration 方法

**CreateLicenseEnumeration** 方法會建立授權列舉值物件，讓您可以在本機授權存放區中取得授權的相關資訊。

## <a name="syntax"></a>語法


```C++
HRESULT CreateLicenseEnumeration(
  [in]  WMDRM_LICENSE_FILTER *pLicenseFilter,
  [out] IWMDRMLicense        **pEnumerator
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pLicenseFilter* \[在\]
</dt> <dd>

[**WMDRM \_ 授權 \_ 篩選**](wmdrm-license-filter.md)結構的指標，其中包含列舉值中授權清單的篩選參數。

</dd> <dt>

*pEnumerator* \[擴展\]
</dt> <dd>

此指標會接收新建立的授權列舉值物件之 [**IWMDRMLicense**](iwmdrmlicense.md) 介面的位址。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回 **HRESULT**。 可能的值包括 (但不限於) 下表中的這些值。



| 傳回碼                                                                                                | Description                                              |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**NS \_ E \_ DRM \_ RIV \_ 太 \_ 小**</dt> </dl> | 需要更新的內容撤銷清單。<br/> |
| <dl> <dt>**S \_ 確定**</dt> </dl>                       | 此方法已成功。<br/>                         |



 

## <a name="remarks"></a>備註

無。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Wmdrmsdk。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>Wmdrmsdk .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**列舉本機授權存放區中的授權**](enumerating-licenses-in-the-local-license-store.md)
</dt> <dt>

[**IWMDRMLicenseManagement 介面**](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





