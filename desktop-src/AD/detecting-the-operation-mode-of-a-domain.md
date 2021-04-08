---
title: 偵測網域的操作模式
description: 在 Windows 2000 中，網域可在混合和原生兩種作業模式中執行。
ms.assetid: c20dec14-50ad-4f63-bd5c-222c2f2c83e4
ms.tgt_platform: multiple
keywords:
- 偵測網域 AD 的操作模式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7d871bd50c9a7462972992685d4226963a3eaff
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "103842096"
---
# <a name="detecting-the-operation-mode-of-a-domain"></a>偵測網域的操作模式

在 Windows 2000 中，網域可在兩種作業模式下執行：混合和原生。 混合模式應該用來包含在 Windows 2000 網域中執行 Windows NT 4.0 的網域控制站。 混合模式不支援萬用群組或嵌套群組。 如果網域中的所有網域控制站都是執行 Windows 2000，您可以使用原生模式。

若要以程式設計方式偵測 Windows 2000 網域的作業模式，請閱讀該網域之 [**domainDNS**](/windows/desktop/ADSchema/c-domaindns)物件的 [**ntMixedDomain**](/windows/desktop/ADSchema/a-ntmixeddomain)屬性。 值為零 (0) 表示該網域處於原生模式。 值 (1) 表示該網域處於混合模式。 您也可以使用 [**DsRoleGetPrimaryDomainInformation**](/windows/desktop/api/Dsrole/nf-dsrole-dsrolegetprimarydomaininformation) 函式來取得作業模式，以及有關網域及其狀態的其他資料。

若要系結至您的應用程式執行所在的使用者帳戶之網域的 [**domainDNS**](/windows/desktop/ADSchema/c-domaindns) 物件，請使用無伺服器系結和 rootDSE 來取得網域的辨別名稱，然後使用該辨別名稱系結至代表該網域的 **domainDNS** 物件。 如需無伺服器系結和 rootDSE 的詳細資訊，請參閱 [無伺服器系結和 rootdse](serverless-binding-and-rootdse.md)。

如需詳細資訊和示範如何以程式設計方式偵測網域作業模式的程式碼範例，請參閱 [判斷作業模式的範例程式碼](example-code-for-determining-the-operation-mode.md)。

 

 