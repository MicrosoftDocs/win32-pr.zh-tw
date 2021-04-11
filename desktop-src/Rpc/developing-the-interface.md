---
title: 開發介面
description: RPC 介面會描述伺服器程式所實行的遠端函式。
ms.assetid: f0dfe9d1-fe84-461c-8684-147fbd0bdefe
keywords:
- 遠端程序呼叫 RPC、工作、開發介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68b6f720bcd492e784ad07fe20e221ac54951680
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104093059"
---
# <a name="developing-the-interface"></a>開發介面

RPC 介面會描述伺服器程式所實行的遠端函式。 介面可確保用戶端和伺服器會在用戶端叫用伺服器提供的遠端程式時，使用相同的規則進行通訊。 介面是由介面名稱、某些屬性、選擇性類型或常數定義，以及一組程式聲明所組成。 每個程式宣告都必須包含程式名稱、傳回型別和參數清單。

介面是以 Microsoft 介面定義語言 (MIDL) 來定義。 如果您熟悉 C 或 c + +，MIDL 介面定義看起來會相當簡單。 MIDL 在許多方面類似 C 和 c + +。

開發 RPC 應用程式時，會使用文字編輯器來定義介面，並將它儲存在副檔名為 .idl 的文字檔中。 如需詳細資訊，請參閱 [IDL 和 ACF](the-idl-and-acf-files.md)檔。 MIDL 編譯器會產生您的程式在用戶端和伺服器原始程式檔中所包含的標頭檔。 MIDL 編譯器也會產生兩個 C 來源檔案。 您可以將其中一個連結至您的用戶端程式，並將另一個連結至您的伺服器程式。 這兩個 C 來源檔案是用戶端和伺服器 stub。 如需用戶端和伺服器 stub 的總覽，請參閱 [RPC 的運作方式](how-rpc-works.md)。 如需 MIDL 編譯器的總覽，請參閱 [編譯 midl](using-midl.md)檔案。

根據預設，用戶端和伺服器 stub 都有相同的名稱，如果用戶端與伺服器 stub 連結，則可能會造成問題，反之亦然。 使用 MIDL [**/prefix**](/windows/desktop/Midl/-prefix) 選項可防止發生這個常見的錯誤。

下圖顯示建立介面的程式。

![使用/prefix 選項建立用戶端和伺服器 stub，以防止意外的編譯問題](images/idldev.png)

您也可能需要指定應用程式佈建檔， (ACF) ，以輸入 MIDL 編譯器。 如需應用程式佈建檔的詳細資訊，請參閱 [IDL 和 ACF](the-idl-and-acf-files.md)檔。

除了 MIDL 編譯器之外，您通常還需要使用 Uuidgen.exe 公用程式來產生 (UUID 的通用唯一識別碼，並與「GUID) 」一詞交換。 本節提供這兩種工具的相關資訊，分為下列主題：

-   [產生介面 Uuid](generating-interface-uuids.md)
-   [使用 MIDL](using-midl.md)

 

 