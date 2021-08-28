---
description: 指定加密範例的保護設定。
ms.assetid: 04E9F908-C61C-43DC-8CF5-9A629FCDD82C
title: 'MFSampleExtension_Encryption_ProtectionScheme 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a9db7d00d67b0e9806167ea574d10c3dca5f199293c03f5e055d60430c2dd75
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119603178"
---
# <a name="mfsampleextension_encryption_protectionscheme-attribute"></a>MFSampleExtension \_ Encryption \_ ProtectionScheme 屬性

指定加密範例的保護設定。

## <a name="data-type"></a>資料類型

**UINT32**

## <a name="remarks"></a>備註

這個屬性的值是 [**MFSampleEncryptionProtectionScheme**](/windows/win32/api/mfapi/ne-mfapi-mfsampleencryptionprotectionscheme) 列舉的成員。 如果媒體來源是以值為基礎，則會根據 [配置類型] 方塊中的 [ **配置 \_ 類型** ] 欄位值來設定值， ( ( [moov] 或 [moof] ) 的 [配置類型] 方塊中的 [schm] ) 。

如果 **配置 \_ 類型** 為基礎的檔案或資料流程中的配置類型欄位設定為 ' cenc ' 或 ' cbc1 '，則應該分別將 **MFSampleExtension \_ encryption \_ ProtectionScheme** 屬性設定為「 **保護 \_ 配置 \_ AES \_ CTR** 」或「 **保護 \_ 配置 \_ CBC**」，且不應針對 [MFSampleExtension \_ encryption \_ CryptByteBlock](mfsampleextension-encryption-cryptbyteblock.md) 和 [MFSampleExtension \_ encryption \_ SkipByteBlock](mfsampleextension-encryption-skipbyteblock.md)設定任何值。

如果 [設定檔案] 或 [資料流程] 中的 [ **配置 \_ 類型** ] 欄位設定為 [cens] 或 [cbcs]，則應該將 [ **MFSampleExtension \_ 加密 \_ ProtectionScheme** ] 屬性分別設定為 [ **保護 \_ 配置 \_ AES \_ CTR** ] 或 [ **保護 \_ 配置 \_ CBC**]，並使用 [MFSampleExtension] 方塊中的值設定 [CryptByteBlock \_ 加密 \_](mfsampleextension-encryption-cryptbyteblock.md) MFSampleExtension 和 [SkipByteBlock \_ 加密 \_ tenc](mfsampleextension-encryption-skipbyteblock.md) 。

## <a name="examples"></a>範例

下列範例顯示如何設定 **MFSampleExtension \_ 加密 \_ ProtectionScheme** 和相關聯的 **MFSampleExtension \_ encryption \_ CryptByteBlock** 和 **MFSampleExtension \_ encryption \_ SkipByteBlock** 屬性。


```C++
HRESULT AddEncryptionAttributes(_In_ IMFSample* pSample, _In_ bool fIsEncrypted)
{
      HRESULT hr = S_OK;

      if (fIsEncrypted)
    {
        //Set Encryption Protection Scheme
        hr = pSample->UINT32(MFSampleExtension_Encryption_ProtectionScheme,
            SAMPLE_ENCRYPTION_PROTECTION_SCHEME_AES_CBC);
            if (FAILED(hr))
                return hr;

        //Set the Initialization Vector (IV)
  //(spSampleEncryptionData is omitted from this example for simplicity.) 
        hr = pSample->SetBlob(MFSampleExtension_Encryption_SampleID, 
            (BYTE*)(spSampleEncryptionData->m_pInitializationVector),
            spSampleEncryptionData->m_bIVSize);
            if (FAILED(hr))
                return hr;

        //Set crypt and skip byte blocks for pattern encryption
        hr = pSample->SetUINT32(MFSampleExtension_Encryption_CryptByteBlock, 1);
            if (FAILED(hr))
                return hr;

        hr = pSample->SetUINT32(MFSampleExtension_Encryption_SkipByteBlock, 9);
            if (FAILED(hr))
                return hr;
    }
      return hr;
}
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10， \[ 僅限1709版桌面應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>Mfidl。h</dt> </dl> |



 

 
