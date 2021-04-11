---
title: 使用 __midl 預先定義的常數
description: 當 MIDL 編譯器處理輸入 IDL 和 ACF 檔時， \_ \_ 預設會定義 midl，並且用於條件式編譯以達成整個組建的一致性。
ms.assetid: ba9557f8-d398-4c87-993d-f4e545894cdd
keywords:
- MIDL 編譯器 MIDL，使用 _midl 預先定義的常數
- _midl 預先定義的常數 MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae49675b38dcc3cab2d3d41e4f48cd0637d78523
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021525"
---
# <a name="using-the-__midl-predefined-constant"></a>使用 \_ \_ Midl 預先定義的常數

當 MIDL 編譯器處理輸入 IDL 和 ACF 檔時， \_ \_ 預設會定義 midl，並且用於條件式編譯以達成整個組建的一致性。 這個階段會在標頭檔中使用 define 語句，例如 **MIDL \_ PASS**，並以一致的旗標加以取代。 Midl 常數的值會 \_ \_ 根據公式的 *主要*  \* 100 +*次要*（例如 midl ver）指出編譯器的主要版本。 6.0. x 將 \_ \_ midl 定義為600。

如果您選擇，可以覆寫此預設值，方法是在命令列上指定下列命令： **/u \_ \_ midl**。 如需詳細資訊，請參閱 [**/u**](-u.md)。

 

 




