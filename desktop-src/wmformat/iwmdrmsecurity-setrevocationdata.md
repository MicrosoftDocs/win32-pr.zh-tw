---
title: 'IWMDRMSecurity SetRevocationData 方法 (Wmdrmsdk .h) '
description: SetRevocationData 方法會在本機存放區中設定憑證撤銷清單。
ms.assetid: 7e1c6d50-7a22-41b7-b29f-b1e5809a2097
keywords:
- SetRevocationData 方法 windows Media 格式
- SetRevocationData 方法 windows Media Format，IWMDRMSecurity 介面
- IWMDRMSecurity 介面 windows Media Format，SetRevocationData 方法
topic_type:
- apiref
api_name:
- IWMDRMSecurity.SetRevocationData
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e3ece5a9285420261add123a61d0b7123896e2d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990117"
---
# <a name="iwmdrmsecuritysetrevocationdata-method"></a>IWMDRMSecurity：： SetRevocationData 方法

**SetRevocationData** 方法會在本機存放區中設定憑證撤銷清單。

## <a name="syntax"></a>語法


```C++
HRESULT SetRevocationData(
  [in] REFGUID f_guidRevocationType,
  [in] BYTE    *f_pbCRL,
  [in] DWORD   f_cbCRL
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*f \_ guidRevocationType* \[ in\]
</dt> <dd>

指定撤銷清單類型的 GUID。 設定為下表中的其中一個常數。



| GUID 常數                 | Description                                                                      |
|-------------------------------|----------------------------------------------------------------------------------|
| WMDRM \_ REVOCATIONTYPE \_ 應用程式    | 指定應用程式憑證撤銷清單。                           |
| WMDRM \_ REVOCATIONTYPE \_ 裝置 | 指定裝置憑證撤銷清單。                                |
| WMDRM \_ REVOCATIONTYPE \_ CARDEA | 指定「網路裝置的 Windows Media DRM」憑證撤銷清單。 |



 

</dd> <dt>

*f \_ pbCRL* \[ in\]
</dt> <dd>

包含憑證撤銷清單的緩衝區。

</dd> <dt>

*f \_ cbCRL* \[ in\]
</dt> <dd>

緩衝區的大小（以位元組為單位）。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回 **HRESULT**。 可能的值包括 (但不限於) 下表中的這些值。



| 傳回碼                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl> | 此方法已成功。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Wmdrmsdk。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>Wmdrmsdk .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**GetRevocationData**](iwmdrmsecurity-getrevocationdata.md)
</dt> <dt>

[**GetRevocationDataVersion**](iwmdrmsecurity-getrevocationdataversion.md)
</dt> <dt>

[**IWMDRMSecurity 介面**](iwmdrmsecurity.md)
</dt> </dl>

 

 





