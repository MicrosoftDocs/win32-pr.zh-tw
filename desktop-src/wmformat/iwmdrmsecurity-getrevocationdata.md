---
title: 'IWMDRMSecurity GetRevocationData 方法 (Wmdrmsdk .h) '
description: GetRevocationData 方法會從本機存放區抓取憑證撤銷清單。
ms.assetid: 218f4f3a-02bc-4b1d-9320-e35ed8cc3b11
keywords:
- GetRevocationData 方法 windows Media 格式
- GetRevocationData 方法 windows Media Format，IWMDRMSecurity 介面
- IWMDRMSecurity 介面 windows Media Format，GetRevocationData 方法
topic_type:
- apiref
api_name:
- IWMDRMSecurity.GetRevocationData
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c38e9e0b428a3922f84141ef855d8468b79b3bb2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989720"
---
# <a name="iwmdrmsecuritygetrevocationdata-method"></a>IWMDRMSecurity：： GetRevocationData 方法

**GetRevocationData** 方法會從本機存放區抓取憑證撤銷清單。

## <a name="syntax"></a>語法


```C++
HRESULT GetRevocationData(
  [in]      REFGUID f_guidRevocationType,
  [out]     BYTE    *f_pbCRL,
  [in, out] DWORD   *f_pcbCRL
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*f \_ guidRevocationType* \[ in\]
</dt> <dd>

識別要取出的撤銷清單類型的 GUID。 使用下表中的其中一個常數。



| GUID 常數                 | Description                                                                      |
|-------------------------------|----------------------------------------------------------------------------------|
| WMDRM \_ REVOCATIONTYPE \_ 應用程式    | 指定應用程式憑證撤銷清單。                           |
| WMDRM \_ REVOCATIONTYPE \_ 裝置 | 指定裝置憑證撤銷清單。                                |
| WMDRM \_ REVOCATIONTYPE \_ CARDEA | 指定「網路裝置的 Windows Media DRM」憑證撤銷清單。 |



 

</dd> <dt>

*f \_ pbCRL* \[ 輸出\]
</dt> <dd>

接收撤銷清單的緩衝區。 設定為 **Null** 可取得所需的緩衝區大小。

</dd> <dt>

*f \_ pcbCRL* \[ in，out\]
</dt> <dd>

以位元組為單位的緩衝區大小。 如果 *f \_ PbCRL* 為 **Null**，則會在輸出時將此值設定為所需的緩衝區大小。

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

[**自動化元件撤銷和更新**](automated-component-revocation-and-renewal.md)
</dt> <dt>

[**GetRevocationDataVersion**](iwmdrmsecurity-getrevocationdataversion.md)
</dt> <dt>

[**IWMDRMSecurity 介面**](iwmdrmsecurity.md)
</dt> <dt>

[**SetRevocationData**](iwmdrmsecurity-setrevocationdata.md)
</dt> </dl>

 

 





