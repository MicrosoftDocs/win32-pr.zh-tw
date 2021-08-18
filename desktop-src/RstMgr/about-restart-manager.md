---
title: 關於重新開機管理員
description: 軟體安裝和更新需要系統重新開機的主要原因是，正在執行的應用程式或服務目前正在使用一些正在更新的檔案。
ms.assetid: 9a1166d7-a0e1-4948-9077-278c84afccac
keywords:
- 重新開機管理員重新開機管理員，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98003ff4193ce26eb4ed2a3bdab60db8d58adf86698c6b9369a80b8043458579
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010296"
---
# <a name="about-restart-manager"></a>關於重新開機管理員

軟體安裝和更新需要系統重新開機的主要原因是，正在執行的應用程式或服務目前正在使用一些正在更新的檔案。 重新開機管理員可讓所有重要的應用程式和服務關閉並重新啟動。 這會釋出使用中的檔案，並允許安裝作業完成。 它也可以消除或減少完成安裝或更新所需的系統重新開機次數。

重新開機管理員會依下列順序停止應用程式，並在更新應用程式之後，重新開機已註冊為以相反順序重新開機的應用程式。

1.  GUI 應用程式
2.  主控台應用程式
3.  Windows 服務
4.  Windows explorer

只有當呼叫者有權進行此作業時，重新開機管理員才會關閉應用程式或服務。 請注意，不支援跨會話的關機。

使用[Windows Installer](/windows/desktop/Msi/windows-installer-portal) 4.0 版進行安裝和服務的應用程式會自動使用重新開機管理員來減少系統重新開機。 自訂安裝程式也可以設計來呼叫重新開機管理員 API，以關閉並重新啟動應用程式和服務。 在無法避免系統重新開機的情況下，安裝程式可以使用重新開機管理員 API 來排程重新開機，以將使用者工作流程的停機時間降到最低。

如需在安裝和更新期間使用重新開機管理員 API 的詳細資訊，請參閱 [使用重新開機管理員](using-restart-manager.md)。

重新開機管理員無法停止和重新開機重要的系統服務，不需要重新開機系統。 如需識別重要系統服務的詳細資訊，請參閱 [重要的系統服務](critical-system-services.md)。

您的應用程式和服務應該準備好由重新開機管理員關閉，並儲存清除重新開機所需的使用者資料和狀態資訊。 如需如何準備您的應用程式和服務以使用重新開機管理員的詳細資訊，請參閱 [應用程式和服務的指導方針](guidelines-for-applications-and-services.md)。

如需重新開機管理員 API 的列舉、結構和函式的參考資訊，請參閱 [重新開機管理員參考](restart-manager-reference.md) 一節。

 

 