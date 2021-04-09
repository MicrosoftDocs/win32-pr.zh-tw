---
title: 序列化服務
description: Microsoft RPC 支援兩種編碼和解碼資料的方法，統稱為資料的序列化方式。
ms.assetid: 36d6ea16-7d01-436e-ac32-610c3ddb8b8d
keywords:
- 遠端程序呼叫 RPC、描述、序列化
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fc5b877e29f7a7f6cd102663017f64bebfdff04
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675228"
---
# <a name="serialization-services"></a>序列化服務

Microsoft RPC 支援兩種編碼和解碼資料的方法，統稱為 *資料* 的序列化方式。 序列化表示資料會從您所控制的緩衝區封送處理和取消封送處理。 這與傳統的 RPC 使用方式不同，因為存根和 RPC 執行時間程式庫具有封送處理緩衝區的完整控制權，而進程是透明的。 您可以使用緩衝區來儲存永久媒體、加密等等。 當您編碼資料時，RPC 存根會將資料封送處理至緩衝區，並將緩衝區傳遞給您。 當您將資料解碼時，會提供封送處理緩衝區和其中的資料，並將資料從緩衝區取消封送處理至記憶體。 您可以根據程式或類型來進行序列化。

> [!Note]  
> *Pickling* 一詞通常是在開發人員用來描述序列化。 事實上，Windows SDK 範例包含名為 *pickle* 的目錄，它會保留 RPC 序列化範例程式。

 

針對其他用途，序列化會利用 RPC 機制來封送處理和封送處理資料。 例如，應用程式可以將不同類型的數個物件序列化為緩衝區，然後在單一作業中寫入整個緩衝區，而不是使用數個 i/o 作業將物件群組序列化為數據流。 操作序列化控制碼的函式與您所使用的序列化類型無關。

另一個範例是，如果您需要使用 RPC 以外的網路傳輸機制，例如 Microsoft Windows 通訊端 (Winsock) 。 使用 RPC 序列化時，您的程式可以呼叫函式，將您的資料封送處理為緩衝區，然後使用 Winsock 傳輸此資料。 當您的應用程式接收資料時，可以使用 RPC 序列化機制，從 Winsock 常式所填滿的緩衝區 unmarshal 資料。 這可為您提供 RPC 樣式應用程式的許多優點，同時也可讓您使用非 RPC 傳輸機制。

您也可以使用序列化進行與網路通訊無關的用途。 例如，當您使用 RPC 編碼函式將資料封送處理至緩衝區時，就可以將它儲存在檔案中，供其他應用程式使用。 您也可以將它加密。 您甚至可以使用它，在資料庫中儲存與硬體和作業系統無關的資料標記法。

下列主題提供 Microsoft RPC 支援的序列化服務討論：

-   [使用序列化服務](using-serialization-services.md)
-   [程式序列化](procedure-serialization.md)
-   [類型序列化](type-serialization.md)
-   [序列化控制碼](serialization-handles.md)

 

 




