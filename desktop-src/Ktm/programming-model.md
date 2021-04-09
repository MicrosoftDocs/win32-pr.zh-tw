---
description: 應用程式寫入器可以使用核心交易管理員 (KTM) ，來進行次要的原始程式碼變更，以新增交易檔案和登錄作業。
ms.assetid: 356c66dc-5ddd-472f-835c-2e2cb019bcfd
title: 使用交易
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 255e40fb38ca4bfb24acdce717f133dbcf0c76f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849656"
---
# <a name="working-with-transactions"></a>使用交易

應用程式寫入器可以使用核心交易管理員 (KTM) ，來進行次要的原始程式碼變更，以新增交易檔案和登錄作業。 一般而言，這會牽涉到建立交易，並將控制碼傳遞給交易式資源（例如 [交易式 NTFS](/windows/desktop/FileIO/transactional-ntfs-portal) 和交易登錄）所提供的其他函式。

KTM 提供的機制可讓您的應用程式參與交易，以及撰寫您自己的交易式資源管理員。 有一些函數可讓您建立、管理和使用四個核心物件類別：交易、交易管理員、資源管理員和登記。 如果您只是使用交易，您只需要使用交易對象，並使用這些函數：

-   [**CreateTransaction**](/windows/desktop/api/KtmW32/nf-ktmw32-createtransaction)
-   [**CommitTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-committransaction)
-   [**RollbackTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbacktransaction)

絕對不要假設交易處於作用中狀態。 交易可基於許多原因和隨時復原。

Windows 會將以控制碼為基礎的介面公開給系統資源。 若要使用作業系統物件，應用程式會先要求物件的控制碼，然後在後續的函式呼叫中使用這個控制碼來存取或修改物件。 控制碼通常可以不同的模式開啟;指定的模式會影響後續函式呼叫的語法。 例如，透過呼叫 [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) 開啟的檔案控制代碼，並將 *dwDesiredAccess* 旗標設為 [ **泛型 \_ READ** ]，就不能在修改檔案的呼叫中使用。

您可以使用 [分散式交易協調器](/previous-versions/windows/desktop/ms684146(v=vs.85)) 的使用者模式資源（例如 SQL 或 MSMQ），以及使用 KTM 的核心模式資源來進行協調。 首先，建立 DTC 交易或 [**system.object**](/dotnet/api/system.transactions?view=dotnet-plat-ext-3.1) 物件，然後呼叫 [**IKernelTransaction**](/previous-versions/windows/desktop/aa344210(v=vs.85)) 物件，您可以從中取得 KTM 控制碼。 **IKernelTransaction** 物件會建立隸屬于 DTC 交易的 KTM 交易。 使用這個控制碼，您可以建立交易對象，但使用 **DTC 或 system.string** 來表示交易結果。

 

 
