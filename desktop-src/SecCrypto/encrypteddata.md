---
description: 提供屬性和方法，以使用衍生自秘密的工作階段金鑰來加密和解密資料。
ms.assetid: 3b9bd0a2-6e15-4d58-a682-588a93895799
title: A 物件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EncryptedData
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 15a66640ccdf794e88ae9cff04854a40fcfa6b763259da191bcdc6b07f11f449
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119874488"
---
# <a name="encrypteddata-object"></a>A 物件

\[CAPICOM 是僅限32位的元件，可供下列作業系統使用： Windows Server 2008、Windows Vista 和 Windows XP。 相反地，請使用 (PInvoke) 的平台叫用服務來呼叫 WIN32 API 函式 [**CryptEncryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencryptmessage) 和 [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) ，以加密和解密訊息。 如需 PInvoke 的詳細資訊，請參閱 [平台叫用教學](https://msdn.microsoft.com/library/aa288468.aspx)課程。 [.Net 和 cryptoapi Via p/invoke：第1部分](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5)和[.net，以及透過 p/invoke](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6)叫用的 cryptoapi：[利用 CAPICOM 和 p/invoke 擴充 .net 密碼](/previous-versions/ms867087(v=msdn.10))編譯的第二部分，可能也很有用。\]

**A** 物件提供屬性和方法，以使用衍生自秘密的 [*工作階段金鑰*](../secgloss/s-gly.md)來加密和解密資料。

> [!Note]  
> CAPICOM 不支援 PKCS \# 7 a 內容類型，但會使用非標準的 ASN 結構來進行 **a**。 因此，只有 CAPICOM 才能解密 CAPICOM **a** 物件。

 

## <a name="members"></a>成員

**A** 物件具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**A** 物件有這些方法。



| 方法                                       | 描述                                                                             |
|:---------------------------------------------|:----------------------------------------------------------------------------------------|
| [**解密**](encrypteddata-decrypt.md)     | 使用秘密來解密加密的內容。<br/>                                 |
| [**加密**](encrypteddata-encrypt.md)     | 使用目前的密碼和加密演算法來加密內容。<br/>      |
| [**>client.setsecret**](encrypteddata-setsecret.md) | 設定用來衍生加密/解密工作階段金鑰的秘密。<br/> |



 

### <a name="properties"></a>屬性

**A** 物件具有這些屬性。



| 屬性                                                | 存取類型           | 描述                                                                                                                                                                                                                                                                                                                                                                                                                               |
|:--------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**演算法**](encrypteddata-algorithm.md)<br/> | 唯讀<br/>  | 用於加密/解密的演算法。<br/>                                                                                                                                                                                                                                                                                                                                                                                      |
| [**內容**](encrypteddata-content.md)<br/>     | 讀取/寫入<br/> | 要加密或解密的內容。 設定此屬性必須在呼叫 [**加密**](encrypteddata-encrypt.md) 方法之前完成。 <br/> 當這個屬性的值是直接或間接重設時，會重設物件的整個 [*狀態*](../secgloss/s-gly.md) ，而且會遺失物件中任何加密的內容。<br/> 這是預設屬性。<br/> |



 

## <a name="remarks"></a>備註

您可以建立 **a** 物件，而且可以安全地進行腳本處理。 **A** 物件的 PROGID 是 CAPICOM。A。1。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------------|----------------------------------------------------------------------------------------|
| 用戶端支援結束<br/> | Windows Vista<br/>                                                               |
| 伺服器支援結束<br/> | Windows Server 2008<br/>                                                         |
| 可轉散發套件<br/>       | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**加密物件**](cryptography-objects.md)
</dt> </dl>

 

 
