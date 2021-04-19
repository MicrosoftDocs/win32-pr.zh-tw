---
description: .
ms.assetid: bbfee966-121b-4b53-9e3e-08a747559da0
title: 部署映像服務與管理 (DISM)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 734ac9fae497eeb61d706a228fc1ffc6ea4da264
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980695"
---
# <a name="deployment-image-servicing-and-management-dism"></a>部署映像服務與管理 (DISM)

## <a name="affected-platforms"></a>受影響的平臺

**客戶** 端-WINDOWS Vista SP1 和更新版本的 \| windows 7  
**伺服器** -windows SERVER 2008 RTM 和更新版本的 \| Windows server 2008 R2  


## <a name="description"></a>Description

部署映射服務與管理 (DISM) 工具取代 Windows 7 中已淘汰的 pkgmgr、PEImg 和 IntlConfg 工具。 DISM 提供單一的集中式工具，以更有效率且標準化的方式來執行這三項工具的所有功能，消除這些工具目前使用者所經歷的許多挫折來源。

DISM 包含適用于 Windows Vista SP1 和更新版本的填充碼，以及 Windows Server 2008 RTM 和更新版本的填充碼，可將 pkgmgr 呼叫從 Windows 7 上執行的繼承應用程式重新導向至 DISM。 如果應用程式是在其中一個支援的作業系統上執行，填充碼會將呼叫路由傳送至 pkgmgr。 呼叫 PEImg 或 IntlConfg 的繼承應用程式不會有填充碼。

## <a name="usage"></a>使用方式

DISM 在任何支援的平臺上 pkgmgr 終端使用者是透明的。 但是，如果應用程式從 Windows 7 呼叫 PEImg 或 IntlConfg，則呼叫會失敗。

更新任何呼叫 pkgmgr、PEImg 或 IntlConfg 的腳本，以改為呼叫 DISM。 請務必包含 pkgmgr 腳本的更新，因為在未來的 Windows 作業系統版本中，將會移除為 pkgmgr 提供回溯相容性的填充碼。

檢查以確定對 DISM 的呼叫已取代任何對 pkgmgr、PEImg 和 IntlConfg 的呼叫，且作業順利執行。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[部署映射服務與管理 (TechNet) ](/previous-versions/windows/it-pro/windows-7/dd744256(v=ws.10))
</dt> </dl>

 

 
