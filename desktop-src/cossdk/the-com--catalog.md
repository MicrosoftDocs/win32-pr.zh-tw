---
description: COM + 目錄會儲存 COM + 應用程式屬性、類別屬性和電腦層級的屬性。 它保證這些屬性之間的一致性，並在這些屬性上提供一般作業。
ms.assetid: 1838757c-aa8e-4678-8042-207498fb0bbc
title: COM + 類別目錄
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b345c45fddab245c1e2290dc279742ac7b3b6b25c093d677c74b232077b43ae1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118305265"
---
# <a name="the-com-catalog"></a>COM + 類別目錄

COM + 目錄會儲存 COM + 應用程式屬性、類別屬性和電腦層級的屬性。 它保證這些屬性之間的一致性，並在這些屬性上提供一般作業。

COM + 類別目錄會使用兩個不同的存放區，如下所示：

-   COM + 註冊資料庫
-   Windows 登錄 (**HKEY \_ 類別 \_ 根目錄**) 

目錄提供這兩個存放區的統一、邏輯觀點，並透過 COM + 系統管理程式庫公開這些存放區。 此程式庫透過指令碼語言提供元件服務系統管理工具的所有功能。

如果現有的 com 元件不需要任何新的 com + 服務，則會在現有的 Windows 登錄中進行查閱。 com + 類別目錄也會針對類型程式庫和介面 proxy/存根登錄使用 Windows 登錄。

## <a name="split-registration"></a>分割註冊

針對實際已經存在於服務環境中的現有 COM 元件的新元件 (例如，) 的 MTS 元件，註冊的基本 COM 層面會儲存在 Windows 登錄和新的服務和屬性 (例如，已排入佇列的元件) 儲存在 com + 註冊資料庫中。 這稱為「 *分割註冊*」。

每個屬性只會儲存在一個位置： Windows 登錄或 com + 註冊資料庫。 新的 com 元件會以獨佔方式在 com + 註冊資料庫中註冊，並在 Windows 登錄中進行一些重複，讓現有的工具可以使用這些元件。

## <a name="transactional-updates-to-the-catalog"></a>目錄的交易式更新

目錄上的某些作業會以交易方式執行。 當您從交易元件叫用 COM + 系統管理程式庫時，會在呼叫元件的交易界限內進行 COM + 註冊資料庫的更新。

不過，牽涉到其他存放區變更的更新 (例如檔案系統和 Windows 登錄) 都不保證是完全交易。 中止的交易可讓這些存放區的狀態與對另一個或 COM + 註冊資料庫所做的任何變更不一致。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[建立 COM + 應用程式的安裝套件](creating-installation-packages-for-com--applications.md)
</dt> <dt>

[部署應用程式 proxy](deploying-application-proxies.md)
</dt> <dt>

[COMREPL 複製公用程式](the-comrepl-replication-utility.md)
</dt> </dl>

 

 



