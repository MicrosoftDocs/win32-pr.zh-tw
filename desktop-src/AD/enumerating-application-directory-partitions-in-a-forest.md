---
title: 列舉樹系中的應用程式目錄分割
description: 如同網域分割區，每個應用程式目錄分割都會以設定分割區之分割區容器中的交互參照物件來表示。
ms.assetid: dd1ff72d-ed19-4e8c-a401-a5b1b3d577e8
ms.tgt_platform: multiple
keywords:
- 列舉樹系 AD 中的應用程式目錄分割
- 應用程式目錄分割廣告，在樹系中列舉
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d42bbe28ef37932394721d0c234ba3970ac263b
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "104023247"
---
# <a name="enumerating-application-directory-partitions-in-a-forest"></a>列舉樹系中的應用程式目錄分割

如同網域分割區，每個應用程式目錄分割都會以設定分割區之分割區容器中的 [**交叉引用**](/windows/desktop/ADSchema/c-crossref) 物件來表示。 每個 **交叉引用** 物件都會儲存與其對應之資料分割相關的資料。

表示網域分割區的 [**交叉引用**](/windows/desktop/ADSchema/c-crossref)物件，可區別于以 [**systemFlags**](/windows/desktop/ADSchema/a-systemflags)屬性內容表示應用程式目錄分割的 **交叉引用** 物件。 代表網域分割區的 **交叉引用** 物件，會在 **systemFlags** 屬性中同時設定 [**ads \_ SYSTEMFLAG \_ cr \_ ntds \_ NC**](/windows/win32/api/iads/ne-iads-ads_systemflag_enum)和 **ads \_ SYSTEMFLAG \_ cr \_ ntds \_ 網域** 旗標。 代表應用程式目錄分割的 **交叉引用** 物件將會設定 **ADS \_ SYSTEMFLAG \_ CR \_ ntds \_ NC** 旗標，且不會在 **systemFlags** 屬性中設定 **ads \_ SYSTEMFLAG \_ CR \_ ntds \_ 網域** 旗標。

表示架構和設定分割區的 [**交叉引用**](/windows/desktop/ADSchema/c-crossref)物件也會設定 [**ads \_ SYSTEMFLAG \_ CR \_ ntds \_ NC**](/windows/win32/api/iads/ne-iads-ads_systemflag_enum)旗標，且不會在 [**systemFlags**](/windows/desktop/ADSchema/a-systemflags)屬性中設定 **ads \_ SYSTEMFLAG \_ CR \_ ntds \_ 網域** 旗標。 這需要將這兩個 **交叉引用** 物件區分成 [**nCName**](/windows/desktop/ADSchema/a-ncname) 屬性的內容。 代表架構容器的 **交叉引用** 物件的 **nCName** 屬性將與 RootDSE 物件的 **schemaNamingCoNtext** 屬性相同。 同樣地，代表設定容器的 **交叉引用** 物件的 **nCName** 屬性將與 RootDSE 物件的 **configurationNamingCoNtext** 屬性相同。

**若要識別樹系中的所有應用程式目錄分割，請執行下列步驟**

1.  在設定分割區的資料分割容器中，搜尋或列舉所有的 [**交叉引用**](/windows/desktop/ADSchema/c-crossref) 物件。
2.  如果 [**交叉引用**](/windows/desktop/ADSchema/c-crossref)物件未設定 [**ads \_ SYSTEMFLAG \_ CR \_ ntds \_ NC**](/windows/win32/api/iads/ne-iads-ads_systemflag_enum)旗標，或在 [**systemFlags**](/windows/desktop/ADSchema/a-systemflags)屬性值中設定 **ads \_ SYSTEMFLAG \_ CR \_ ntds \_ 網域** 旗標，請將物件從結果集中排除。
3.  藉由比較 [**交叉引用**](/windows/desktop/ADSchema/c-crossref)物件的 [**NCName**](/windows/desktop/ADSchema/a-ncname)屬性與 RootDSE 物件的 **schemaNamingCoNtext** 屬性，從結果集中排除架構資料分割。
4.  藉由比較 [**交叉引用**](/windows/desktop/ADSchema/c-crossref)物件的 [**NCName**](/windows/desktop/ADSchema/a-ncname)屬性與 RootDSE 物件的 **configurationNamingCoNtext** 屬性，從結果集中排除設定磁碟分割。
5.  結果集中其餘的 [**交叉引用**](/windows/desktop/ADSchema/c-crossref) 物件全都代表應用程式目錄分割。

 

 