---
title: 'IWMDRMSecurity CheckCertForRevocation 方法 (Wmdrmsdk .h) '
description: CheckCertForRevocation 方法會判斷憑證是否已撤銷。
ms.assetid: 3efde398-f2ba-486e-b017-6787ca402e4c
keywords:
- CheckCertForRevocation 方法 windows Media 格式
- CheckCertForRevocation 方法 windows Media Format，IWMDRMSecurity 介面
- IWMDRMSecurity 介面 windows Media Format，CheckCertForRevocation 方法
topic_type:
- apiref
api_name:
- IWMDRMSecurity.CheckCertForRevocation
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e090dfb655837ad2cf36cf45486488fde1440b499b73f16fdfbdaf2989532687
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118700784"
---
# <a name="iwmdrmsecuritycheckcertforrevocation-method"></a>IWMDRMSecurity：： CheckCertForRevocation 方法

**CheckCertForRevocation** 方法會判斷憑證是否已撤銷。

## <a name="syntax"></a>語法


```C++
HRESULT CheckCertForRevocation(
  [in]  REFGUID rguidRevocationList,
  [in]  BYTE    *pbCert,
  [in]  DWORD   cbCert,
  [out] BOOL    *fRevoked
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*rguidRevocationList* \[在\]
</dt> <dd>

識別要使用之撤銷清單的 GUID。 設定為下表中的其中一個值。



| GUID 常數                 | 描述                                                                                |
|-------------------------------|--------------------------------------------------------------------------------------------|
| WMDRM \_ REVOCATIONTYPE \_ 應用程式    | 指定應用程式憑證撤銷清單。                                     |
| WMDRM \_ REVOCATIONTYPE \_ 裝置 | 指定裝置憑證撤銷清單。                                          |
| WMDRM \_ REVOCATIONTYPE \_ CARDEA | 指定 Microsoft Windows 媒體 DRM 的網路裝置憑證撤銷清單。 |



 

</dd> <dt>

*pbCert* \[在\]
</dt> <dd>

包含要查閱之憑證的緩衝區。

</dd> <dt>

*cbCert* \[在\]
</dt> <dd>

緩衝區 *pbCert* 的大小（以位元組為單位）。

</dd> <dt>

*fRevoked* \[擴展\]
</dt> <dd>

在 [輸出] 上，指出憑證是否存在於撤銷清單中。

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

[**IWMDRMSecurity 介面**](iwmdrmsecurity.md)
</dt> </dl>

 

 





