---
title: 'IWMDRMLicense GetLicenseProperty 方法 (Wmdrmsdk .h) '
description: GetLicenseProperty 方法會從目前的授權抓取屬性。
ms.assetid: 5431f849-b37e-40b7-8bdb-ee30948aeff1
keywords:
- GetLicenseProperty 方法 windows Media 格式
- GetLicenseProperty 方法 windows Media Format，IWMDRMLicense 介面
- IWMDRMLicense 介面 windows Media Format，GetLicenseProperty 方法
topic_type:
- apiref
api_name:
- IWMDRMLicense.GetLicenseProperty
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 167fc0aa050765700805b4339e68142fa5d1eb7fc99e010c7393095dd9aa5c0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119084838"
---
# <a name="iwmdrmlicensegetlicenseproperty-method"></a>IWMDRMLicense：： GetLicenseProperty 方法

**GetLicenseProperty** 方法會從目前的授權抓取屬性。

## <a name="syntax"></a>語法


```C++
HRESULT GetLicenseProperty(
  [in]  BSTR        bstrName,
  [out] PROPVARIANT *ppropVariant
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*bstrName* \[在\]
</dt> <dd>

要取得之屬性的名稱。 設定為下表中的其中一個常數：



| 常數                   | 描述                                                                                                          |
|----------------------------|----------------------------------------------------------------------------------------------------------------------|
| g \_ wszWMDRMNet \_ 撤銷 | 用來取得目前授權的網路裝置撤銷清單 Windows 媒體 DRM。                        |
| g \_ wszWMDRM \_ SAPLEVEL      | 使用可取得 (SAP) 層級所需的安全音訊路徑，以播放目前授權所涵蓋的內容。                |
| g \_ wszWMDRM \_ SAPRequired   | 使用來確定目前的授權是否需要使用 SAP 來播放內容。                               |
| g \_ wszWMDRM \_ SOURCEID      | 用來取得目前授權的來源識別碼。                                                            |
| g \_ wszWMDRM \_ 優先順序      | 使用以取得目前授權的優先權。 較高優先順序的授權會在較低優先順序的授權之前套用。 |
| g \_ wszWMDRM \_ UplinkID      | 用來取得目前授權所屬授權鏈中根授權的金鑰識別碼。                  |



 

</dd> <dt>

*ppropVariant* \[擴展\]
</dt> <dd>

接收屬性值。

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

[**GetLicense**](iwmdrmlicense-getlicense.md)
</dt> <dt>

[**IWMDRMLicense 介面**](iwmdrmlicense.md)
</dt> </dl>

 

 





