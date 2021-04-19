---
description: 設定範例的子樣本對應，指出範例資料中的明確和加密的位元組。
ms.assetid: E672F53D-2083-430B-90D2-A1DA482EF9E1
title: 'MFSampleExtension_Encryption_SubSampleMappingSplit 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c90fb6ae22417f059bfa3268382877363178940
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106986806"
---
# <a name="mfsampleextension_encryption_subsamplemappingsplit-attribute"></a>MFSampleExtension \_ Encryption \_ SubSampleMappingSplit 屬性

設定範例的子樣本對應，指出範例資料中的明確和加密的位元組。

## <a name="data-type"></a>資料類型

**Blob**

## <a name="remarks"></a>備註

**BLOB** 應該包含位元組範圍的陣列，做為 dword，其中每兩個 dword 都會進行設定。 每個集合中的第一個 DWORD 是清除位元組的數目，而集合的第二個 dword 是已加密的位元組數目。 請注意，0對0不是有效的集合 (其中一個值可以是0，但不是兩個) 。 位元組範圍陣列指出要解密的範圍，包括整個範例不應解密的可能性。 建議您不要在清除範例上設定這項功能，雖然您可以使用適當的值來設定相同的結果來達到相同的結果。

## <a name="examples"></a>範例

下列範例顯示如何設定 MFSampleExtension \_ 加密 \_ SubSampleMappingSplit。


```C++
// m_spSample is a IMFSample
// pdwSubSampleMap is a DWORD*
// dwSubSampleMapSize is a DWORD

m_spSample->SetBlob( MFSampleExtension_Encryption_SubSampleMappingSplit,
                    (BYTE*)pdwSubSampleMap, 
                    dwSubSampleMapSize * sizeof(DWORD) );
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8.1 \[ 桌面應用程式 \| UWP 應用程式\]<br/>                                |
| 最低支援的伺服器<br/> | Windows Server 2012 R2 \[ 桌面應用程式 \| UWP 應用程式\]<br/>                     |
| 標頭<br/>                   | <dl> <dt>Mfapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)
</dt> <dt>

[MFSampleExtension \_ 內容 \_ KeyID](mfsampleextension-content-keyid.md)
</dt> </dl>

 

 




