---
title: 'IWMDRMLicense CreateSecureDecryptor 方法 (Wmdrmsdk .h) '
description: CreateSecureDecryptor 方法會建立安全的解密子物件。 安全解密程式與一般解密程式不同，因為它會解密內容，然後根據此方法的參數中指定的設定重新加密。
ms.assetid: f3fe8d47-ec7b-4ba5-b5ae-6262cb455ffc
keywords:
- CreateSecureDecryptor 方法 windows Media 格式
- CreateSecureDecryptor 方法 windows Media Format，IWMDRMLicense 介面
- IWMDRMLicense 介面 windows Media Format，CreateSecureDecryptor 方法
topic_type:
- apiref
api_name:
- IWMDRMLicense.CreateSecureDecryptor
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96c562dcafd72a72ecef340688fd709ecbe5446abae53403d403c9a70bdd6f2b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118433667"
---
# <a name="iwmdrmlicensecreatesecuredecryptor-method"></a>IWMDRMLicense：： CreateSecureDecryptor 方法

**CreateSecureDecryptor** 方法會建立安全的解密子物件。 安全解密程式與一般解密程式不同，因為它會解密內容，然後根據此方法的參數中指定的設定重新加密。

## <a name="syntax"></a>語法


```C++
HRESULT CreateSecureDecryptor(
  [in]      BYTE          *pbCertificate,
  [in]      DWORD         cbCertificate,
  [in]      DWORD         dwCertificateType,
  [in]      DWORD         dwFlags,
  [out]     BYTE          *pbInitializationVector,
  [in, out] DWORD         *pcbInitializationVector,
  [out]     IWMDRMDecrypt **ppDecryptor
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pbCertificate* \[在\]
</dt> <dd>

呼叫應用程式的憑證。

</dd> <dt>

*cbCertificate* \[在\]
</dt> <dd>

憑證的大小（以位元組為單位）。

</dd> <dt>

*dwCertificateType* \[在\]
</dt> <dd>

憑證的類型。 設定為 WMDRM \_ 憑證 \_ 類型 \_ XML。

</dd> <dt>

*dwFlags* \[在\]
</dt> <dd>

要用於重新編碼的會話保護類型。 必須設定為下表中的其中一個常數：



| 常數                     | 描述                                                                                                 |
|------------------------------|-------------------------------------------------------------------------------------------------------------|
| WMDRM \_ 保護 \_ 類型 \_ RC4 | 使用 RC4 加密進行會話加密。 這是此版本唯一支援的會話保護。 |



 

</dd> <dt>

*pbInitializationVector* \[擴展\]
</dt> <dd>

接收初始化向量。 初始化向量是使用 OAEP 填補配置與憑證中找到的 RSA 公開金鑰進行加密的 RSA。 設定為 **Null** ，以接收 *pcbInitializationVector* 中所需的緩衝區大小。

</dd> <dt>

*pcbInitializationVector* \[in、out\]
</dt> <dd>

在輸入時，緩衝區的大小會以 *pbInitializationVector* 的形式傳遞。 在輸出時，緩衝區所使用部分的大小。 如果您傳遞 **Null** 給 *pbInitializationVector*，此值會在輸出時設定為所需的緩衝區大小。

</dd> <dt>

*ppDecryptor* \[擴展\]
</dt> <dd>

接收新建立物件之 [**IWMDRMDecrypt**](iwmdrmdecrypt.md) 介面的指標。

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
|-------------------|---------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Wmdrmsdk。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IWMDRMLicense 介面**](iwmdrmlicense.md)
</dt> </dl>

 

 





