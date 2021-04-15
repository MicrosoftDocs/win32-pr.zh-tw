---
title: 選擇性執行
description: 以下是選用的功能，但建議使用
ms.assetid: 6123bdda-06cf-4b8b-b2a8-89882b6341b4
ms.tgt_platform: multiple
keywords:
- 選用實行 ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 043b07f3a9bcfaef4bde8e95458d64828d4e46be
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507028"
---
# <a name="optional-implementation"></a>選擇性執行

以下是選用的功能，但建議使用：

-   非自動化用戶端的 [**>idirectorysearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) 介面。 因為 ADSI OLE DB 提供者會使用 **>idirectorysearch** 來呈現查詢並從基礎目錄服務收集結果，所以執行此介面的提供者會自動提供 OLE DB 樣式資料庫的存取權，而不需要執行任何額外的介面。
-   [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)、 [**IADsAccessControlList**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrollist)和 [**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry)介面。 建議支援以 ACL 為基礎之物件安全性的目錄服務提供者，以實行這些額外的功能。

 

 




