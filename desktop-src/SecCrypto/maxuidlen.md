---
description: 數值常數，指定某些 Microsoft 密碼編譯提供者在取得使用者識別碼時將使用的最大字元數。
ms.assetid: cc15a166-9a0c-41ce-9cb1-ecdc922565c0
title: 'MAXUIDLEN (Wincrypt) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d3a2cad5f6e676fc0e0677ccc9f76262f4ba4104aa58d0662b92f23206cb6d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119408006"
---
# <a name="maxuidlen"></a>MAXUIDLEN

MAXUIDLEN 是一個數值常數，可指定某些 Microsoft 密碼編譯提供者在取得使用者識別碼時將使用的最大字元數。 MAXUIDLEN 定義于 Wincrypt 中。



| 常數/值                                                                                                                                                                                                  | Description                                                                                                                                                                                                                                                                                                                                                                                                   |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MAXUIDLEN"></span><span id="maxuidlen"></span><dl> <dt>**MAXUIDLEN**</dt> <dt>64 (0x40)</dt> </dl> | 當 [**CryptAcquireCoNtext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta)函式的 *PszContainer* 參數為 **Null** 時，某些 Microsoft 密碼編譯提供者會使用目前登入之使用者的登入名稱做為金鑰容器名稱。 MAXUIDLEN 指定這些提供者將用於使用者名稱的字元數上限，包括結束的 **Null** 字元。<br/> |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Wincrypt。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CryptAcquireCoNtext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta)
</dt> <dt>

[**CPAcquireCoNtext**](https://www.bing.com/search?q=**CPAcquireContext**)
</dt> </dl>

 

 




