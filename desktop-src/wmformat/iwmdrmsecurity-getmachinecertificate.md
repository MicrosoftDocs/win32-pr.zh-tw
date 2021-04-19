---
title: 'IWMDRMSecurity GetMachineCertificate 方法 (Wmdrmsdk .h) '
description: GetMachineCertificate 方法會抓取用戶端電腦上 DRM 子系統的電腦憑證。
ms.assetid: 38b8e812-e997-4a63-b906-ebd26a5556be
keywords:
- GetMachineCertificate 方法 windows Media 格式
- GetMachineCertificate 方法 windows Media Format，IWMDRMSecurity 介面
- IWMDRMSecurity 介面 windows Media Format，GetMachineCertificate 方法
topic_type:
- apiref
api_name:
- IWMDRMSecurity.GetMachineCertificate
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d6c66c54ab9528a458910def5978ec83b191654
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977693"
---
# <a name="iwmdrmsecuritygetmachinecertificate-method"></a>IWMDRMSecurity：： GetMachineCertificate 方法

**GetMachineCertificate** 方法會抓取用戶端電腦上 DRM 子系統的電腦憑證。

## <a name="syntax"></a>語法


```C++
HRESULT GetMachineCertificate(
  [in]      DWORD dwCertificateType,
  [out]     BYTE  rgbVersion[4],
  [out]     BYTE  **ppbCertificate,
  [in, out] DWORD *pcbCertificate
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*dwCertificateType* \[在\]
</dt> <dd>

要取出的憑證類型。 設定為下表中的其中一個值。



| 值                        | 描述                                                                           |
|------------------------------|---------------------------------------------------------------------------------------|
| WMDRM \_ 憑證 \_ 類型 \_ V1 | 憑證將以舊版元件使用的格式抓取。            |
| WMDRM \_ 憑證 \_ 類型 \_ V2 | 憑證將以 Windows Vista 元件使用的格式抓取。 |



 

</dd> <dt>

*rgbVersion \[ 4 \]* \[ 輸出\]
</dt> <dd>

四個位元組的陣列，指定用戶端電腦上的 DRM 子系統版本。

</dd> <dt>

*ppbCertificate* \[擴展\]
</dt> <dd>

接收憑證資料指標之變數的位址。 設定為 **Null** ，讓方法提供在 *pcbCertificate* 中保存憑證所需的緩衝區大小。

</dd> <dt>

*pcbCertificate* \[in、out\]
</dt> <dd>

憑證的大小（以位元組為單位）。 如果 *ppbCertificate* 為 **Null**，則此值會設定為憑證的大小。 如果 *ppbCertificate* 不是 **Null**，這個值就必須設定為緩衝區的大小。

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

[**IWMDRMSecurity 介面**](iwmdrmsecurity.md)
</dt> </dl>

 

 





