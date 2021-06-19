---
title: 列舉包含許多成員的群組
description: 瞭解如何使用資料 (範圍抓取) 的增量抓取，來列舉包含許多成員的 Azure Active Directory 群組。
ms.assetid: 78f81b09-2223-4b74-b8d5-7a97494c0324
ms.tgt_platform: multiple
keywords:
- 列舉包含許多成員的群組 Active Directory
- 群組 Active Directory，列舉具有許多成員的群組
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7cab63b809fdbd2666f39a09d32f601346da00e
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405151"
---
# <a name="enumerating-groups-that-contain-many-members"></a>列舉包含許多成員的群組

群組的成員會儲存在名為 **member** 的多重值屬性中。 **成員** 屬性可以包含大量的值。 當多重值屬性中的值數目變大時，列舉成員可能會沒有效率。 伺服器也會限制可在單一查詢中取出的最大值數目。 這表示，如果群組的成員可能超過伺服器所能提供的成員，列舉所有成員的唯一方法就是使用資料的累加抓取，稱為 *範圍* 抓取。

範圍抓取需要在單一查詢中要求有限數目的屬性值。 要求的值數目必須小於或等於伺服器支援的最大值數目。 若要減少查詢必須與伺服器聯繫的次數，要求的值數目應該盡可能接近此最大值。 若要讓應用程式能夠在所有伺服器上正常運作，應使用最大的1000數目。

提供所要求資料的伺服器版本會決定可在單一查詢中取出的最大值數目。 下表列出可在單一查詢中取出的伺服器版本和最大值數目。



| 伺服器作業系統版本 | 已抓取的最大值 |
|---------------------------------|--------------------------|
| Windows 2000                    | 1000                     |
| Windows Server 2003             | 1500                     |



 

如需使用 ADSI 來抓取屬性值範圍的詳細資訊，請參閱 [屬性範圍](/windows/desktop/ADSI/attribute-range-retrieval)抓取。

如需有關使用 [DirectoryServices](/dotnet/api/system.directoryservices)來抓取屬性值範圍的詳細資訊，請參閱 [列舉大型群組中的成員](https://msdn.microsoft.com/library/ms180907(v=VS.80).aspx)。

 

 