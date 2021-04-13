---
description: 指定加密範例的保護設定。
ms.assetid: 04E9F908-C61C-43DC-8CF5-9A629FCDD82C
title: 'MFSampleExtension_Encryption_ProtectionScheme 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de298eb310e1258274a4ce24d49e9b53def38cde
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115005"
---
# <a name="mfsampleextension_encryption_protectionscheme-attribute"></a><span data-ttu-id="11b3f-103">MFSampleExtension \_ Encryption \_ ProtectionScheme 屬性</span><span class="sxs-lookup"><span data-stu-id="11b3f-103">MFSampleExtension\_Encryption\_ProtectionScheme attribute</span></span>

<span data-ttu-id="11b3f-104">指定加密範例的保護設定。</span><span class="sxs-lookup"><span data-stu-id="11b3f-104">Specifies the protection scheme for encrypted samples.</span></span>

## <a name="data-type"></a><span data-ttu-id="11b3f-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="11b3f-105">Data type</span></span>

<span data-ttu-id="11b3f-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="11b3f-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="11b3f-107">備註</span><span class="sxs-lookup"><span data-stu-id="11b3f-107">Remarks</span></span>

<span data-ttu-id="11b3f-108">這個屬性的值是 [**MFSampleEncryptionProtectionScheme**](/windows/win32/api/mfapi/ne-mfapi-mfsampleencryptionprotectionscheme) 列舉的成員。</span><span class="sxs-lookup"><span data-stu-id="11b3f-108">The value of this attribute is a member of the [**MFSampleEncryptionProtectionScheme**](/windows/win32/api/mfapi/ne-mfapi-mfsampleencryptionprotectionscheme) enumeration.</span></span> <span data-ttu-id="11b3f-109">如果媒體來源是以值為基礎，則會根據 [配置類型] 方塊中的 [ **配置 \_ 類型** ] 欄位值來設定值， ( ( [moov] 或 [moof] ) 的 [配置類型] 方塊中的 [schm] ) 。</span><span class="sxs-lookup"><span data-stu-id="11b3f-109">In cases where the media source is MP4-based, the value is set based off the value of the **scheme\_type** field within the scheme type box (‘schm’) in the MP4 header (‘moov’ or ‘moof’).</span></span>

<span data-ttu-id="11b3f-110">如果 **配置 \_ 類型** 為基礎的檔案或資料流程中的配置類型欄位設定為 ' cenc ' 或 ' cbc1 '，則應該分別將 **MFSampleExtension \_ encryption \_ ProtectionScheme** 屬性設定為「 **保護 \_ 配置 \_ AES \_ CTR** 」或「 **保護 \_ 配置 \_ CBC**」，且不應針對 [MFSampleExtension \_ encryption \_ CryptByteBlock](mfsampleextension-encryption-cryptbyteblock.md) 和 [MFSampleExtension \_ encryption \_ SkipByteBlock](mfsampleextension-encryption-skipbyteblock.md)設定任何值。</span><span class="sxs-lookup"><span data-stu-id="11b3f-110">If the **scheme\_type** field in an MP4-based file, or stream, is set to ‘cenc’ or ‘cbc1’, then the **MFSampleExtension\_Encryption\_ProtectionScheme** attribute should be set to **PROTECTION\_SCHEME\_AES\_CTR** or **PROTECTION\_SCHEME\_CBC**, respectively, and no values should be set for [MFSampleExtension\_Encryption\_CryptByteBlock](mfsampleextension-encryption-cryptbyteblock.md) and [MFSampleExtension\_Encryption\_SkipByteBlock](mfsampleextension-encryption-skipbyteblock.md).</span></span>

<span data-ttu-id="11b3f-111">如果 [設定檔案] 或 [資料流程] 中的 [ **配置 \_ 類型** ] 欄位設定為 [cens] 或 [cbcs]，則應該將 [ **MFSampleExtension \_ 加密 \_ ProtectionScheme** ] 屬性分別設定為 [ **保護 \_ 配置 \_ AES \_ CTR** ] 或 [ **保護 \_ 配置 \_ CBC**]，並使用 [MFSampleExtension] 方塊中的值設定 [CryptByteBlock \_ 加密 \_](mfsampleextension-encryption-cryptbyteblock.md) MFSampleExtension 和 [SkipByteBlock \_ 加密 \_ tenc](mfsampleextension-encryption-skipbyteblock.md) 。</span><span class="sxs-lookup"><span data-stu-id="11b3f-111">If the **scheme\_type** field in an MP4-based file, or stream, is set to ‘cens’ or ‘cbcs’, then the **MFSampleExtension\_Encryption\_ProtectionScheme** attribute should be set to **PROTECTION\_SCHEME\_AES\_CTR** or **PROTECTION\_SCHEME\_CBC**, respectively, and [MFSampleExtension\_Encryption\_CryptByteBlock](mfsampleextension-encryption-cryptbyteblock.md) and [MFSampleExtension\_Encryption\_SkipByteBlock](mfsampleextension-encryption-skipbyteblock.md) must be set using the values in the ‘tenc’ box.</span></span>

## <a name="examples"></a><span data-ttu-id="11b3f-112">範例</span><span class="sxs-lookup"><span data-stu-id="11b3f-112">Examples</span></span>

<span data-ttu-id="11b3f-113">下列範例顯示如何設定 **MFSampleExtension \_ 加密 \_ ProtectionScheme** 和相關聯的 **MFSampleExtension \_ encryption \_ CryptByteBlock** 和 **MFSampleExtension \_ encryption \_ SkipByteBlock** 屬性。</span><span class="sxs-lookup"><span data-stu-id="11b3f-113">The following example shows how to set the **MFSampleExtension\_Encryption\_ProtectionScheme** and the associated **MFSampleExtension\_Encryption\_CryptByteBlock** and **MFSampleExtension\_Encryption\_SkipByteBlock** attributes.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="11b3f-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="11b3f-114">Requirements</span></span>



| <span data-ttu-id="11b3f-115">需求</span><span class="sxs-lookup"><span data-stu-id="11b3f-115">Requirement</span></span> | <span data-ttu-id="11b3f-116">值</span><span class="sxs-lookup"><span data-stu-id="11b3f-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="11b3f-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="11b3f-117">Minimum supported client</span></span><br/> | <span data-ttu-id="11b3f-118">Windows 10， \[ 僅限1709版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="11b3f-118">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="11b3f-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="11b3f-119">Minimum supported server</span></span><br/> | <span data-ttu-id="11b3f-120">都不支援</span><span class="sxs-lookup"><span data-stu-id="11b3f-120">None supported</span></span><br/>                                                          |
| <span data-ttu-id="11b3f-121">標頭</span><span class="sxs-lookup"><span data-stu-id="11b3f-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="11b3f-122"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="11b3f-122"><dt>Mfidl.h</dt></span></span> </dl> |



 

 
