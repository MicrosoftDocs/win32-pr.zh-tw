---
title: 'IWMDRMSecurity GetRevocationDataVersion 方法 (Wmdrmsdk .h) '
description: GetRevocationDataVersion 方法會抓取本機存放區中憑證撤銷清單的版本號碼。
ms.assetid: 2fa13b38-02c2-4c81-938b-409cadca00fb
keywords:
- GetRevocationDataVersion 方法 windows Media 格式
- GetRevocationDataVersion 方法 windows Media Format，IWMDRMSecurity 介面
- IWMDRMSecurity 介面 windows Media Format，GetRevocationDataVersion 方法
topic_type:
- apiref
api_name:
- IWMDRMSecurity.GetRevocationDataVersion
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d139b2daf3f3bc6ad78beaa50e19c0141aecd5e8bedac2dd20582fb1536d9b74
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119930778"
---
# <a name="iwmdrmsecuritygetrevocationdataversion-method"></a>IWMDRMSecurity：： GetRevocationDataVersion 方法

**GetRevocationDataVersion** 方法會抓取本機存放區中憑證撤銷清單的版本號碼。

## <a name="syntax"></a>語法


```C++
HRESULT GetRevocationDataVersion(
  [in]  REFGUID   f_guidRevocationType,
  [out] ULONGLONG *f_pdwCRLVersion
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*f \_ guidRevocationType* \[ in\]
</dt> <dd>

指定撤銷清單類型的 GUID。 設定為下表中的其中一個常數。



| GUID 常數                 | 描述                                                                      |
|-------------------------------|----------------------------------------------------------------------------------|
| WMDRM \_ REVOCATIONTYPE \_ 應用程式    | 指定應用程式憑證撤銷清單。                           |
| WMDRM \_ REVOCATIONTYPE \_ 裝置 | 指定裝置憑證撤銷清單。                                |
| WMDRM \_ REVOCATIONTYPE \_ CARDEA | 指定網路裝置憑證撤銷清單的 Windows 媒體 DRM。 |



 

</dd> <dt>

*f \_ pdwCRLVersion* \[ 輸出\]
</dt> <dd>

接收版本號碼的變數。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回 **HRESULT**。 可能的值包括 (但不限於) 下表中的這些值。



| 傳回碼                                                                          | 描述                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl> | 此方法已成功。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Wmdrmsdk。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>Wmdrmsdk .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**自動化元件撤銷和更新**](automated-component-revocation-and-renewal.md)
</dt> <dt>

[**GetRevocationData**](iwmdrmsecurity-getrevocationdata.md)
</dt> <dt>

[**IWMDRMSecurity 介面**](iwmdrmsecurity.md)
</dt> <dt>

[**SetRevocationData**](iwmdrmsecurity-setrevocationdata.md)
</dt> </dl>

 

 





