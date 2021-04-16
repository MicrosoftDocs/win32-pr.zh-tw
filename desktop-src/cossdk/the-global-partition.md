---
description: 全域分割區
ms.assetid: db11e6f5-0a3d-44ce-9a51-90d7e2b80981
title: 全域分割區
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dc218067bbf7170a1c2df6f306b6dfe5787ac2f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468517"
---
# <a name="the-global-partition"></a>全域分割區

除了系統管理員定義的磁碟分割和資料分割集之外，每台電腦上都有一個特殊的資料分割，稱為「 *全域分割* 區」。 安裝 COM + 時，會自動建立全域資料分割。 全域分割區的設計目的是要包含伺服器或網域中的所有使用者都必須能夠存取的全系統應用程式。 將應用程式安裝到全域分割區，不需要將應用程式的複本安裝到每個個別使用者的磁碟分割集。

如果使用者的資料分割集未包含使用者嘗試存取的特定應用程式，但該應用程式安裝在全域分割區中，則會從全域分割區啟動應用程式。 不過，在此情況下，全域磁碟分割中安裝之應用程式的所有元件都必須標示為公用，而非私用元件。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[預設分割區](default-partitions.md)
</dt> <dt>

[本機分割區](local-partitions.md)
</dt> <dt>

[分割區屬性](partition-properties.md)
</dt> <dt>

[磁碟分割和 Active Directory](partitions-and-active-directory.md)
</dt> </dl>

 

 



