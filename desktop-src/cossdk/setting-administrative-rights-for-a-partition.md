---
description: 設定資料分割的系統管理許可權
ms.assetid: d38e4a63-9ff9-4acb-bb7e-d6c96644bd32
title: 設定資料分割的系統管理許可權
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c421b37dd50fa21ee9cf146749ec00b0c91d98c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103688816"
---
# <a name="setting-administrative-rights-for-a-partition"></a>設定資料分割的系統管理許可權

已獲指派 COM + 系統應用程式系統管理員角色的使用者，可以建立、修改和刪除 COM + 分割。 在 [元件服務] 系統管理工具中，您可以藉由展開 COM + 系統應用程式的 [ **角色** ] 資料夾，將系統管理角色指派給使用者。

從 Windows Server 2003，COM + 系統應用程式的驗證功能包含 EOAC \_ DISABLE AAA 的值 \_ 。 此值會在啟動系統應用程式時，在 [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) 呼叫中使用停用的 (AAA) 啟用。 將驗證功能設定為 EOAC \_ DISABLE \_ AAA，可讓在特殊許可權帳戶下執行的應用程式 (例如 LocalSystem) ，以協助防止其身分識別用來啟動未受信任的元件。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[收集分割區計量](collecting-partition-metrics.md)
</dt> <dt>

[設定資料分割快取](configuring-the-partition-cache.md)
</dt> <dt>

[將應用程式群組至資料分割](grouping-applications-into-partitions.md)
</dt> <dt>

[管理本機磁碟分割](managing-local-partitions.md)
</dt> <dt>

[管理 Active Directory 內的磁碟分割](managing-partitions-within-active-directory.md)
</dt> </dl>

 

 
