---
description: 基底提供者和延伸提供者都可以指定要使用之 salt 值的值和長度。 基底提供者會使用 KP salt 參數值來設定 salt 值 \_ 。 基底提供者一律會設定十個位元組的 salt 值。
ms.assetid: ea56d064-b725-431f-b951-66167624e14b
title: 指定 Salt 值
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70d80ca64bc69cbcf0ed98d72b5b061616fc3cf641f3970d1533b094ef5687f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118897943"
---
# <a name="specifying-a-salt-value"></a>指定 Salt 值

基底提供者和延伸提供者都可以指定要使用之 [*salt 值*](../secgloss/s-gly.md) 的值和長度。 基底提供者會使用 KP salt 參數值來設定 salt 值 \_ 。 基底提供者一律會設定十個位元組的 salt 值。

增強型提供者會藉由呼叫 [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) ，並以指定的 KP \_ salt （ \_ 例如參數值）和 *>pbdata* 參數指向包含 salt 的 [**CRYPT \_ 整數 \_ BLOB**](/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)) 結構來設定 salt 值。

> [!Note]  
> 增強型提供者 [*對稱金鑰*](../secgloss/s-gly.md) 及其 salt 值的總長度不能大於128位。

 

\_會持續提供適用于基底提供者的回溯相容性的 KP SALT。 較新的應用程式應該使用 KP SALT 的範例 \_ \_ 參數值。

下列範例會設定 salt 值。


```C++
// Specify 4 bytes of salt.
BYTE rgbSalt[] = {0x01, 0x02, 0x03, 0x04};
CRYPT_DATA_BLOB sSaltData;
sSaltData.pbData = rgbSalt;
sSaltData.cbData = sizeof(rgbSalt);

// Set the 4 bytes of salt required.
// hKey is an HCRYPTPROV handle previously
// assigned, such as by CryptImportKey.
if (CryptSetKeyParam(
        hKey,    
        KP_SALT_EX,    
        (BYTE*)&sSaltData,    
        0))
{
     printf("The salt value is set.\n");
}
else
{
     printf("Setting the salt value failed.\n");
}
```



 

 
