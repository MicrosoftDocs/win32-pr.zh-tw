---
description: 基底提供者和延伸提供者都可以指定要使用之 salt 值的值和長度。 基底提供者會使用 KP salt 參數值來設定 salt 值 \_ 。 基底提供者一律會設定十個位元組的 salt 值。
ms.assetid: ea56d064-b725-431f-b951-66167624e14b
title: 指定 Salt 值
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9fc8aeea66c536db1c24d7ef3cf4fb9a05b543f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106998903"
---
# <a name="specifying-a-salt-value"></a><span data-ttu-id="220b7-105">指定 Salt 值</span><span class="sxs-lookup"><span data-stu-id="220b7-105">Specifying a Salt Value</span></span>

<span data-ttu-id="220b7-106">基底提供者和延伸提供者都可以指定要使用之 [*salt 值*](../secgloss/s-gly.md) 的值和長度。</span><span class="sxs-lookup"><span data-stu-id="220b7-106">Both the Base Provider and the Extended Provider can specify the value and length of the [*salt value*](../secgloss/s-gly.md) to be used.</span></span> <span data-ttu-id="220b7-107">基底提供者會使用 KP salt 參數值來設定 salt 值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="220b7-107">The Base Provider sets a salt value using the KP\_SALT parameter value.</span></span> <span data-ttu-id="220b7-108">基底提供者一律會設定十個位元組的 salt 值。</span><span class="sxs-lookup"><span data-stu-id="220b7-108">The Base Provider always sets eleven bytes of salt value.</span></span>

<span data-ttu-id="220b7-109">增強型提供者會藉由呼叫 [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) ，並以指定的 KP \_ salt （ \_ 例如參數值）和 *>pbdata* 參數指向包含 salt 的 [**CRYPT \_ 整數 \_ BLOB**](/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)) 結構來設定 salt 值。</span><span class="sxs-lookup"><span data-stu-id="220b7-109">The Enhanced Provider sets the salt value by calling [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) with the KP\_SALT\_EX parameter value specified and with the *pbData* parameter pointing to a [**CRYPT\_INTEGER\_BLOB**](/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)) structure that contains the salt.</span></span>

> [!Note]  
> <span data-ttu-id="220b7-110">增強型提供者 [*對稱金鑰*](../secgloss/s-gly.md) 及其 salt 值的總長度不能大於128位。</span><span class="sxs-lookup"><span data-stu-id="220b7-110">The total length of an Enhanced Provider [*symmetric key*](../secgloss/s-gly.md) and its salt value cannot be greater than 128 bits.</span></span>

 

<span data-ttu-id="220b7-111">\_會持續提供適用于基底提供者的回溯相容性的 KP SALT。</span><span class="sxs-lookup"><span data-stu-id="220b7-111">KP\_SALT continues to be provided for backward compatibility with the Base Provider.</span></span> <span data-ttu-id="220b7-112">較新的應用程式應該使用 KP SALT 的範例 \_ \_ 參數值。</span><span class="sxs-lookup"><span data-stu-id="220b7-112">Newer applications should use the KP\_SALT\_EX parameter value.</span></span>

<span data-ttu-id="220b7-113">下列範例會設定 salt 值。</span><span class="sxs-lookup"><span data-stu-id="220b7-113">The following example sets a salt value.</span></span>


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



 

 
