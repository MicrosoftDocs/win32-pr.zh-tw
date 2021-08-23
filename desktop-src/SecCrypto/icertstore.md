---
description: 提供 CAPICOM 存放區物件內容的存取權。 此內容允許將 CAPICOM 憑證存放區用於其他的 CryptoAPI 衍生。
ms.assetid: dc108e2d-d6ec-4972-9c8e-e6e738c25756
title: ICertStore 介面
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ICertStore
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: a48913b4bfb1fc28b612437a8f3b6934941c19b22683913f68d59f3f11d9e1c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119005576"
---
# <a name="icertstore-interface"></a>ICertStore 介面

\[CAPICOM 是僅限32位的元件，可供下列作業系統使用： Windows Server 2008、Windows Vista 和 Windows XP。\]

**ICertStore** 介面可讓您存取 CAPICOM [**存放區**](store.md)物件的內容。 此內容允許將 CAPICOM 憑證存放區用於其他的 CryptoAPI 衍生。

## <a name="when-to-use"></a>使用時機

當您需要在 CryptoAPI 的另一個衍生中使用 CAPICOM [**存放區**](store.md) 物件時，請使用此介面。

## <a name="members"></a>成員

**ICertStore** 介面具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**ICertStore** 介面具有這些方法。



| 方法                                        | 描述                                                                                                         |
|:----------------------------------------------|:--------------------------------------------------------------------------------------------------------------------|
| [**CloseHandle**](icertstore-closehandle.md) | 關閉透過 [**StoreHandle**](icertstore-storehandle.md) 屬性取得的 HCERTSTORE 控制碼。<br/> |



 

### <a name="properties"></a>屬性

**ICertStore** 介面具有這些屬性。



| 屬性                                                     | 存取類型           | 描述                                                                                                         |
|:-------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------|
| [**StoreHandle**](icertstore-storehandle.md)<br/>     | 讀取/寫入<br/> | 設定或抓取證書存儲的 HCERTSTORE 控制碼。<br/>                                          |
| [**StoreLocation**](icertstore-storelocation.md)<br/> | 讀取/寫入<br/> | 設定或抓取證書存儲的 [**CAPICOM \_ 存放區 \_ 位置**](capicom-store-location.md) 。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|----------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 




