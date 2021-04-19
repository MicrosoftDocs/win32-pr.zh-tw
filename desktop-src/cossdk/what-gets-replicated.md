---
description: 複寫的內容
ms.assetid: d1f0bc92-37bc-4de2-876a-e6b8b09da58d
title: 複寫的內容
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd2739cb0ff615ddc38f30a7aa9b0a572be5e28a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971319"
---
# <a name="what-gets-replicated"></a>複寫的內容

## <a name="applications"></a>應用程式

在來源電腦上安裝的所有應用程式都會進行複寫，但下列情況除外：

<dl> <dt>

<span id="Non-COM__application_elements_and_dependencies"></span><span id="non-com__application_elements_and_dependencies"></span><span id="NON-COM__APPLICATION_ELEMENTS_AND_DEPENDENCIES"></span>非 COM + 應用程式元素和相依性
</dt> <dd>

系統管理員必須負責複寫 COM + 應用程式相依的任何資訊，但這不是應用程式本身的一部分，例如資料檔案和 Dll。 COMREPL 不會在 COM + 應用程式元素之外複寫任何專案。

</dd> <dt>

<span id="COM__preinstalled_applications"></span><span id="com__preinstalled_applications"></span><span id="COM__PREINSTALLED_APPLICATIONS"></span>COM + 預先安裝的應用程式
</dt> <dd>

COM + 所使用並透過 COM + 安裝程式安裝的應用程式，則不會進行複寫。 這些選項包括：

-   系統應用程式
-   COM + 公用程式
-   COM + QC 無效信件佇列接聽程式

</dd> <dt>

<span id="Applications_created_by_IIS"></span><span id="applications_created_by_iis"></span><span id="APPLICATIONS_CREATED_BY_IIS"></span>IIS 所建立的應用程式
</dt> <dd>

這些應用程式不會複寫，並包含下列各項：

-   IIS 同進程應用程式
-   IIS 公用程式
-   針對隔離或集區虛擬根目錄建立的所有應用程式

</dd> </dl>

## <a name="computer-list"></a>電腦清單

在 [元件服務] 系統管理工具的 [ **電腦** ] 資料夾中指定的遠端電腦，將不會從來源複寫到目的電腦。

## <a name="properties"></a>屬性

以下是複寫的 **LocalComputer** 集合屬性：

-   TransactionTimeout
-   ResourcePoolingEnabled
-   DCOMEnabled
-   DefaultAuthenticationLevel
-   DefaultImpersonationLevel
-   SecurityTrackingEnabled
-   CISEnabled
-   SecureReferencesEnabled
-   InternetPortsListed
-   DeafultToInternetPorts
-   連接埠
-   RpcProxyEnabled

下列 **LocalComputer** 集合屬性不會複寫：

-   Description
-   ApplicationProxyRSN
-   IsRouter

如需 **LocalComputer** 集合屬性的說明，請參閱 [**LocalComputer**](localcomputer.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[檔案管理](file-management.md)
</dt> <dt>

[記錄和錯誤報表](logging-and-error-reporting.md)
</dt> <dt>

[複寫階段](replication-phases.md)
</dt> <dt>

[使用 COMREPL](using-comrepl.md)
</dt> </dl>

 

 



