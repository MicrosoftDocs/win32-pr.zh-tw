---
description: 下列函式是可以擴充的 CryptoAPI 函數之一。
ms.assetid: eb4c1352-1432-4f45-a309-fa17b694a35e
title: 建立新功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d660c14e99247c7d17f57100858b104d1cbcc9ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511174"
---
# <a name="creating-the-new-functionality"></a>建立新功能

下列函式是可以擴充的 CryptoAPI 函數之一。



| CryptoAPI 函數                                   | OID 函數名稱定義                         | OID 函數名稱字串  |
|------------------------------------------------------|--------------------------------------------------|---------------------------|
| [**CryptEncodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject)       | CRYPT \_ OID \_ 編碼 \_ OBJECT \_ FUNC<br/>     | "CryptDllEncodeObject"    |
| [**CryptDecodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecodeobject)       | CRYPT \_ OID \_ 解碼 \_ 物件 \_ FUNC<br/>     | "CryptDllDecodeObject"    |
| [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore)               | CRYPT \_ OID \_ OPEN \_ STORE \_ >PROV \_ FUNC<br/>  | "CertDllOpenStoreProv"    |
| [**CertVerifyCTLUsage**](/windows/desktop/api/Wincrypt/nf-wincrypt-certverifyctlusage)     | CRYPT \_ OID \_ 驗證 \_ CTL \_ 使用方式 \_ FUNC<br/> | "CertDllVerifyCTLUsage"   |
| [**CertVerifyRevocation**](/windows/desktop/api/Wincrypt/nf-wincrypt-certverifyrevocation) | CRYPT \_ OID \_ 確認 \_ 撤銷 \_ FUNC<br/> | "CertDllVerifyRevocation" |



 

在一般情況下使用現有的 OID 和編碼類型時，會使用 CryptoAPI 函式本身的程式碼。 如果使用 OID 函式中的程式碼所呼叫的其中一個函式不是設計來處理的，則必須在 DLL 中建立包含新功能的新函式。 該 DLL 必須在登錄中註冊或安裝在記憶體中。

使用新指定的 OID 和編碼類型呼叫其中一個列出的函式時，會使用新 DLL 中的程式碼，而不是 CryptoAPI 函式所提供的程式碼。

新開發的函式名稱可以是上表的「OID 函式名稱字串」下所列的名稱，或者，在註冊新的函式程式碼時，可以指定不同的名稱。

新的函數必須使用適當的原型。 除了 [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore)以外的所有情況下，這個原型與呼叫 new 函式的 CryptoAPI 函數相同。 在 **CertOpenStore** 的案例中，原型如下所示。


```C++
#include <windows.h>

BOOL WINAPI CertDllOpenStoreProv(
  IN LPCSTR lpszStoreProvider,
  IN DWORD dwEncodingType,
  IN HCRYPTPROV hCryptProv,
  IN DWORD dwFlags,
  IN const void *pvPara,
  IN HCERTSTORE hCertStore,
  IN OUT PCERT_STORE_PROV_INFO pStoreProvInfo
);
```



> [!Note]  
> 如果原型不相符，系統堆疊將會損毀。

 

除了提供 DLL 中新函式的程式碼之外，擴充 [**CryptEncodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject) 或 [**CryptDecodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecodeobject) 的功能需要將新 C 資料結構的型別定義放在使用者的程式編譯時所包含的標頭檔中。

 

 




