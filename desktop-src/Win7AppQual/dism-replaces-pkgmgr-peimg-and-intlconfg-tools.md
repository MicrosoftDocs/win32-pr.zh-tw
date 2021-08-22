---
description: 部署映像服務與管理 (DISM)
ms.assetid: bbfee966-121b-4b53-9e3e-08a747559da0
title: 部署映像服務與管理 (DISM)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b6da1cc8ec3e77a6c63df8e44917cb5f3474ae8e7a5e34b58f49255fa34b5b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119053176"
---
# <a name="deployment-image-servicing-and-management-dism"></a>部署映像服務與管理 (DISM)

## <a name="affected-platforms"></a>受影響的平臺

**客戶** 端-Windows Vista SP1 和更新版本 \| Windows 7  
**伺服器-Windows** server 2008 RTM 和更新版本 \| Windows server 2008 R2  


## <a name="description"></a>描述

部署映射服務與管理 (DISM) 工具會取代 Windows 7 中即將淘汰的 pkgmgr、PEImg 和 IntlConfg 工具。 DISM 提供單一的集中式工具，以更有效率且標準化的方式來執行這三項工具的所有功能，消除這些工具目前使用者所經歷的許多挫折來源。

DISM 包含 Windows Vista SP1 和更新版本的填充碼，以及適用于 Windows Server 2008 RTM 和更新版本的填充碼，可將在 Windows 7 上執行的繼承應用程式的 pkgmgr 呼叫重新導向至 DISM。 如果應用程式是在其中一個支援的作業系統上執行，填充碼會將呼叫路由傳送至 pkgmgr。 呼叫 PEImg 或 IntlConfg 的繼承應用程式不會有填充碼。

## <a name="usage"></a>使用方式

DISM 在任何支援的平臺上 pkgmgr 終端使用者是透明的。 但是，如果應用程式從 Windows 7 呼叫 PEImg 或 IntlConfg，則呼叫會失敗。

更新任何呼叫 pkgmgr、PEImg 或 IntlConfg 的腳本，以改為呼叫 DISM。 請務必包含 pkgmgr 腳本的更新，因為在未來的 Windows 作業系統版本中，將會移除為 pkgmgr 提供回溯相容性的填充碼。

檢查以確定對 DISM 的呼叫已取代任何對 pkgmgr、PEImg 和 IntlConfg 的呼叫，且作業順利執行。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[部署映射服務與管理 (TechNet) ](/previous-versions/windows/it-pro/windows-7/dd744256(v=ws.10))
</dt> </dl>

 

 
