---
description: 代表功能
ms.assetid: 34a4a015-614d-4fac-98d8-29ae43165798
title: 代表功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f969bcf6352cd4eef02c1580a93bebcbf769953e2ae658243b4499e6d1ca763
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117842700"
---
# <a name="representing-functionality"></a>代表功能

功能物件存在，可識別或以邏輯方式將裝置的功能分組。 例如，應用程式可以藉由尋找 SMS 功能物件，來看到裝置支援 SMS。 同樣地，應用程式可以藉由尋找靜止的影像捕捉功能物件，來看到裝置具有相機功能。

這種彈性的物件表示可讓具有多功能功能的裝置輕鬆支援。 驅動程式可以直接公開任何代表其裝置的功能物件，這比使用傳統裝置類別更細微。 物件標記法也有助於隔離重迭的功能片段;例如，有些電話可能有兩個相機或四個儲存體。

在 Windows 7 作業系統中，服務會提供豐富的功能查詢和抽象的內容群組，藉此擴充功能物件。 應用程式可以使用服務來探索裝置功能，並更有效率地與內容互動。 例如，應用程式可以藉由尋找連絡人服務物件，來查看裝置支援連絡人同步處理功能，並可將所有連絡人尋找為服務物件的子物件，而不需要以遞迴方式搜尋儲存體階層。

服務也允許應用程式在裝置上探索和叫用自訂行為。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**應用程式總覽**](application-overview.md)
</dt> </dl>

 

 



