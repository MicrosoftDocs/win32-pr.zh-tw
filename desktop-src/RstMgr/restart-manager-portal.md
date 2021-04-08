---
title: 重新開機管理員
description: 撰寫自訂安裝程式，以消除完成更新使用中的檔案所需的系統重新開機。 從程式關閉並重新啟動所有但重要的系統服務。
ms.assetid: 44b7975a-0093-4c8f-9a14-2a6bfd7a68a5
keywords:
- 重新開機管理員重新開機管理員
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1244cff7bc22fd2e7b6d2540051bd0984596086
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023813"
---
# <a name="restart-manager"></a>重新開機管理員

## <a name="purpose"></a>目的

重新開機管理員 API 可以消除或減少完成安裝或更新所需的系統重新開機次數。 在安裝或更新期間，軟體更新需要系統重新開機的主要原因是目前正在執行的應用程式或服務正在更新某些檔案。 重新開機管理員可讓所有的 [重要系統服務](critical-system-services.md) 關閉並重新啟動。 這會釋出使用中的檔案，並允許完成安裝作業。

## <a name="where-applicable"></a>適用時

重新開機管理員 DLL 會匯出可由標準或自訂安裝程式載入的公用 C 介面。 安裝程式可以使用重新開機管理員來註冊在安裝應用程式或更新期間應取代的檔案。 然後，在後續的更新或安裝期間，安裝程式可以使用重新開機管理員來判斷哪些檔案因為目前正在使用中而無法更新。 重新開機管理員可以關閉並重新啟動目前正在使用這些檔案的非關鍵服務或應用程式。 安裝程式可以指示重新開機管理員根據使用中的檔案、處理序識別碼 (PID) 或 Windows 服務的簡短名稱，來關閉和重新開機應用程式或服務。

重新開機管理員適用于桌面樣式應用程式的開發。

## <a name="developer-audience"></a>開發人員對象

本檔適用于想要充分利用 Windows Vista 或 Windows Server 2008 安裝程式功能的安裝應用程式開發人員。 使用 [Windows Installer](/windows/desktop/Msi/windows-installer-portal) 4.0 版進行安裝和服務的應用程式會自動使用重新開機管理員來減少系統重新開機。 自訂安裝程式也可以設計來呼叫重新開機管理員 API，以關閉並重新啟動應用程式和服務。 在無法避免系統重新開機的情況下，安裝程式可以使用重新開機管理員 API 來排程重新開機，以將使用者工作流程的停機時間降到最低。

## <a name="run-time-requirements"></a>執行階段需求求

從 Windows Vista 和 Windows Server 2008 開始，可以使用重新開機管理員 API。 重新開機管理員包含單一 DLL，應用程式可以載入該 DLL 來存取重新開機管理員 API。

## <a name="in-this-section"></a>本節內容



| 主題                                                                 | 描述                                                     |
|-----------------------------------------------------------------------|-----------------------------------------------------------------|
| [關於重新開機管理員](about-restart-manager.md)<br/>         | 描述重新開機管理員的總覽主題。<br/>   |
| [使用重新開機管理員](using-restart-manager.md)<br/>         | 使用重新開機管理員 API 的總覽主題。<br/> |
| [重新開機管理員參考](restart-manager-reference.md)<br/> | 重新開機管理員 API 的參考主題。<br/>        |



 

 

