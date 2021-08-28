---
title: 'IWMDRMLicense GetLicense 方法 (Wmdrmsdk .h) '
description: GetLicense 方法會以 XML 或 XMR 資料的形式來捕獲授權。
ms.assetid: 63317841-fd13-4e83-8b99-e3cab1405050
keywords:
- GetLicense 方法 windows Media 格式
- GetLicense 方法 windows Media Format，IWMDRMLicense 介面
- IWMDRMLicense 介面 windows Media Format，GetLicense 方法
topic_type:
- apiref
api_name:
- IWMDRMLicense.GetLicense
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09b303c3280b42858bb319bb49baa209c1f99cdac819a719743db403bfdc08ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119585398"
---
# <a name="iwmdrmlicensegetlicense-method"></a>IWMDRMLicense：： GetLicense 方法

**GetLicense** 方法會以 XML 或 XMR 資料的形式來捕獲授權。

## <a name="syntax"></a>語法


```C++
HRESULT GetLicense(
  [out] BYTE  **ppbLicense,
  [out] DWORD *pcbLicense,
  [out] DWORD *pdwLicenseType
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ppbLicense* \[擴展\]
</dt> <dd>

接收授權。

</dd> <dt>

*pcbLicense* \[擴展\]
</dt> <dd>

接收授權的大小。

</dd> <dt>

*pdwLicenseType* \[擴展\]
</dt> <dd>

接收傳回的授權類型。 此值會設定為下表中的其中一個常數。



| 常數                  | 描述                            |
|---------------------------|----------------------------------------|
| WMDRM \_ 授權 \_ 類型 \_ XML | 取出的授權會格式化為 XML。 |
| WMDRM \_ 授權 \_ 類型 \_ XMR | 已取出的授權格式為 XMR。 |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回 **HRESULT**。 可能的值包括 (但不限於) 下表中的這些值。



| 傳回碼                                                                          | 描述                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl> | 此方法已成功。<br/> |



 

## <a name="remarks"></a>備註

無。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Wmdrmsdk。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>Wmdrmsdk .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**GetLicenseProperty**](iwmdrmlicense-getlicenseproperty.md)
</dt> <dt>

[**IWMDRMLicense 介面**](iwmdrmlicense.md)
</dt> </dl>

 

 





