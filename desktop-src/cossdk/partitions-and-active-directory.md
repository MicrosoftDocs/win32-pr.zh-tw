---
description: 除了包含一或多個應用程式的資料分割之外，COM + 也包含資料分割集，其中包含一或多個資料分割。
ms.assetid: 0b1a6daa-55e1-4a74-be01-e39473e3c0cc
title: 磁碟分割和 Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b08e7b70c4b474e7b7bd949f530fb73973d39c6a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973967"
---
# <a name="partitions-and-active-directory"></a>磁碟分割和 Active Directory

除了包含一或多個應用程式的資料分割之外，COM + 也包含資料 *分割集*，其中包含一或多個資料分割。 在 Active Directory 中建立的資料分割集會讓網域中的使用者存取整個網域的 COM + 應用程式。 在建立期間，會將每個特定的使用者或組織單位 (OU) 指派或對應至資料分割集。

單一使用者或 OU 可以存取多個分割區和其應用程式，因為使用者身分識別或 OU 與分割集之間有一對一的相互關聯。 如果沒有分割集，使用者或 OU 就需要多個使用者身分識別，才能存取不同分割區中的應用程式。

若要讓網域使用者可以使用 COM + 應用程式，系統管理員必須在 Active Directory 所在的網域控制站上，以及已安裝 COM + 應用程式的伺服器上執行工作。

## <a name="on-the-domain-controller"></a>在網域控制站上

系統管理員會先在 Active Directory 中建立磁碟分割。 您可以透過使用 Active Directory 消費者和電腦系統管理工具，或使用 Active Directory Services 介面 (ADSI) ，以程式設計方式來建立 COM + 分割。

在 Active Directory 中建立分割區之後，系統管理員會建立分割集。 在建立資料分割集時，系統管理員會定義該集合中包含的資料分割。 建立 COM + 分割集的方法是透過使用 Active Directory 消費者和電腦系統管理工具，或使用 (ADSI) 的 Active Directory Services 介面以程式設計方式進行。

最後，系統管理員會將網域使用者或組織單位 (Ou) 對應到新建立的資料分割集。 這是藉由顯示使用者的 [ **屬性** ] 頁面、存取 [ **Com + 資料分割集** ] 索引標籤，然後從清單方塊中選取資料分割集來完成。

## <a name="on-the-com-application-server"></a>在 COM + 應用程式伺服器上

系統管理員會建立新的磁碟分割，並指定相同的分割區名稱和資料分割識別碼 (GUID) 與在網域控制站 Active Directory 內建立的分割區識別碼相同。 這是使用 [元件服務] 系統管理工具內的 [ **Com + 磁碟分割** ] 資料夾來完成的。 為了簡化這項工作，[元件服務] 工具可讓系統管理員流覽 Active Directory，以選取所需的磁碟分割和其 GUID。

在應用程式伺服器上建立網域分割區時，使用者的預設分割區會成為 Active Directory 中分割集的預設資料分割。 最後，系統管理員可以將 COM + 應用程式安裝到應用程式伺服器上新建立的磁碟分割。

如需管理資料分割以供網域使用者存取的詳細資訊，請參閱與 Active Directory 消費者和電腦系統管理工具相關聯的說明。

## <a name="mapping-user-identities-and-ous-to-partition-sets"></a>將使用者身分識別和 Ou 對應到資料分割集

使用者和 Ou 可以對應到資料分割集。 藉由將 Ou 對應到資料分割集，系統管理員可以將多個使用者與一次資料分割集建立關聯，而不需要對應多個使用者識別。 單一使用者識別或 OU 只能對應到一個資料分割集。 一般情況下，將使用者身分識別或 Ou 對應到資料分割集，會執行下列動作：

-   確保應用程式可供網域中的適當使用者使用
-   協助 COM + 判斷應用程式所在的磁碟分割
-   建立使用者存取特定應用程式的許可權

若要將資料分割與 Active Directory 內的資料分割集建立關聯，並將使用者和 Ou 對應到這些分割集，系統管理員可以使用 Active Directory 消費者和電腦和元件服務系統管理工具。 在 Active Directory 中建立分割區時，系統管理員必須在要安裝相關 COM + 應用程式的電腦上，于本機設定該分割區。 在 Active Directory 中建立之分割區的本機設定是透過 [元件服務] 系統管理工具來完成。

如果網域使用者身分識別未對應到資料分割集，則會將使用者的 OU 存取權授與使用者，而該 OU 會對應到資料分割。 如果使用者的 OU 未對應到資料分割集，但階層中的下一個最高 OU 對應到該分割集，則使用者可以存取該資料分割。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[預設分割區](default-partitions.md)
</dt> <dt>

[本機分割區](local-partitions.md)
</dt> <dt>

[分割區屬性](partition-properties.md)
</dt> <dt>

[全域分割區](the-global-partition.md)
</dt> </dl>

 

 



