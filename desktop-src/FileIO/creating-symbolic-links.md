---
description: 使用 CreateSymbolicLink 函數建立使用絕對或相對路徑的符號連結。
ms.assetid: 3821478d-87bb-4e47-8263-d977cf665503
title: 建立符號連結
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0340dc362ff550ab2d74e533ac66e74622c965266440103d6f6ec155bfa80f21
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118150854"
---
# <a name="creating-symbolic-links"></a>建立符號連結

函數 [**CreateSymbolicLink**](/windows/desktop/api/WinBase/nf-winbase-createsymboliclinka) 可讓您使用絕對或相對路徑來建立符號連結。

符號連結可以是絕對或相對連結。 絕對連結是指定路徑名稱的每個部分的連結;相對連結與指定路徑中的相對連結指定名稱，會決定相對連結。 相對連結會使用下列慣例來指定：

-   點 (。 和。。) 慣例，例如 \\ 「...」解析相對於上層目錄的路徑。
-   沒有斜線的名稱 (\\) ，例如 "tmp" 會解析相對於目前的目錄的路徑。
-   根目錄相對-例如，" \\ Windows \\ System32" 會解析為「*目前磁片磁碟機*： \\ Windows \\ System32」。 directory
-   目前的工作目錄相對，例如，如果目前的工作目錄是 "c： \\ Windows \\ System32"，"C:File.txt" 會解析為 "c： \\ Windows \\ system32 \\File.txt"。

    **注意**  如果您指定目前的工作目錄相對連結，則會建立為絕對連結，因為根據使用者和執行緒目前工作目錄的方式。

符號連結也可以同時包含連接點和裝載的資料夾，作為路徑名稱的一部分。

符號連結可以直接指向使用 UNC 路徑的遠端檔案或目錄。

相對符號連結會限制為單一磁片區。

## <a name="example-of-an-absolute-symbolic-link"></a>絕對符號連結的範例

在此範例中，原始路徑包含元件 '*x*'，這是絕對的符號連結。 當遇到 '*x*' 時，會將原始路徑的片段（最多加上 '*x*'）完全取代為 '*x*' 所指向的路徑。 在 '*x*' 之後，路徑的其餘部分會附加至這個新路徑。 這現在會變成修改過的路徑。

X： "C： \\ Alpha \\ Beta \\ absLink \\ gamma \\ file"

Link： "absLink" 對應至 " \\ \\ machineB \\ share"

修改的路徑： " \\ \\ machineB \\ share \\ gamma \\ file"

## <a name="example-of-a-relative-symbolic-links"></a>相對符號連結的範例

在此範例中，原始路徑包含元件 '*x*'，也就是相對的符號連結。 當遇到 '*x*' 時 *，' x*' 會完全由 '*x*' 所指向的新片段取代。 '*X*' 之後路徑的其餘部分會附加至新的路徑。  ( 的任何點。) 在這個新路徑中，取代在點 ( 之前出現的元件。) 。 每一組點都取代上述的元件。 如果 ( 的點數目。) 超過元件的數目，則會傳回錯誤。 否則，當所有元件取代都完成時，會保留最後一個修改過的路徑。

X： C： \\ Alpha \\ Beta \\ 連結 \\ gamma \\ 檔

Link： "link" 對應至 ".... \\ \\theta

修改的路徑： "C： \\ Alpha \\ Beta \\ ... \\ . \\theta \\ gamma \\ file "

最終路徑： "C： \\ theta \\ gamma \\ file"

## <a name="related-topics"></a>相關主題

<dl> <dt>

[符號連結](symbolic-links.md)
</dt> <dt>

[永久連結和接合](hard-links-and-junctions.md)
</dt> <dt>

[命名檔案、路徑和命名空間](naming-a-file.md)
</dt> </dl>

 

 



