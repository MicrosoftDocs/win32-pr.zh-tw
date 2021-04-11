---
title: 列舉應用程式目錄分割的複本
description: 本主題說明如何列舉應用程式目錄分割的複本。
ms.assetid: a1d6865b-ec77-4687-9da7-7fc717568bda
ms.tgt_platform: multiple
keywords:
- 列舉應用程式目錄分割 AD 的複本
- 應用程式目錄分割廣告，列舉的複本
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1415c147fe4320e5f8169487a656db4f365f03a
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "103933077"
---
# <a name="enumerating-replicas-of-an-application-directory-partition"></a>列舉應用程式目錄分割的複本

新增應用程式目錄分割的複本時，將包含複本之網域控制站的 [**nTDSDSA**](/windows/desktop/ADSchema/c-ntdsdsa)物件辨別名稱會加入至 [**交叉引用**](/windows/desktop/ADSchema/c-crossref)物件的 [屬性]-[[**位置**](/windows/desktop/ADSchema/a-msds-nc-replica-locations)] 屬性。 使用的 **交叉引用** 物件代表應用程式目錄分割。

**列舉應用程式目錄分割的複本**

1.  在 [資料分割] 容器中搜尋具有與應用程式目錄分割的辨別名稱相等的 [**nCName**](/windows/desktop/ADSchema/a-ncname)屬性值的 [**交叉引用**](/windows/desktop/ADSchema/c-crossref)物件。
2.  使用 [**交叉交叉**](/windows/desktop/ADSchema/c-crossref)系結物件之 [屬性]-[[**位置**](/windows/desktop/ADSchema/a-msds-nc-replica-locations)] 屬性的每個值，以系結至伺服器的 [**nTDSDSA**](/windows/desktop/ADSchema/c-ntdsdsa)物件。
3.  針對每個 [**nTDSDSA**](/windows/desktop/ADSchema/c-ntdsdsa) 物件的父系取得 ADsPath。 這是代表域控制器伺服器的物件。 使用 ADsPath 系結至 server 物件。
4.  取得伺服器物件的 [**dNSHostName**](/windows/desktop/ADSchema/a-dnshostname) 屬性值。 這是單一值屬性，其中包含伺服器的 DNS 名稱。

由於複寫延遲和已排程的 KCC 執行延遲，應用程式目錄分割的實際作用中複本可能不符合相互 [**引用**](/windows/desktop/ADSchema/c-crossref)物件的 [使用 [**NC-複本位置**](/windows/desktop/ADSchema/a-msds-nc-replica-locations)] 屬性所指示的網域控制站清單。 若要判斷應用程式目錄分割的實際使用中複本，更精確但較不有效率的方式是搜尋樹系中具有 [**hasMasterNCs**](/windows/desktop/ADSchema/a-msds-hasmasterncs)屬性的所有 [**nTDSDSA**](/windows/desktop/ADSchema/c-ntdsdsa)物件，其中包含應用程式目錄分割的辨別名稱。 **HasMasterNCs** 屬性包含網域控制站所裝載之所有可寫入目錄分割的辨別名稱，包括應用程式目錄分割。

 

 