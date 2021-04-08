---
title: 應用程式目錄分割複寫
description: 應用程式目錄分割最常用來儲存動態資料。
ms.assetid: b5fbec54-ee1a-4fe6-b4b7-67fc4e77d043
ms.tgt_platform: multiple
keywords:
- 應用程式目錄分割複寫廣告
- 應用程式目錄分割 AD，複寫
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41523b86ae8d3a744d4eb288c5b240a60222aa21
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "104023292"
---
# <a name="application-directory-partition-replication"></a>應用程式目錄分割複寫

應用程式目錄分割最常用來儲存動態資料。 由於資料的變更頻率高於樹系的設定資料，因此可以針對每個分割區設定應用程式目錄分割的複寫範圍和頻率。 您可以利用 Active Directory Domain Services 的複寫功能，但是可以微調複寫資料，以符合儲存在資料分割上的資料類型。

作業系統不會強制執行最大複本數目，但複本數目應保持最小值，以降低複寫動態應用程式目錄分割資料的效能影響。

KCC 會產生並維護應用程式目錄分割的複寫拓撲。

## <a name="application-directory-partition-replication-within-a-site"></a>網站內的應用程式目錄分割複寫

您可以設定控制應用程式目錄分割之網站內複寫的複寫間隔。 這樣可讓應用程式目錄分割中的動態資料比網域分割區中的靜態資料更快速地進行同步處理。 如需以程式設計方式設定應用程式目錄分割的詳細資訊，請參閱 [修改應用程式目錄分割](modifying-application-directory-partition-configuration.md)設定。

應用程式目錄分割的 [**交叉引用**](/windows/desktop/ADSchema/c-crossref) 物件上有兩個屬性，而每個 Windows 2000 和更新版本的網域控制站上有兩個登錄值，可控制對網站內的複寫協力電腦起始原始變更通知的延遲。

-   [**交叉引用**](/windows/desktop/ADSchema/c-crossref)物件的 [複寫 [**-通知-第一個-DSA-延遲**](/windows/desktop/ADSchema/a-msds-replication-notify-first-dsa-delay)] 屬性會指定在第一個複寫夥伴收到通知之前，原始物件變更之後的延遲（以秒為單位）。 每個網域控制站上的登錄值都可以指定類似的值。 在 Windows Server 2003 樹系中，預設的第一個延遲是15秒。 在混合模式的樹系中，預設的第一個延遲是五分鐘。
-   [**交叉引用**](/windows/desktop/ADSchema/c-crossref)物件的 [複寫 [**-通知-後續-DSA-延遲**](/windows/desktop/ADSchema/a-msds-replication-notify-subsequent-dsa-delay)] 屬性會指定後續通知到第二個、第三個和 [複寫] 夥伴之間的延遲（以秒為單位）。 每個網域控制站上的登錄值都可以指定類似的值。 在 Windows Server 2003 樹系中，預設的後續延遲為3秒。 在混合模式的樹系中，預設的後續延遲為30秒。

相互 [**引用**](/windows/desktop/ADSchema/c-crossref) 屬性適用于裝載應用程式目錄分割複本的所有網域控制站，而且只會影響 **交叉引用** 物件所識別的應用程式目錄分割的複寫。 登錄值只適用于設定這些值的網域控制站，並會影響網域控制站所裝載之所有磁碟分割的內部複寫。 如果未設定 **交叉引用** 屬性及其登錄值，網域控制站會使用預設值。 如果已設定登錄值，它們會覆寫在 **交叉引用** 物件中設定的任何值。 依預設，不會設定登錄和 **交叉引用** 值，因此會使用預設值。 這可讓系統管理員藉由設定 **交叉引用** 值來加速所有應用程式目錄分割複本的複寫，同時對每個網域控制站上的登錄設定啟用更細微的微調。

從 Windows Server 2003 開始，網域分割區也會使用 [**交叉引用**](/windows/desktop/ADSchema/c-crossref) 物件的這些屬性來控制網站內複寫延遲。 這是先前伺服器版本的變更，其中延遲間隔是由每個網域控制站上的登錄值所控制。 當樹系升級至 Windows Server 2003 時，只有在已從預設值修改現有的登錄值時，才會保留現有的登錄值。 登錄中的網域控制站通知間隔會覆寫儲存在分割區 **交叉引用** 物件上的通知間隔。

## <a name="application-directory-partition-replication-across-sites"></a>跨網站複製應用程式目錄分割

跨網站之應用程式目錄分割的複本會觀察到針對網域分割區和通用類別目錄複寫所做的站上複寫排程。 不過，裝載真正的變動性資料時，應用程式目錄分割的複本通常會在網站內，因為網站間複寫延遲可能無法接受，讓複本彼此保持一致。

## <a name="application-directory-partitions-are-not-replicated-to-global-catalogs"></a>應用程式目錄分割不會複寫到通用類別目錄

應用程式目錄分割中的物件不會複寫到通用類別目錄。 應用程式目錄分割會被想像成裝載動態資料和物件，而這可能不是可行的，也不適合用來廣泛地複寫物件。 基於這個理由，應用程式目錄分割提供控制範圍和複寫頻率。 因此，沒有理由讓這些物件複寫到通用類別目錄中，因此會散佈到通用類別目錄伺服器所在的整個樹系中。 這不會限制應用程式目錄分割中的物件使用標示為 [**isMemberOfPartialAttributeSet**](/windows/desktop/ADSchema/a-ismemberofpartialattributeset)之架構中的屬性。 如同任何網域控制站，通用類別目錄伺服器仍可設定為應用程式目錄分割的完整複本。

 

 