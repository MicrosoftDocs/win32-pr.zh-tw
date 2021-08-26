---
description: COM + 磁碟分割是一種邏輯容器，可讓應用程式獨立于這些應用程式的其他設定以外執行。
ms.assetid: c1290d10-968f-44f0-8099-d69c9e706c9e
title: 什麼是 COM + 磁碟分割？
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edc678089948770181d98af065afa414741055062ed2e942215de5d7cb8bc7b5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120070260"
---
# <a name="what-are-com-partitions"></a>什麼是 COM + 磁碟分割？

COM + 磁碟分割是一種邏輯容器，可讓應用程式獨立于這些應用程式的其他設定以外執行。 應用程式的每個設定都會安裝到個別的磁碟分割，而且可以根據其使用者的特定需求來個別管理。

在 COM + 元件啟用期間，資料分割服務會根據要求元件啟用的使用者身分識別，判斷要啟用的元件設定。 例如，有兩個不同群組、生產和定型的單一組織可以實作為 COM + 分割，以允許這兩個群組在同一部電腦上使用不同的 COM + 應用程式設定。

**Windows XP：** 無法使用建立、設定或委派 COM + 分割的能力。 全域分割區是唯一可用的 COM + 分割。

**Windows 2000：** Windows 2000 中無法使用 com + 分割服務。

## <a name="benefits-of-using-com-partitions"></a>使用 COM + 磁碟分割的優點

使用 COM + 分割可提供數個優點，包括下列各項：

-   組織可以使用較少的實體應用程式伺服器來支援需要多個應用程式設定的使用者，以降低其擁有權總成本 (TCO) 。
-   系統管理額外負荷會降低。 系統管理員不需要設定及管理多部電腦，而只需要在同一部電腦上設定和管理多個磁碟分割。 此外，您也可以透過加入新的 COM + 程式設計介面，以程式設計方式管理分割區。
-   您可以針對本機使用者、網域使用者和組織單位，以分割區為基礎來執行和管理安全性， (Ou) 。
-   程式設計人員和系統管理員可以使用 Microsoft 的開發和系統管理工具（例如 Windows SDK、Active Directory 消費者和電腦和元件服務系統管理工具）來管理 com + 分割。 分割區功能完全整合到這些工具中。

## <a name="primary-usage-scenario"></a>主要使用案例

客戶部署 COM + 分割功能的主要原因是裝載 Web 應用程式。 例如，假設小型軟體公司開發了一個可供醫院人員使用的 COM + 應用程式。 此應用程式是一種分散式 Web 應用程式，可讓醫院使用 SQL Server 資料庫來儲存及取出患者醫療記錄。

假設軟體公司有三個客戶：醫院 A、醫院 B 和醫院 C。雖然每個客戶都會在其桌上型電腦上本機執行 COM + 應用程式的用戶端，但 COM + 應用程式的伺服器端是位於軟體公司的內部網頁伺服器上，並由其客戶透過 Web 來存取。

由於每個醫院都有自己的一組儲存和抓取需求，以及自己的自訂患者資料集，因此軟體公司必須提供一種方式，讓應用程式的多個伺服器部分設定在 web 伺服器上同時執行。 COM + 分割可提供此問題的解決方案。

下圖顯示軟體公司的 COM + 應用程式的磁碟分割案例。

![顯示 com + 應用程式之資料分割案例的圖表，其中包含用戶端應用程式到 SQL server 資料庫的伺服器應用程式。](images/c4a96ff9-9afd-43c7-807c-4593cb77f51b.png)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[應用程式設計限制](application-design-restrictions.md)
</dt> <dt>

[COM + 佇列元件和分割區](com--queued-components-and-partitions.md)
</dt> <dt>

[分割區執行](partition-implementation.md)
</dt> <dt>

[在分割區中註冊和啟用元件](registering-and-activating-components-in-partitions.md)
</dt> </dl>

 

 



