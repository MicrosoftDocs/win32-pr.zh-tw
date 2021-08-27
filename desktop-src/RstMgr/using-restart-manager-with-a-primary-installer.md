---
title: 搭配主要安裝程式使用重新開機管理員
description: 下列程式說明如何使用重新開機管理員來關閉和重新開機應用程式和服務。 使用重新開機管理員搭配單一安裝程式時，此安裝程式也是控制使用者介面的主要安裝程式。
ms.assetid: 8d2b4129-c595-4b11-9771-6dc953f4db40
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 764086166fc895d44f1a555f453d2941487c5d999adfa8d38581a12f07c9c45c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010006"
---
# <a name="using-restart-manager-with-a-primary-installer"></a>搭配主要安裝程式使用重新開機管理員

下列程式說明如何使用重新開機管理員來關閉和重新開機應用程式和服務。 使用重新開機管理員搭配單一安裝程式時，此安裝程式也是控制使用者介面的主要安裝程式。

**搭配主要安裝程式使用重新開機管理員**

1.  安裝程式會呼叫 [**RmStartSession**](/windows/desktop/api/RestartManager/nf-restartmanager-rmstartsession) 函式來啟動重新開機管理員會話，並取得會話控制碼和金鑰。
2.  安裝程式會呼叫 [**RmRegisterResources**](/windows/desktop/api/RestartManager/nf-restartmanager-rmregisterresources) 函數來註冊資源。 重新開機管理員只能使用已註冊的資源來判斷哪些應用程式和服務必須關閉並重新啟動。 所有可能受安裝影響的資源都應該向會話註冊。 您可以依檔案名、服務簡短名稱或 [**RM 的 \_ 唯一 \_ 進程**](/windows/desktop/api/RestartManager/ns-restartmanager-rm_unique_process) 結構來識別資源。
3.  安裝程式會呼叫 [**RmGetList**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetlist) 函式，以取得 [**RM \_ 進程 \_ 資訊**](/windows/desktop/api/RestartManager/ns-restartmanager-rm_process_info) 結構的陣列，其中列出必須關閉和重新開機的所有應用程式和服務。

    如果 [**RmGetList**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetlist)函數所傳回的 *lpdwRebootReason* 參數值為非零值，則重新開機管理員無法透過關閉應用程式或服務來釋放已註冊的資源。 在此情況下，需要系統關機並重新啟動，才能繼續安裝。 安裝程式應該會提示使用者輸入動作、停止程式或服務，或排程系統關機並重新啟動。

    如果 [**RmGetList**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetlist)函數所傳回之 *lpdwRebootReason* 參數的值為零，則安裝程式應該呼叫 [**RmShutdown**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown)函數。 這會關閉使用已註冊資源的服務和應用程式。 接著，安裝程式應該執行完成安裝所需的系統修改。 最後，安裝程式應該呼叫 [**RmRestart**](/windows/desktop/api/RestartManager/nf-restartmanager-rmrestart) 函式，讓重新開機管理員可以重新開機已關閉的應用程式，並已註冊重新開機。

4.  安裝程式可以使用 [**RmAddFilter**](/windows/desktop/api/RestartManager/nf-restartmanager-rmaddfilter) 函式，以防止指定的應用程式和服務被重新開機管理員作業關閉或重新開機。 [**RmGetFilterList**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetfilterlist)函式會傳回要從關機和重新開機進行篩選的應用程式和服務清單。 [**RmRemoveFilter**](/windows/desktop/api/RestartManager/nf-restartmanager-rmremovefilter)函數會移除篩選。
5.  安裝程式會呼叫 [**RmEndSession**](/windows/desktop/api/RestartManager/nf-restartmanager-rmendsession) 函數來關閉重新開機管理員會話。

如需示範如何使用主要安裝程式來啟動和使用重新開機管理員會話的範例程式碼片段，然後將次要安裝程式加入至現有的會話，請參閱搭配 [次要安裝程式使用重新開機管理員](using-restart-manager-with-a-secondary-installer.md)。

 

 




