---
description: 指定以範例為基礎的模式加密的加密位元組區塊大小。
ms.assetid: 1F370DEC-20B5-456D-BB68-C94E183410F3
title: 'MFSampleExtension_Encryption_CryptByteBlock 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 927e08d81cc8066f73b579c8abf419d754fc1713
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026534"
---
# <a name="mfsampleextension_encryption_cryptbyteblock-attribute"></a>MFSampleExtension \_ Encryption \_ CryptByteBlock 屬性

指定以範例為基礎的模式加密的加密位元組區塊大小。

## <a name="data-type"></a>資料類型

**UINT32**

## <a name="remarks"></a>備註

Subsample 對應區塊中的 clear (非加密) 位元組數目是在 [MFSampleExtension \_ Encryption \_ SkipByteBlock](mfsampleextension-encryption-skipbyteblock.md) 屬性中指定。 如果其中一個屬性不存在或值為0，則表示範例資料不會加密。 這兩個值都必須為非零、正值或兩者都必須有零值。

如果來源是以值為基礎，則會根據 [ \_ crypt] \_ ( [tenc] ) 在 [配置] 標頭中的 [預設值] 位元組區塊的值來設定值 \_ 。 如需詳細資訊，請參閱 [MFSampleExtension \_ 加密 \_ ProtectionScheme](mfsampleextension-encryption-protectionscheme.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10， \[ 僅限1709版桌面應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>Mfidl。h</dt> </dl> |



 

 




