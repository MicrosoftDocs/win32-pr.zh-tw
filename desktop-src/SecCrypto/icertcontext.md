---
description: 提供 CAPICOM x.509v3 憑證物件內容的存取權。 此內容可讓 CAPICOM 憑證用於其他的 CryptoAPI 衍生。
ms.assetid: 084a3a7b-7523-419f-a504-6fd397030d78
title: ICertCoNtext 介面
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ICertContext
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 693e259c730209049f669d1499001d026b3d11088c7bef09616826a4673cac0b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006036"
---
# <a name="icertcontext-interface"></a>ICertCoNtext 介面

\[CAPICOM 是僅限32位的元件，可供下列作業系統使用： Windows Server 2008、Windows Vista 和 Windows XP。\]

**ICertCoNtext** 介面可讓您存取 CAPICOM x.509v3 [**憑證**](certificate.md)物件的內容。 此內容可讓 CAPICOM 憑證用於其他的 CryptoAPI 衍生。

## <a name="when-to-use"></a>使用時機

當您需要在 CryptoAPI 的另一個衍生中使用 CAPICOM [**憑證**](certificate.md) 物件時，請使用此介面。

## <a name="members"></a>成員

**ICertCoNtext** 介面具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**ICertCoNtext** 介面具有這些方法。



| 方法                                          | 描述                                                                                                          |
|:------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------|
| [**FreeCoNtext**](icertcontext-freecontext.md) | 釋放 \_ 透過 [**CertCoNtext**](icertcontext-certcontext.md) 屬性取得的 PCCERT 內容。<br/> |



 

### <a name="properties"></a>屬性

**ICertCoNtext** 介面具有這些屬性。



| 屬性                                                   | 存取類型           | 描述                                                        |
|:-----------------------------------------------------------|:----------------------|:-------------------------------------------------------------------|
| [**CertCoNtext**](icertcontext-certcontext.md)<br/> | 讀取/寫入<br/> | 設定或抓取憑證的 PCCERT \_ 內容。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|----------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 




