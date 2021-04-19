---
description: 提供 CAPICOM 鏈物件內容的存取權。 此內容允許將 CAPICOM 憑證信任鏈用於其他的 CryptoAPI 衍生。
ms.assetid: ee258586-028e-486e-8129-07f43b6cc468
title: IChainCoNtext 介面
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IChainContext
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 34ba471c50ceb9475121139c3ecb997cf1d26f2b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001489"
---
# <a name="ichaincontext-interface"></a>IChainCoNtext 介面

\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。\]

**IChainCoNtext** 介面可讓您存取 CAPICOM [**鏈**](chain.md)物件的內容。 此內容允許將 CAPICOM 憑證信任鏈用於其他的 CryptoAPI 衍生。

## <a name="when-to-use"></a>使用時機

當您需要在 CryptoAPI 的另一個衍生中使用 CAPICOM [**鏈**](chain.md) 物件時，請使用此介面。

## <a name="members"></a>成員

**IChainCoNtext** 介面具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**IChainCoNtext** 介面具有這些方法。



| 方法                                           | 描述                                                                                                                    |
|:-------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------|
| [**FreeCoNtext**](ichaincontext-freecontext.md) | 釋放 \_ \_ 透過 [**ChainCoNtext**](ichaincontext-chaincontext.md) 屬性取得的 PCCERT 鏈內容。<br/> |



 

### <a name="properties"></a>屬性

**IChainCoNtext** 介面具有這些屬性。



| 屬性                                                      | 存取類型           | Description                                                               |
|:--------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------|
| [**ChainCoNtext**](ichaincontext-chaincontext.md)<br/> | 讀取/寫入<br/> | 設定或抓取憑證的 PCCERT \_ 鏈 \_ 內容。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|----------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 




