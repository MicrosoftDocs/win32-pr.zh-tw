---
description: 在應用程式伺服器上安裝時，COM + 會自動建立一個磁碟分割，稱為「全域分割區」。
ms.assetid: fbe894ae-5356-4522-884a-dc579a3a8dd3
title: 分割區執行
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0130b1d2daeddee28b01271aa6b767ebc5a7eac5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973398"
---
# <a name="partition-implementation"></a>分割區執行

在應用程式伺服器上安裝時，COM + 會自動建立一個磁碟分割，稱為「 *全域分割* 區」。 全域分割區包含一組標準的 COM + 應用程式。 安裝在全域分割區中的 COM + 應用程式，會自動提供給伺服器上的所有使用者使用。 如果您有其他 COM + 應用程式可供伺服器上的所有使用者使用，您可以將這些應用程式新增至全域資料分割。

除了全域分割區之外，您還可以針對該伺服器上的使用者或整個網域中的使用者建立其他磁碟分割。 建立額外的分割區，並在其中安裝多個 COM + 應用程式設定，可讓您的使用者在同一部電腦上同時執行這些應用程式設定。 此外，將 COM + 應用程式安裝到全域資料分割以外的磁碟分割中，就可以控制使用者對這些應用程式的存取。

**WINDOWS XP：** 無法使用建立、設定或委派 COM + 分割的能力。 全域分割區是唯一可用的 COM + 分割。

如需 Active Directory 中定義之本機分割區和分割區的詳細資訊，請參閱下列主題：

-   [本機分割區](local-partitions.md)
-   [磁碟分割和 Active Directory](partitions-and-active-directory.md)
-   [預設分割區](default-partitions.md)
-   [全域分割區](the-global-partition.md)
-   [分割區屬性](partition-properties.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[應用程式設計限制](application-design-restrictions.md)
</dt> <dt>

[COM + 佇列元件和分割區](com--queued-components-and-partitions.md)
</dt> <dt>

[在分割區中註冊和啟用元件](registering-and-activating-components-in-partitions.md)
</dt> <dt>

[什麼是 COM + 磁碟分割？](what-are-com--partitions-.md)
</dt> </dl>

 

 



