---
description: EnvelopedData 物件提供屬性和方法，以透過加密波封隱私權的資料。
ms.assetid: 7c5f3e3d-6a70-455d-8921-20495eec4b3e
title: EnvelopedData 物件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnvelopedData
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: af88fd9b4be0c7ddd9fe5dfc204558c1a36cab418166f73c8de0ec0c06c0a8dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117766109"
---
# <a name="envelopeddata-object"></a>EnvelopedData 物件

\[CAPICOM 是僅限32位的元件，可供下列作業系統使用： Windows Server 2008、Windows Vista 和 Windows XP。 相反地，請使用 [**EnvelopedCms 類別**](/dotnet/api/system.security.cryptography.pkcs.envelopedcms?view=dotnet-plat-ext-3.1&preserve-view=true)，以使用 [**system.servicemodel 命名空間。**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true)\]

**EnvelopedData** 物件提供屬性和方法，以透過加密波封隱私權的資料。 若要波封資料，會產生會話密碼編譯金鑰。 接著，會針對每個預定的收件者，使用來自收件者憑證之收件者的 [*公開金鑰*](../secgloss/p-gly.md)來加密該 [*工作階段金鑰*](../secgloss/s-gly.md)。 加密的資料和加密的工作階段金鑰集可以傳送給所有預定的收件者。 產生的訊息是 PKCS \# 7 格式。

## <a name="members"></a>成員

**EnvelopedData** 物件具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**EnvelopedData** 物件有這些方法。



| 方法                                   | 描述                                                                                                 |
|:-----------------------------------------|:------------------------------------------------------------------------------------------------------------|
| [**解密**](envelopeddata-decrypt.md) | 解密封裝的內容。<br/>                                                                      |
| [**加密**](envelopeddata-encrypt.md) | 加密內容、為每個收件者加密工作階段金鑰，並傳回加密的 BLOB。<br/> |



 

### <a name="properties"></a>屬性

**EnvelopedData** 物件具有這些屬性。



| 屬性                                                  | 存取類型           | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|:----------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**演算法**](envelopeddata-algorithm.md)<br/>   | 讀取/寫入<br/> | 加密演算法和 [*金鑰長度*](../secgloss/k-gly.md)。<br/>                                                                                                                                                                                                                                                                                                                              |
| [**內容**](envelopeddata-content.md)<br/>       | 讀取/寫入<br/> | 要封裝之訊息的純文字內容。 設定此屬性必須在呼叫 [**加密**](envelopeddata-encrypt.md) 方法之前完成。<br/> 當這個屬性的值是直接或間接重設時，會重設物件的整個 [*狀態*](../secgloss/s-gly.md) ，而且會遺失物件中任何加密的內容。<br/> 這是預設屬性。<br/> |
| [**收件者**](envelopeddata-recipients.md)<br/> | 唯讀<br/>  | 接收封包訊息的 [**憑證**](certificate.md) 物件集合。<br/>                                                                                                                                                                                                                                                                                                                                              |



 

## <a name="remarks"></a>備註

您可以建立 **EnvelopedData** 物件，而且可以安全地進行腳本處理。 **EnvelopedData** 物件的 PROGID 是 CAPICOM。EnvelopedData。1。

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

 

 
