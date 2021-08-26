---
title: 程式格式字串
description: 以下是完整的格式字串描述。 它會組合與解譯器演進的不同階段相關的所有層級。
ms.assetid: fab603ed-1f68-4e0b-9c8d-b9730b8cd389
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb17434a1c05b66212283237d61ee4492aa23ed0bf1ecca75f1fec1b3ddd784b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120019056"
---
# <a name="procedure-format-strings"></a>程式格式字串

以下是完整的格式字串描述。 它會組合與解譯器演進的不同階段相關的所有層級。

## <a name="procedure-descriptor-overview"></a>程式描述項總覽

程式描述項是由標頭描述元和參數描述元所組成。 在目前的 RPC 程式設計中， [**-Oi**](/windows/desktop/Midl/-oi) 樣式描述會視為過時。 **– Oif** 被視為較新的。

## <a name="the-oi-style-description"></a>– Oi 樣式描述

此描述包含下列各項：

``` syntax
-Oi_style_header_descriptor<>
{-Oi_style_parameter_descriptor<>}*
```

標頭的大小為6到16個位元組。

在 [**– Oi**](/windows/desktop/Midl/-oi) 模式下編譯時，會產生完整的描述。 在 [**–作業系統**](/windows/desktop/Midl/-os) 模式中，只會產生參數描述項，以用於轉換。 Pickling 解譯器會使用舊的樣式參數描述元。

## <a name="the-oif-style-description"></a>– Oif 樣式描述

描述包含下列各項：

``` syntax
-Oif_style_header_descriptor<>
{-Oif_style_parameter_descriptor<6>}*
```

[**– Oif**](/windows/desktop/Midl/-oi)樣式標頭描述項包含

在編譯器的 [**Oif**](/windows/desktop/Midl/-oi) 或 **-Oicf** 模式中進行編譯時，會產生– Oif 樣式描述。

``` syntax
-Oi_style_header_descriptor<>
-Oif_extensions_to_the_old_header<6>
```

某些較新的功能（例如管道、非同步和 [**/robust**](/windows/desktop/Midl/-robust) ）會在使用時強制執行編譯器的 [**– Oicf**](/windows/desktop/Midl/-oi) 模式。

## <a name="the-extended-oif-description"></a>外延– Oif 描述

描述包含下列各項：

``` syntax
-Oif_style_header_descriptor<>
extensions_to_the_-Oif_header<8>
{-Oif style parameter descriptors<6>}*
```

 

 