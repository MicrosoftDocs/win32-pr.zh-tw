---
title: 一般 MIDL 命令列語法
description: MIDL 編譯器會處理 IDL 檔案和選擇性的應用程式佈建檔， (ACF) 以產生一組輸出檔。
ms.assetid: 1906b374-d0d1-4ec8-9a00-c5228b4c29ca
keywords:
- 命令列參考 MIDL，一般語法
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14baa145c7be03467a24bd4298cf2f502d93b6ba
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840728"
---
# <a name="general-midl-command-line-syntax"></a>一般 MIDL 命令列語法

MIDL 編譯器會處理 IDL 檔案和選擇性的應用程式佈建檔， (ACF) 以產生一組輸出檔。 IDL 檔案的介面屬性清單中指定的屬性，會決定編譯器是否要產生 RPC 介面的來源檔案，或自訂的 OLE 介面。

## <a name="switch-options"></a>切換選項

``` syntax
     midl [command-line-switch [switch-options]] filename
    
```

<dl> <dt>

<span id="command-line-switch"></span><span id="COMMAND-LINE-SWITCH"></span>*命令列參數*
</dt> <dd>

指定 MIDL 編譯器命令列參數。 參數可以依任何順序出現。

</dd> <dt>

<span id="switch-options"></span><span id="SWITCH-OPTIONS"></span>*切換-選項*
</dt> <dd>

指定與每個參數相關聯的選項。 有效的選項會在每個 MIDL 編譯器參數的參考專案中描述。

</dd> <dt>

<span id="filename"></span><span id="FILENAME"></span>*檔案名*
</dt> <dd>

指定 IDL 檔案的名稱。 這個檔案的副檔名通常是 .idl，但它可以有另一個或無。

</dd> </dl>

## <a name="remarks"></a>備註

下列清單顯示為名為 idl 的 IDL 檔案所產生之檔案的預設名稱。 您可以使用命令列參數來覆寫這些預設名稱。 請注意，IDL 檔案的名稱可以有 .idl 以外的副檔名，或完全沒有副檔名。

依預設 (也就是，如果介面屬性清單未包含 [**物件**](object.md) 或 [**本機**](local.md) 屬性) ，則編譯器會為 [RPC 介面](files-generated-for-an-rpc-interface.md)產生下列檔案：

-   用戶端 stub (名稱 \_ c.) 
-   伺服器 stub (名稱 \_ s. c) 
-   標頭檔 (名稱 .h) 

當 [**物件**](object.md) 屬性出現在 [介面屬性] 清單中時，編譯器會產生 COM 介面的下列檔案：

-   介面 proxy 檔案 (名稱 \_ p. c) 
-   介面標頭檔 (名稱 .h) 
-   介面 UUID 檔案 (名稱 \_ I .c) 

當 [**本機**](local.md) 屬性出現在介面屬性清單中時，編譯器只會產生介面標頭檔名稱 .h。

Microsoft RPC 提供的 MIDL 編譯器會視需要叫用 C 預處理器來處理 IDL 檔案。 它不會自動叫用 C 編譯器來編譯產生的檔案。

> [!Note]  
> Microsoft RPC 提供的 MIDL 編譯器所使用的命令列語法與 DCE IDL 編譯器不同。

 

MIDL 編譯器會將 [**/env**](-env.md)、 [**/server**](-server.md)、 [**/sstub**](-sstub.md)和 [**/out**](-out.md) 切換為伺服器 stub 檔案。

從 MIDL 版本6.0.359 開始，MIDL 編譯器的預設命令列選項是 [**/Oicf**](-oi.md)- [**/robust**](-robust.md)。 若要停用/robust，請指定 [**/no \_ 健全**](-no-robust.md) 的選項。

## <a name="the-header-file"></a>標頭檔

標頭檔包含 IDL 檔案中宣告之所有資料類型和作業的定義。 所有呼叫已定義作業的應用程式模組都必須包含標頭檔、執行定義的作業，或操作已定義的類型。

MIDL 編譯器參數 [**/header**](-header.md) 和 [**/out**](-out.md) 會影響標頭檔。

 

 




